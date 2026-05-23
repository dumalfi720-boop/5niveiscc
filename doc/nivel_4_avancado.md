# Level 4 — Advanced

**Level 4** begins when Claude stops being just a task performer and starts functioning as a **coordinated technical team**, especially using **Claude Code**.

Here, the focus is no longer just asking for answers, creating files or organizing folders. The focus becomes building, reviewing, testing, versioning and improving real systems.

> In Level 3, Claude does computer tasks.  
> At Level 4, Claude works as a technical team on structured projects.

## What characterizes Level 4

Level 4 is marked by:

-Claude Code;
- work on software projects;
- version control;
- planning before execution;
- multiple sessions in parallel;
- specialized subagents;
- testing and validation;
- custom commands;
- continuous improvement of the project context.

Here Claude stops being “an assistant” and starts to look like a small engineering team.

## The big change from Level 4

The main change is to move away from:

> “Claude, perform this task.”

For:

> “Claude, plan, implement, test, validate and deliver me a reviewable solution.”

At Level 3, you delegate tasks.  
At Level 4, you delegate **complete technical cycles**.

## What is it for in practice

### 1. Create real systems and tools

Examples:

- dashboards;
- websites;
- landing pages;
- internal systems;
- automations with backend;
- integrations with APIs;
- simple applications;
- administrative panels;
- tools for customers;
- robust scripts;
- extensions;
- functional prototypes.

Order example:```text
Crie uma ferramenta interna para controlar propostas comerciais.

Preciso de:
1. Cadastro de clientes
2. Status da proposta
3. Valor estimado
4. Próxima ação
5. Filtro por etapa
6. Exportação em CSV

Antes de implementar, analise a estrutura do projeto e me apresente um plano.
```### 2. Work with planning before execution

A common mistake is to ask Claude to leave the code immediately.

At Level 4, you use **planning mode**.

The logic is:

1. Claude analyzes the project.
2. Identifies relevant files.
3. Propose a plan.
4. Ask questions if necessary.
5. You approve.
6. Only then does he execute.

Practical prompt:```text
Antes de alterar qualquer arquivo, entre em modo planejamento.

Analise o projeto e me entregue:
1. O que precisa ser feito
2. Quais arquivos serão alterados
3. Riscos
4. Perguntas importantes
5. Plano passo a passo

Não implemente nada até eu aprovar.
```This reduces errors, unnecessary changes and rework.

## 3. Use the file`claude.md`

O `claude.md`It is one of the most important elements of Level 4.

It works like a **project manual** that Claude reads at the beginning of each session.

### What to put in`claude.md`

```markdown
# Projeto

Este projeto é uma aplicação para controle de propostas comerciais.

## Objetivo

Ajudar consultores a registrar clientes, acompanhar propostas e visualizar oportunidades em andamento.

## Stack

- Frontend: React
- Estilo: Tailwind
- Backend: Node.js
- Banco: Supabase

## Convenções

- Componentes em `/src/components`
- Páginas em `/src/pages`
- Funções utilitárias em `/src/lib`
- Usar nomes claros e descritivos
- Evitar arquivos muito longos

## Preferências

- Respostas em português do Brasil
- Código limpo e comentado apenas quando necessário
- Priorizar soluções simples
- Não criar dependências novas sem justificar

## Regras

- Nunca sobrescrever arquivos sem verificar antes
- Sempre rodar testes quando possível
- Sempre explicar o que foi alterado
- Não usar dados fictícios em produção
```### Rule of thumb

Keep the`claude.md`short.

Ideally:

- clear;
- objective;
- updated;
- with less than 200 lines;
- no excess details.

If you have long information, put it in separate files, for example:```text
/docs/regras-de-negocio.md
/docs/design-system.md
/docs/api.md
```And in`claude.md`, just reference:```markdown
Para regras de negócio detalhadas, consulte @docs/regras-de-negocio.md.
```## 4. Update`claude.md`when Claude makes a mistake

Whenever Claude makes a repeatable mistake, ask:```text
Atualize o claude.md com uma regra para evitar esse erro no futuro.
```Example:```text
Você criou este componente na pasta errada.

Atualize o claude.md dizendo que componentes reutilizáveis devem ficar em /src/components e páginas completas devem ficar em /src/pages.
```Over time, the project gets smarter and Claude makes fewer mistakes.

## 5. Use specialized subagents

Subagents are like experts within the team.

You can have agents to:

