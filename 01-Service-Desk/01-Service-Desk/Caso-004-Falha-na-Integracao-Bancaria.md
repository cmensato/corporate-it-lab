# Caso 004 — Falha na Integração Bancária

**Área de estudo:** Service Desk  
**Competência principal:** APIs e Integrações  
**Nível:** Iniciante  
**Status:** Concluído

> Caso fictício desenvolvido para praticar a investigação de falhas em integrações entre ERP e APIs bancárias.

---

## 1. Objetivo

Investigar uma falha na baixa automática de boletos, identificar a causa utilizando logs e compreender o funcionamento básico de uma integração via API.

---

## 2. Cenário

Às 11h20, Fernanda, do Financeiro, informou que os boletos pagos pelos clientes não estavam sendo baixados automaticamente no ERP.

O banco confirmava o recebimento dos pagamentos, porém os títulos permaneciam em aberto no sistema.

O problema afetava aproximadamente 80 clientes.

---

## 3. Registro operacional do chamado

**Tipo:** Incidente

**Área solicitante:** Financeiro

**Serviço afetado:** Integração bancária (Retorno de boletos)

**Usuários afetados:** Financeiro

**Prioridade:** Alta

**Status inicial:** Em investigação

### Descrição

A baixa automática dos boletos deixou de ocorrer.

Os pagamentos estavam registrados pelo banco, porém não eram refletidos no ERP.

### Impacto

- Títulos permaneciam em aberto.
- Financeiro impossibilitado de conciliar recebimentos.
- Aproximadamente 80 clientes afetados.

---

## 4. Aplicação do método A.C.E.R.T.O.

### A — Analisar a demanda

Foi identificado um incidente coletivo relacionado ao processo automático de retorno bancário.

---

### C — Compreender o problema

Perguntas realizadas:

- Qual foi a última baixa realizada com sucesso?
- Outros usuários possuem o mesmo problema?
- O problema ocorre apenas no Contas a Receber?
- Alguma rotina foi executada de forma diferente?

Informações obtidas:

- Última baixa realizada às 18h12 do dia anterior.
- Todos os usuários do Financeiro apresentavam o mesmo problema.
- Contas a Pagar funcionava normalmente.
- A rotina automática deveria executar às 07h00.

---

### E — Entender o impacto

O problema impedia a atualização automática dos recebimentos.

O Financeiro não conseguia visualizar os pagamentos realizados pelos clientes.

Prioridade definida: **Alta**.

---

### R — Rastrear a causa

Foi verificado o agendamento da rotina automática.

Resultado:

```
Status: Executada

Resultado: ERRO
```

Análise do log:

```
HTTP 401 - Unauthorized

Token inválido
```

Foi realizada a verificação das credenciais da integração.

Resultado:

- Token expirado às 23h59 do dia anterior.

---

### T — Tratar a solução

Foi identificado que a integração utilizava um token expirado.

Foi gerado um novo token junto ao banco.

A credencial foi atualizada no ERP.

A rotina de importação foi reexecutada.

Os títulos passaram a ser baixados normalmente.

---

### O — Organizar o conhecimento

Após validação pelo Financeiro, o chamado foi encerrado.

Foi recomendada a implementação de monitoramento para alertar previamente sobre expiração de tokens.

---

## 5. Comunicação ao usuário

Foi identificado que a integração com o banco deixou de funcionar devido à expiração do token de autenticação.

Após a atualização da credencial e reprocessamento da rotina, as baixas foram realizadas normalmente.

---

## 6. Conclusão

O incidente não estava relacionado ao ERP nem ao banco.

A causa foi a expiração do token utilizado na autenticação da API.

A atualização da credencial restabeleceu a comunicação entre os sistemas.

---

## 7. Aprendizados

- Interpretar logs de integração.
- Compreender códigos HTTP.
- Investigar autenticação em APIs.
- Diferenciar erro de negócio de erro de infraestrutura.
- Validar a solução antes do encerramento.

---

## 8. Competências praticadas

- Atendimento ao usuário;
- Investigação de incidentes;
- APIs;
- Integrações;
- Leitura de logs;
- Autenticação;
- Comunicação;
- Documentação técnica.

---

## 9. Observação

Este caso é fictício e foi desenvolvido exclusivamente para treinamento e desenvolvimento profissional.
