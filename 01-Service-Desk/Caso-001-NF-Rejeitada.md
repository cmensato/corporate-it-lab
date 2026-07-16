# CASE 001 - Incidente na Emissão de Nota Fiscal

## Objetivo

Simular o atendimento de um incidente relacionado à emissão de Nota Fiscal, aplicando técnicas de investigação, comunicação com o usuário e gerenciamento de incidentes utilizando o método A.C.E.R.T.O.

---

# Cenário

**Data:** Segunda-feira - 08:17

A colaboradora Juliana, do departamento Financeiro, entrou em contato com a equipe de TI informando que não conseguia emitir Notas Fiscais.

Outro colaborador do mesmo setor (Carlos) também apresentava o mesmo problema.

O sistema permanecia operacional, porém a falha ocorria apenas no momento da emissão da Nota Fiscal.

Mensagem apresentada:

> Rejeição 108 - Serviço Paralisado Momentaneamente

---

# Competências Desenvolvidas

- Atendimento ao usuário
- Comunicação
- Investigação inicial
- Gestão de incidentes
- Priorização
- Análise de impacto
- Documentação técnica

---

# Método Utilizado

## A.C.E.R.T.O.

- Analisar a Demanda
- Compreender o Problema
- Entender o Impacto
- Rastrear a Causa
- Tratar a Solução
- Organizar o Conhecimento

---

# Atendimento Inicial

## Perguntas realizadas

- Desde quando ocorre o problema?
- Outros usuários apresentam o mesmo erro?
- Esse problema já aconteceu anteriormente?
- Em qual etapa ocorre o erro?
- A Nota Fiscal chega a ser gerada?
- Existe alguma mensagem de erro?

---

# Informações Coletadas

- O problema iniciou às 08:00.
- Outro usuário apresentava o mesmo comportamento.
- O sistema funcionava normalmente.
- O erro ocorria somente na emissão da Nota Fiscal.
- A mensagem apresentada era:

```
Rejeição 108
Serviço Paralisado Momentaneamente
```

---

# Análise do Impacto

## Áreas impactadas

- Financeiro
- Expedição
- Comercial

## Consequências

- Aproximadamente 140 Notas Fiscais aguardando emissão.
- Caminhões aguardando liberação.
- Atraso nas entregas.
- Interrupção do faturamento.

## Prioridade

**Alta**

Justificativa:

O incidente impactava diretamente a operação do negócio, porém não caracterizava indisponibilidade total do ERP.

---

# Hipóteses Levantadas

- Indisponibilidade da SEFAZ
- Falha na comunicação do ERP
- Problema no certificado digital
- Problema de integração
- Problema de rede

---

# Diagnóstico

Após a investigação, foi identificado comunicado oficial informando indisponibilidade temporária dos serviços da SEFAZ.

---

# Plano de Ação

- Abrir incidente geral.
- Comunicar os usuários impactados.
- Monitorar a normalização dos serviços.
- Validar a emissão após o retorno da SEFAZ.
- Encerrar o incidente somente após confirmação do funcionamento.

---

# Lições Aprendidas

- Nunca assumir a causa do problema apenas pela mensagem de erro.
- Sempre identificar o impacto no negócio antes de definir a prioridade.
- Evitar prometer prazos antes da investigação.
- Comunicação eficiente reduz abertura de chamados duplicados.
- O Analista de Sistemas nem sempre resolve tecnicamente o problema, mas é responsável por conduzir o incidente até sua conclusão.

---

# Competências Demonstradas

✅ Comunicação com usuários

✅ Investigação inicial

✅ Gestão de incidentes

✅ Priorização

✅ Visão de negócio

✅ Documentação

---

# Próximos Passos

- Aprender classificação de incidentes.
- Conhecer matriz de prioridade.
- Introduzir conceitos de ITIL.