- tests;
- security;
- documentation;
- code review;
- UX;
- performance;
- accessibility;
- architecture;
- database;
- integration with APIs.

Practical example:```text
Use um subagente de revisão de código para analisar esta implementação.

Ele deve verificar:
1. Bugs prováveis
2. Problemas de segurança
3. Código duplicado
4. Falhas de performance
5. Pontos que precisam de testes
```Another example:```text
Use um subagente de documentação para criar uma explicação clara de como este módulo funciona.
```## 6. Work with parallel sessions

At Level 4, you can have multiple sessions of Claude working at the same time, each on an isolated task.

Example:

- session 1: creates new feature;
- session 2: fixes bug;
- session 3: write tests;
- session 4: improve documentation;
- session 5: reviews security.

This greatly increases productivity, but requires organization.

## 7. Use worktrees

Worktrees allow each session to work in an isolated space, without overwriting files from another session.

Example:```text
claude-worktree nova-feature-clientes
claude-worktree corrigir-bug-login
claude-worktree testes-dashboard
```This prevents two sessions from touching the same files at the same time.

## 8. Use branches clearly

Name examples:```text
feature/dashboard-clientes
fix/login-error
docs/api-readme
test/propostas-flow
refactor/components-table
```Helpful prompt:```text
Crie uma branch para esta tarefa com nome claro.
Implemente a mudança nela.
Ao terminar, gere um resumo para pull request.
```## 9. Create better pull requests

Ask Claude to generate:

- summary of the change;
- changed files;
- reason for the change;
- risks;
- how to test;
- screenshots, if applicable;
- next steps.

Practical model:```text
Prepare a descrição do pull request com:

1. Resumo
2. O que foi alterado
3. Por que foi alterado
4. Como testar
5. Riscos conhecidos
6. Checklist final
```## 10. Use check loop

The **verification loop** is essential.

It's not enough for Claude to say he's finished. He needs to test.

Always ask for:```text
Antes de me entregar, verifique seu próprio trabalho.

Rode os testes disponíveis.
Se for interface, abra no navegador, confira visualmente e tire screenshots.
Se encontrar erro, corrija e teste novamente.
Só me entregue quando passar na validação.
```Example:```text
Implemente a tela de cadastro de clientes.

Depois:
1. Rode lint
2. Rode testes
3. Abra a aplicação
4. Teste o fluxo manualmente
5. Verifique se não quebrou a tela de propostas
6. Gere um resumo final com evidências
```## 11. Use custom commands

If you repeat a prompt more than twice, turn it into a command.

Examples:```text
/revisar-codigo
/criar-pr
/gerar-testes
/documentar-modulo
/verificar-seguranca
/commit-push-pr
```Command example`/criar-pr`:

```markdown
Crie uma descrição de pull request com:

1. Título claro
2. Resumo da mudança
3. Arquivos principais alterados
4. Como testar
5. Riscos
6. Checklist
7. Próximos passos

Use linguagem objetiva e profissional.
```## 12. Use`/compact`to control context

Long sessions get heavy.

Use before the context is full.

Example:```text
Compacte o histórico mantendo:
1. Objetivo do projeto
2. Decisões tomadas
3. Arquivos alterados
4. Pendências
5. Regras importantes
```## 13. Use`/context`Use when the session feels heavy or confusing.```text
Mostre onde o contexto está sendo consumido e sugira o que pode ser compactado ou movido para documentação.
```## 14. Use`/rewind`when the attempt went wrong

When Claude takes a bad turn, go back to the previous point instead of endlessly correcting within the same context.

## 15. Use`/branch`to test alternatives```text
Crie uma branch para testar uma solução simples.
Depois criaremos outra branch para testar uma solução mais robusta.
```## 16. Use`/btw`for parallel questions```text
/btw O que esta função faz?
```This way you can resolve a doubt without changing the direction of the main task.

## 17. Use output styles

You can adapt your response style depending on the task.

Examples:

- code reviewer;
- technical architect;
- teacher;
- direct mode;
- documenter;
- security analyst.

Example:```text
Use um estilo de resposta como revisor técnico sênior: direto, crítico e focado em riscos.
```## Ideal process for a task at Level 4

### Step 1 — Prepare context```text
Leia o claude.md e os arquivos relevantes antes de responder.
```### Step 2 — Plan```text
Antes de implementar, apresente o plano e espere minha aprovação.
```### Step 3 — Implement```text
Implemente somente o que foi aprovado.
```### Step 4 — Test```text
Rode testes, lint e verificações disponíveis.
```### Step 5 — Review```text
Revise seu próprio trabalho e corrija problemas encontrados.
```### Step 6 — Document```text
Atualize documentação se necessário.
```### Step 7 — Deliver```text
Entregue um resumo final com arquivos alterados, testes feitos e próximos passos.
```## Complete prompt for Claude Code```text
Leia o claude.md antes de começar.

