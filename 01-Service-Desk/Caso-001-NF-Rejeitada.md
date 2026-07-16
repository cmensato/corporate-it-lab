# Caso 001 — Incidente na emissão de NF-e

**Área de estudo:** Service Desk  
**Competência principal:** Gestão de incidentes  
**Nível:** Iniciante  
**Status:** Concluído  

> Caso fictício desenvolvido para simular a rotina de atendimento e investigação de incidentes em um ambiente corporativo.

---

## 1. Objetivo

Praticar o atendimento de um incidente relacionado à emissão de Nota Fiscal Eletrônica, aplicando investigação inicial, análise de impacto, priorização, comunicação com usuários e acompanhamento do incidente.

---

## 2. Cenário

Às 08h17, Juliana, colaboradora do setor Financeiro, informou à equipe de TI que não conseguia emitir NF-e.

Outro colaborador do mesmo setor também apresentava o problema. O ERP permanecia acessível e as demais funcionalidades estavam operando normalmente, mas a falha ocorria no momento da emissão da nota.

A mensagem apresentada era:

```text
Rejeição 108 — Serviço Paralisado Momentaneamente
```

---

## 3. Registro operacional do chamado

**Tipo:** Incidente  
**Área solicitante:** Financeiro  
**Serviço afetado:** Emissão de NF-e  
**Usuários afetados:** Múltiplos usuários  
**Prioridade:** Alta  
**Status inicial:** Em investigação  

**Descrição:**

Usuários do setor Financeiro impossibilitados de emitir NF-e. O ERP permanece disponível, porém apresenta a mensagem “Rejeição 108 — Serviço Paralisado Momentaneamente” durante a tentativa de emissão.

**Impacto identificado:**

- Aproximadamente 140 notas aguardando emissão;
- caminhões aguardando liberação;
- faturamento interrompido;
- risco de atraso nas entregas.

---

## 4. Aplicação do método A.C.E.R.T.O.

### A — Analisar a demanda

A demanda foi registrada como incidente porque uma funcionalidade que operava normalmente deixou de funcionar.

Foram identificados:

- usuário solicitante;
- área afetada;
- horário aproximado do início;
- serviço indisponível;
- existência de outros usuários impactados.

### C — Compreender o problema

Perguntas realizadas durante o atendimento:

- Desde quando o problema está ocorrendo?
- Outros usuários apresentam o mesmo erro?
- O sistema está acessível?
- Em qual etapa da emissão ocorre a falha?
- A NF-e chega a ser gerada?
- Existe alguma mensagem de erro?
- Esse problema já aconteceu anteriormente?

Informações coletadas:

- o incidente começou por volta das 08h;
- mais de um usuário foi afetado;
- o ERP estava acessível;
- a falha ocorria somente ao solicitar a emissão;
- a mensagem apresentada era a Rejeição 108.

### E — Entender o impacto

O incidente afetava diretamente o faturamento e a expedição.

Apesar de o ERP não estar totalmente indisponível, a empresa não conseguia concluir a emissão das notas e liberar os veículos para entrega.

Por esse motivo, o chamado foi classificado como prioridade alta.

### R — Rastrear a causa

Hipóteses consideradas:

- indisponibilidade dos serviços da SEFAZ;
- falha de comunicação entre o ERP e a SEFAZ;
- problema de rede;
- problema no certificado digital;
- falha na integração fiscal;
- indisponibilidade do serviço utilizado pelo fornecedor do ERP.

Antes de realizar alterações no sistema, foi verificada a existência de outros chamados semelhantes e de comunicados oficiais.

Foi identificado um comunicado de indisponibilidade temporária dos serviços da SEFAZ.

### T — Tratar a solução

Como a causa estava relacionada a um serviço externo, não havia uma correção interna imediata.

Ações executadas:

1. Registro de um incidente geral;
2. vinculação dos chamados relacionados;
3. comunicação aos usuários afetados;
4. orientação para evitar novos chamados duplicados;
5. acompanhamento da disponibilidade da SEFAZ;
6. validação da emissão após a normalização;
7. confirmação do funcionamento com os usuários.

### O — Organizar o conhecimento

Após a normalização do serviço:

- a emissão de NF-e foi testada;
- o funcionamento foi confirmado;
- os usuários foram comunicados;
- o incidente foi encerrado;
- o registro foi mantido como referência para ocorrências semelhantes.

---

## 5. Comunicação aos usuários

```text
Prezados,

Identificamos uma indisponibilidade temporária nos serviços da SEFAZ, afetando a emissão de NF-e.

A equipe de TI está acompanhando a situação. No momento, não é necessário abrir novos chamados relacionados a esse incidente.

Comunicaremos assim que o serviço for normalizado e validado.

Atenciosamente,
Equipe de TI
```

---

## 6. Conclusão

O incidente não exigiu uma correção técnica interna, mas exigiu gerenciamento, comunicação e acompanhamento até a normalização.

O papel do Analista de Sistemas não se limita a corrigir diretamente todos os problemas. Ele também deve confirmar a causa, avaliar o impacto, coordenar as ações, manter os usuários informados, validar o retorno do serviço e garantir o encerramento adequado do chamado.

---

## 7. Aprendizados

- Não assumir a causa apenas com base na mensagem apresentada.
- Perguntas sobre escopo, horário e etapa do erro reduzem hipóteses.
- A prioridade deve ser definida pelo impacto no negócio.
- Não prometer prazo antes de identificar a causa e as dependências.
- Incidentes coletivos devem ser centralizados para evitar chamados duplicados.
- Problemas externos também precisam ser acompanhados pela equipe de TI.
- O chamado só deve ser encerrado após teste e confirmação do usuário.

---

## 8. Competências praticadas

- Atendimento a usuários;
- gestão de incidentes;
- análise de impacto;
- priorização;
- investigação inicial;
- levantamento de hipóteses;
- comunicação corporativa;
- acompanhamento de serviço externo;
- documentação de chamados;
- visão de processos de negócio.

---

## 9. Observação

Este caso é fictício e foi elaborado exclusivamente para fins de estudo, prática e desenvolvimento profissional.
