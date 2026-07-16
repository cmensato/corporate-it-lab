# Caso 003 — Pedido cancelado por rotina de crédito

**Área de estudo:** Service Desk  
**Competência principal:** Investigação utilizando SQL  
**Nível:** Iniciante  
**Status:** Concluído

> Caso fictício desenvolvido para praticar investigação de incidentes utilizando consultas SQL e análise de processos de negócio.

---

## 1. Objetivo

Investigar o desaparecimento de um pedido no ERP utilizando consultas SQL, identificar a causa do incidente e propor melhorias no processo de negócio.

---

## 2. Cenário

Às 10h42, Patrícia, do Comercial, informou que o pedido **54821** não era mais encontrado no ERP.

Após a investigação inicial, foi confirmado que apenas esse pedido havia desaparecido.

O pedido havia sido criado no dia anterior e aprovado pelo gerente comercial.

O objetivo era identificar se o pedido havia sido excluído, alterado ou cancelado por alguma rotina do sistema.

---

## 3. Registro operacional do chamado

**Tipo:** Incidente

**Área solicitante:** Comercial

**Serviço afetado:** Consulta de pedidos no ERP

**Usuários afetados:** Comercial

**Prioridade:** Alta

**Status inicial:** Em investigação

### Descrição

Usuária informou que o pedido nº 54821 não era localizado no ERP.

Outros pedidos eram encontrados normalmente.

O problema afetava apenas um pedido.

### Impacto

- Pedido indisponível para consulta.
- Atendimento ao cliente comprometido.
- Possível atraso no faturamento.

---

## 4. Aplicação do método A.C.E.R.T.O.

### A — Analisar a demanda

Foi identificado que apenas um pedido apresentava comportamento anormal.

O ERP permanecia funcionando normalmente.

---

### C — Compreender o problema

Perguntas realizadas:

- Apenas esse pedido desapareceu?
- Outros usuários conseguem localizar o pedido?
- Qual a data de criação?
- Os pedidos anteriores e posteriores aparecem?
- O pedido chegou a ser aprovado?

Informações obtidas:

- Apenas o pedido 54821 não aparecia.
- Outros usuários também não localizavam o pedido.
- O pedido havia sido aprovado pelo gerente.

---

### E — Entender o impacto

O Comercial não conseguia consultar o pedido para responder ao cliente.

Apesar do ERP permanecer operacional, havia impacto direto no atendimento e no processo de vendas.

Prioridade definida: **Alta**.

---

### R — Rastrear a causa

Primeira consulta realizada:

```sql
SELECT *
FROM pedidos
WHERE numero_pedido = 54821;
```

Resultado:

| Pedido | Status | Usuário |
|--------|---------|---------|
|54821|CANCELADO|sistema|

Como o cancelamento havia sido realizado pelo usuário "sistema", foi consultado o histórico do pedido.

```sql
SELECT *
FROM historico_pedidos
WHERE numero_pedido = 54821
ORDER BY data_evento;
```

Resultado:

| Evento | Usuário | Origem | Motivo |
|---------|---------|---------|---------|
|Criado|Patrícia|ERP|Pedido criado|
|Aprovado|Gerente|ERP|Aprovado|
|Cancelado|Sistema|Rotina de Crédito|Cliente inadimplente|

Foi realizada nova consulta para validar a situação financeira do cliente.

```sql
SELECT *
FROM titulos_receber
WHERE cliente_id = 7821
AND status = 'VENCIDO';
```

Resultado:

Foram encontrados títulos vencidos.

Também foi confirmado que os títulos já estavam vencidos antes da criação e aprovação do pedido.

---

### T — Tratar a solução

Foi identificado que o ERP executou corretamente a rotina automática de cancelamento.

O incidente foi esclarecido ao Comercial.

Como oportunidade de melhoria, foi registrada solicitação para que o ERP valide a inadimplência antes da aprovação do gerente.

---

### O — Organizar o conhecimento

O incidente foi encerrado.

Foi aberta uma Solicitação de Melhoria para revisão da regra de negócio.

---

## 5. Comunicação ao usuário

Foi identificado que o pedido não havia sido excluído.

O ERP cancelou automaticamente o pedido durante a rotina de crédito em razão da existência de títulos vencidos do cliente.

Foi orientado o Comercial a verificar a situação financeira antes da criação de um novo pedido.

Também foi registrada uma solicitação de melhoria para impedir aprovações de pedidos quando o cliente já estiver inadimplente.

---

## 6. Conclusão

O problema não estava relacionado ao banco de dados ou ao ERP.

O sistema executou corretamente a regra de negócio existente.

Entretanto, foi identificada uma oportunidade de melhoria no fluxo operacional, evitando retrabalho e reduzindo expectativas incorretas junto ao cliente.

---

## 7. Aprendizados

- Utilizar SQL para investigação de incidentes.
- Diferenciar exclusão de cancelamento.
- Consultar histórico antes de concluir uma investigação.
- Validar regras de negócio antes de considerar um erro do sistema.
- Identificar oportunidades de melhoria durante a análise de incidentes.

---

## 8. Competências praticadas

- Atendimento ao usuário;
- Investigação utilizando SQL;
- Leitura de histórico de auditoria;
- Análise de processos;
- Regras de negócio;
- Comunicação;
- Documentação técnica;
- Melhoria contínua.

---

## 9. Observação

Este caso é fictício e foi desenvolvido exclusivamente para treinamento e desenvolvimento profissional.
