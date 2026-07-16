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
