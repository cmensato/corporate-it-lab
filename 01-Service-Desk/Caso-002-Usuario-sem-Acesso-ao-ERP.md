# Caso 002 — Usuário sem acesso ao ERP

| Informação | Valor |
|------------|-------|
| **Módulo** | Service Desk |
| **Categoria** | Gestão de Acessos |
| **Dificuldade** | ⭐ Iniciante |
| **Tempo estimado** | 20 minutos |
| **Ferramentas** | Active Directory |
| **Competência principal** | Investigação de Incidentes |

**Área de estudo:** Service Desk  
**Competência principal:** Gestão de acesso e autenticação  
**Nível:** Iniciante  
**Status:** Concluído  

> Caso fictício desenvolvido para simular o atendimento e a resolução de um incidente de acesso a sistema corporativo.

---

## 1. Objetivo

Praticar o atendimento de um incidente individual de autenticação no ERP, aplicando investigação inicial, levantamento de hipóteses, validação no Active Directory, resolução e documentação do chamado.

---

## 2. Cenário

Às 09h05, Marcos, colaborador do setor de Compras, informou à equipe de TI que não conseguia acessar o ERP.

O sistema abria normalmente, mas apresentava a seguinte mensagem após a tentativa de login:

```text
Usuário ou senha inválidos.
---

## 3. Registro operacional do chamado

**Tipo:** Incidente  
**Área solicitante:** Compras  
**Serviço afetado:** Autenticação no ERP  
**Usuário afetado:** Marcos  
**Prioridade:** Média  
**Status inicial:** Em investigação

**Descrição:**

Usuário informou que não conseguia acessar o ERP. O sistema abria normalmente, porém apresentava a mensagem "Usuário ou senha inválidos". O incidente afetava apenas um usuário.
---

## 4. Aplicação do método A.C.E.R.T.O.

### A — Analisar a demanda

O usuário Marcos informou que não conseguia acessar o ERP, recebendo a mensagem **"Usuário ou senha inválidos"** durante o login.

Inicialmente, o incidente foi registrado como um problema individual de autenticação.

---

### C — Compreender o problema

Perguntas realizadas:

- Qual mensagem de erro é apresentada?
- Apenas você está com esse problema?
- Outros usuários conseguem acessar normalmente?

Informações coletadas:

- O ERP abria normalmente;
- o erro ocorria apenas no momento do login;
- apenas o usuário Marcos era afetado;
- outro colaborador do mesmo setor acessava normalmente.

---

### E — Entender o impacto

O incidente impedia o usuário de executar suas atividades no ERP.

Como o problema afetava apenas um colaborador e não comprometia o funcionamento geral do sistema, foi classificado como prioridade **Média**.

---

### R — Rastrear a causa

Hipóteses levantadas:

- Caps Lock ativado;
- senha digitada incorretamente;
- senha expirada;
- usuário bloqueado;
- problema na autenticação (Active Directory).

Após descartar as hipóteses iniciais, foi realizada consulta ao Active Directory.

Resultado da verificação:

- Usuário ativo;
- conta não bloqueada;
- senha expirada.

---

### T — Tratar a solução

Foi realizada a redefinição da senha temporária conforme procedimento interno.

O usuário foi orientado a alterar a senha no primeiro acesso ao sistema.

Após a alteração da senha, o acesso ao ERP foi restabelecido.

---

### O — Organizar o conhecimento

O acesso foi validado juntamente com o usuário.

Após confirmação do funcionamento normal do ERP, o chamado foi encerrado e documentado para futuras consultas.


**Impacto identificado:**

- Usuário impossibilitado de acessar o ERP;
- impossibilidade de executar atividades do setor de Compras;
- impacto restrito ao colaborador.

---

## 5. Comunicação ao usuário

Após a redefinição da senha temporária, o usuário foi orientado a realizar um novo acesso ao ERP e alterar sua senha imediatamente.

O acesso foi validado com sucesso e o usuário confirmou o funcionamento normal do sistema.

---

## 6. Conclusão

O incidente foi causado pela expiração da senha do usuário no Active Directory.

Após a redefinição da senha temporária e a alteração para uma nova senha pelo usuário, o acesso ao ERP foi restabelecido com sucesso.

O chamado foi validado com o usuário antes do encerramento.

---

## 7. Aprendizados

- Confirmar o sintoma antes de iniciar a investigação.
- Não assumir que o problema está relacionado ao ERP apenas porque o usuário informou que "não consegue acessar".
- Sempre levantar hipóteses antes de executar ações.
- Validar informações diretamente nas ferramentas disponíveis reduz o tempo de atendimento.
- Confirmar a solução com o usuário antes de encerrar o chamado.

---

## 8. Competências praticadas

- Atendimento ao usuário;
- Investigação de incidentes;
- Levantamento de hipóteses;
- Troubleshooting;
- Active Directory (consulta);
- Gestão de acesso;
- Comunicação;
- Documentação técnica.

---

## 9. Observação

Este caso é fictício e foi desenvolvido exclusivamente para treinamento e desenvolvimento das competências de um Analista de Sistemas.