Tarefa:
[descreva a tarefa]

Antes de implementar:
1. Analise os arquivos relevantes.
2. Explique o problema.
3. Proponha um plano.
4. Liste arquivos que pretende alterar.
5. Aponte riscos.
6. Faça perguntas se houver ambiguidade.

Depois que eu aprovar:
1. Implemente em uma branch própria.
2. Rode lint e testes.
3. Verifique o resultado.
4. Corrija erros encontrados.
5. Gere uma descrição de PR.
6. Atualize documentação se necessário.
7. Entregue um resumo final.
```## Practical examples of use

### Example 1: Create a feature```text
Crie uma área de clientes no sistema.

Requisitos:
1. Listar clientes
2. Cadastrar novo cliente
3. Editar cliente existente
4. Filtrar por status
5. Salvar no banco atual

Antes de implementar, analise a arquitetura e proponha o plano.
```### Example 2: Fix bug```text
Existe um erro no login quando o usuário tenta recuperar senha.

Investigue:
1. Onde o erro acontece
2. Qual arquivo está envolvido
3. Qual é a causa provável
4. Como corrigir com o menor impacto

Depois implemente a correção e rode os testes.
```### Example 3: Create tests```text
Crie testes para o fluxo de propostas.

Inclua:
1. Cadastro de proposta
2. Alteração de status
3. Validação de campos obrigatórios
4. Filtro por cliente

Não altere a lógica principal sem justificar.
```### Example 4: Security Review```text
Revise este módulo como especialista em segurança.

Verifique:
1. Dados sensíveis expostos
2. Falta de validação
3. Riscos de permissão
4. Dependências perigosas
5. Logs indevidos

Entregue recomendações priorizadas por risco.
```### Example 5: Refactoring```text
Refatore este componente sem alterar o comportamento.

Objetivos:
1. Reduzir repetição
2. Melhorar nomes
3. Separar responsabilidades
4. Manter compatibilidade
5. Garantir que os testes continuem passando
```## Checklist before letting Claude change code

Before approving a task, check:

- Claude read the`claude.md`;
- he understood the objective;
- presented a plan;
- listed files that will change;
- explained risks;
- created branch or worktree;
- knows how to test;
- will not move outside the scope;
- will not add dependencies without permission;
- will deliver final summary.

## How this helps when working with clients

At Level 4, you can already deliver higher value work, because you leave the field of “simple automation” and enter **complete systems**.

Examples of salable deliveries:

- internal system for service control;
- indicator panel;
- automation with API;
- simple customer portal;
- sales dashboard;
- integration between tools;
- chatbot with knowledge base;
- functional prototype;
- improvement of existing system;
- technical project review.

## Common errors at Level 4

1. Leave Claude to code without a plan.
2. Using too long a session.
3. Not testing.
4. Mixing too many tasks.
5. Don't use version control.
6. Not documenting decisions.
7. Not updating`claude.md`.

## How to know that you have mastered Level 4

You are at Level 4 when:

- uses Claude Code with real projects;
- he has`claude.md`in projects;
- asks for a plan before execution;
- works with branches or worktrees;
- uses subagents for review, testing and documentation;
- runs validations before accepting deliveries;
- creates custom commands;
- can work with several sessions in parallel;
- generates well-described PRs;
- maintains updated project documentation;
- uses Claude as a coaching staff, not just an assistant.

## Expected result

At Level 4, you gain:

- development speed;
- technical quality;
- more complete deliveries;
- ability to work in parallel;
- reduction of rework;
- better documentation;
- more structured review;
- higher value salable projects.

The promise of this level is to move away from small tasks and start building **real systems**.

## Level 4 Limit

The limit of Level 4 is that you still coordinate everything manually.

You need:

- start sessions;
- approve steps;
- review results;
- trigger commands;
- monitor PRs;
- request audits;
- track recurring tasks.

When you realize that you are always repeating the same technical cycles, it is time to advance to **Level 5 — Architect**, where cloud routines, hooks, autonomous agents and automations that run even when you are not present come into play.