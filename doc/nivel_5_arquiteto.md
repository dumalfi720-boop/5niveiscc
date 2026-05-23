# Level 5 — Architect

**Level 5** is when Claude stops being just a tool that you open to work and starts functioning as an **autonomous infrastructure**.

Here, Claude can run tasks even when you're not in front of the computer, react to events, execute routines, review code, send notifications and coordinate agents.

> At Level 4, Claude works as a technical team when you trigger.  
> At Level 5, Claude works as an autonomous system, with rules, triggers and supervision.

## What characterizes Level 5

Level 5 is marked by:

- routines in the cloud;
- automations triggered by events;
- security hooks;
- external control channels;
- execution without human interface;
- specialized agents;
- budget control;
- monitoring;
- gradual confidence.

This is the level at which Claude becomes a kind of **always on operation**.

## The big change from Level 5

The main change is to move away from:

> “Claude, do this task now.”

For:

> “Claude, run this task automatically when this event happens.”

Examples:

- when a pull request is opened, Claude reviews it;
- every Monday, Claude audits dependencies;
- every day at 8am, Claude generates a backlog summary;
- when a meeting is scheduled, Claude prepares a briefing;
- when a report arrives, Claude processes it and sends a summary.

Here you stop operating Claude manually and start designing **autonomous work systems**.

## What is it for in practice

### 1. Run routines in the cloud

**Cloud Routines** are saved configurations that run in the cloud environment, without depending on your computer being turned on.

At Level 3, scheduled tasks still depended on the open desktop.

At Level 5, the routine can run independently.

Practical examples:```text
Toda segunda-feira às 8h, revise as dependências do projeto e gere um relatório.
```

```text
Todo dia às 17h, resuma o que mudou no repositório e envie para mim.
```

```text
Toda sexta-feira, analise tarefas pendentes e gere uma lista de prioridades para a próxima semana.
```Actual use: Claude starts performing predictable routines without you needing to remember.

### 2. Trigger Claude by events

At Level 5, Claude can be triggered by external events.

Examples:

- new pull request on GitHub;
- new issue;
- new file in a folder;
- new line in a spreadsheet;
- new email received;
- completed form;
- meeting created in the calendar;
- API call;
- message in a channel.

Practical example:```text
Quando um novo pull request for aberto, revise o código e publique comentários com:
1. Possíveis bugs
2. Problemas de segurança
3. Pontos de melhoria
4. Sugestões de testes
```This type of automation changes Claude's role: he stops being reactive to you and starts being reactive to the system.

## 3. Use hooks as safety rails

**Hooks** are rules that fire before, during or after certain actions.

They serve to control risks.

### Pre-tool-use hook

Runs before Claude uses a tool or executes a command.

It serves to block dangerous actions.```text
Antes de qualquer comando que apague arquivos, peça confirmação humana.
Bloqueie automaticamente comandos como rm -rf, delete recursive ou reset hard.
```### Post-edit hook

Runs after Claude edits files.

Used to format, validate or record changes.```text
Depois de qualquer edição de código:
1. Rode o formatador
2. Rode lint
3. Registre os arquivos alterados
```### Stop hook

Runs when a task finishes.

It serves to notify you.```text
Quando a tarefa terminar, envie uma mensagem no Slack com:
1. O que foi feito
2. Arquivos alterados
3. Testes executados
4. Pendências
```### Response hook

Wheels when Claude responds.

This is to alert you when you need to return to the session.```text
Quando Claude precisar de aprovação humana, envie uma notificação.
```## 4. Create control channels

**Channels** allow you to control Claude outside of the terminal or the main app.

Channel examples:

- Discord;
- Telegram;
- iMessage;
- Slack;
- webhooks;
- internal panel;
- own app.

### One-way channel

An external event triggers Claude.```text
Quando uma reunião for criada no calendário, acione Claude para preparar um briefing.
```### Two-way channel

You talk to Claude through another channel.

Example on Telegram:```text
Revise o PR mais recente do projeto X e me mande um resumo.
```Claude executes in the configured environment and responds on the channel itself.

## 5. Run in headless mode

**Headless mode** means running Claude without an open chat interface.

You pass an instruction, Claude executes it, returns results and can forward it to another system.

Conceptual example:```text
claude -p "Analise os erros do log e gere um resumo"
```Possible uses:

- send results to Slack;
- save to file;
- feed another agent;
- create report;
- update panel;
- register in monitoring system.

This format is useful when Claude becomes part of an automated flow.

## 6. Use Agent SDK

The **Agent SDK** allows you to create your own products or systems using Claude as the engine.

Instead of just using Claude as a user, you start building tools on top of him.

Examples:

- customer service agent;
- document analysis agent;
- code review agent;
- financial agent;
- reporting agent;
- research agent;
- internal operations agent.

Practical example:

You create a system where the user sends a PDF, and the agent:

1. read the document;
2. extracts important information;
3. compares with an internal policy;
4. generates opinion;
5. saves result;
6. notify the person responsible.

## 7. Use remote control

Remote control allows you to follow or trigger sessions from another device.

Examples:

- start a task via cell phone;
- monitor execution in the browser;
- approve a step outside the computer;
- receive QR code or access link;
- continue monitoring while away.

Actual usage:```text
Verifique se os testes passaram e me avise se precisar de aprovação.
```## 8. Consolidate memory

At Level 5, poorly organized memory becomes a risk.

Over time, agents can accumulate:

- contradictory information;
- old data;
- duplicates;
- outdated decisions;
- vague references like “yesterday” or “last week”.

Memory consolidation serves to clean up and organize this.

Examples of what she does:

- removes contradictory facts;
- joins duplicate information;
- transforms relative dates into real dates;
- archives obsolete information;
- maintains only useful rules;
- reduces noise between sessions.

Practical prompt:```text
Revise os arquivos de memória deste projeto.

Tarefas:
1. Remova duplicatas.
2. Marque informações contraditórias.
3. Atualize datas relativas para datas absolutas.
4. Separe fatos atuais de históricos.
5. Gere um resumo das mudanças.
```## 9. Set task budget

In autonomous agents, cost and time can get out of control.

Therefore, Level 5 requires **task budgets**: limits for an execution.

Example:```text
Execute esta análise com orçamento máximo de 80.000 tokens.
Priorize:
1. Segurança
2. Bugs críticos
3. Testes ausentes
4. Documentação apenas se sobrar orçamento
```The idea is to make the agent self-regulate:

- think better at the beginning;
- avoid loops;
- prioritize the most important;
- close with summary;
- don't spend indefinitely.

## 10. Create agent teams

At Level 5, you can use multiple specialized agents coordinated by a lead agent.

Team example:

- lead agent;
- security officer;
- testing agent;
- documentation agent;
- UX agent;
- performance agent;
- architecture agent.

Unlike simple subagents, a team can share findings, divide tasks, and compare conclusions.

Practical example:```text
Monte uma equipe de agentes para revisar este novo módulo.

Papéis:
1. Arquiteto: avalia estrutura geral
2. Segurança: procura vulnerabilidades
3. Testes: verifica cobertura
4. UX: avalia fluxo do usuário
5. Documentação: confere clareza

O agente líder deve consolidar as conclusões e entregar um plano priorizado.
```## 11. Discover and reuse what already exists

At Level 5, the most important skill is not creating everything from scratch.

It’s knowing how to find and adapt:

- existing skills;
- MCP servers;
- templates;
- ready-made automations;
- open-source repositories;
- examples of agents;
- community integrations.

The logic is:

> First find out if something similar already exists. Then adapt it to your context.

This saves time and reduces errors.

## How to implement Level 5 safely

The biggest challenge at Level 5 is not technical.

It's **confidence**.

You shouldn't start by giving Claude full autonomy on critical tasks.

Start small.

### Step 1 — Low-risk routine

Example:```text
Todo dia às 8h, gere um resumo das tarefas pendentes e envie apenas para mim.
```Characteristics of a good first routine:

- does not send anything to customers;
- does not change important files;
- does not erase anything;
- does not deploy;
- just read, summarize and inform.

### Step 2 — Routine with human validation

Example:```text
Quando um pull request for aberto:
1. Revise o código.
2. Gere comentários sugeridos.
3. Não publique automaticamente.
4. Envie para minha aprovação.
```Claude works here, but you approve it first.

### Step 3 — Limited Automatic Action

Example:```text
Quando uma tarefa for concluída:
1. Atualize o status no quadro.
2. Envie resumo para o canal interno.
3. Não altere código.
4. Não envie mensagem externa.
```### Step 4 — Greater autonomy

Only after weeks of reliable execution do you release stronger actions.

Example:```text
Se o PR alterar apenas documentação:
1. Revise automaticamente.
2. Rode checks.
3. Comente aprovação se tudo estiver correto.
```## Complete practical example: automatic PR review

### Objective

Claude automatically reviews pull requests.

### Trigger

New PR opened on GitHub.

### Flow

1. Claude receives PR event.
2. Reads changed files.
3. Checks for risks.
4. Run review checklist.
5. Generates comments.
6. Submit for human or public approval as per rule.
7. Record summary.

### Security rules```text
Regras:
1. Nunca aprove PRs automaticamente se houver alteração em autenticação, pagamento ou permissões.
2. Nunca rode comandos destrutivos.
3. Se detectar segredo, token ou credencial, pare e avise imediatamente.
4. Se houver mudança em banco de dados, peça revisão humana.
5. Se os testes falharem, não aprove.
```## Complete practical example: automatic meeting briefing

### Objective

Prepare briefing before meetings.

### Trigger

New meeting on the calendar or meeting for the next day.

### Flow

1. Claude identifies participants.
2. Search related documents.
3. Summary of history.
4. To-do list.
5. Suggests questions.
6. Generate a briefing.
7. Sends it to you before the meeting.

### Routine prompt```text
Para cada reunião de amanhã, gere um briefing com:

1. Nome da reunião
2. Participantes
3. Contexto conhecido
4. Últimas decisões
5. Pendências
6. Riscos
7. Perguntas recomendadas
8. Próximos passos sugeridos

Envie apenas para mim.
```## Complete practical example: standalone weekly report

### Objective

Generate weekly report without manual intervention.

### Trigger

Every Friday at 4pm.

### Flow

1. Check completed tasks.
2. Check pending issues.
3. Group by project.
4. Highlight risks.
5. Generate report.
6. Submit for review.

### Routine prompt```text
Toda sexta-feira às 16h, gere um relatório semanal.

Formato:
1. Resumo executivo
2. Entregas da semana
3. Pendências
4. Riscos
5. Próximas ações
6. Itens que precisam da minha decisão

Não envie para clientes. Envie apenas para mim.
```## Level 5 security checklist

Before putting an autonomous routine to run, confirm:

- what is the trigger;
- what is the scope;
- what data it can access;
- what actions it can perform;
- what actions are prohibited;
- when to ask for human approval;
- how you will be notified;
- where the logs will be saved;
- how to interrupt the routine;
- how to review history;
- what is the token budget;
- what is the plan in case of error.

## Rules of thumb for autonomous automations```text
Regras gerais:
1. Nunca apague arquivos sem aprovação humana.
2. Nunca envie mensagens externas sem aprovação humana.
3. Nunca faça deploy sem confirmação explícita.
4. Nunca aprove mudanças críticas automaticamente.
5. Sempre registre o que foi feito.
6. Sempre avise quando encontrar erro.
7. Sempre pare em caso de dúvida.
8. Sempre respeite o escopo definido.
```## Where Level 5 generates the most value

Level 5 is especially useful for:

- technical teams;
- agencies;
- advanced freelancers;
- companies with many repetitive processes;
- teams that receive many PRs;
- businesses with recurring reports;
- operations with customer service and documents;
- projects that need constant monitoring.

## What to sell at Level 5

If you work with services, Level 5 allows you to sell more strategic solutions.

Examples:

- automatic review of PRs;
- weekly report agent;
- meeting briefing agent;
- monitor of pending tasks;
- dependency auditor;
- automatic ticket sorting;
- documentation agent;
- onboarding automation;
- document analysis agent;
- intelligent alert system.

Here you don’t sell “prompt”.

You sell **work infrastructure**.

## Common mistakes at Level 5

1. Giving too much autonomy too soon.
2. Not having logs.
3. No stop button.
4. Do not separate environments.
5. Don't set limits.
6. Trust without observing.
7. Automate bad processes.

## How to know that you have mastered Level 5

You are at Level 5 when:

- there are routines that run without you starting them manually;
- Claude reacts to events;
- there are security hooks;
- tasks have logs and notifications;
- you use external channels to trigger or follow up;
- agents have clear scope;
- there are budget limits;
- you start with low risk and gradually increase autonomy;
- Claude works even when you are not there;
- you think in systems, not conversations.

## Expected result

At Level 5, you gain:

- continuous automation;
- reduction of repetitive tasks;
- active monitoring;
- faster responses to events;
- constant technical review;
- automatic reports;
- more scalable operation;
- less dependence on your presence;
- ability to create more advanced products and services.

This is the level at which Claude becomes an infrastructure layer within the work.

## Practical 7-day plan to start Level 5

### Day 1 — Choose a simple routine

Choose something low risk.

Example:```text
Resumo diário das tarefas pendentes.
```### Day 2 — Define scope

Write:

- what you can read;
- what you can do;
- what you cannot do;
- when to stop.

### Day 3 — Create the output format

Define a fixed model.

Example:```text
1. Resumo do dia
2. Pendências
3. Riscos
4. Ações recomendadas
```### Day 4 — Add notification

Choose where to receive:

- email;
- Slack;
- Telegram;
- file;
- panel.

### Day 5 — Rotate manually

Before automating, run as a test.

### Day 6 — Schedule with supervision

Make it run automatically, but without sending it to third parties.

### Day 7 — Review logs

See:

- did you get it right?
- exaggerated?
- forgot something?
- did you invent something?
- do you need a new rule?

After that, adjust and repeat for a few weeks.

## Base prompt to create a Level 5 routine```text
Quero transformar esta tarefa em uma rotina autônoma.

Tarefa:
[descreva a tarefa]

Gatilho:
[quando deve rodar]

Fontes de informação:
[o que pode acessar]

Ações permitidas:
[o que pode fazer]

Ações proibidas:
[o que nunca deve fazer]

Quando pedir aprovação humana:
[condições]

Formato da entrega:
[modelo de saída]

Notificação:
[onde deve avisar]

Logs:
[onde registrar]

Limite:
[tempo, tokens ou escopo]

Antes de configurar, revise os riscos e sugira regras de segurança.
```## Level 5 Summary

Level 5 is the stage where Claude stops being “something you use” and becomes “something you operate”.

He can:

- run in the cloud;
- respond to events;
- trigger flows;
- review code;
- generate reports;
- prepare meetings;
- send alerts;
- coordinate agents;
- function as infrastructure.

But progress must be gradual.

First reading.  
Then draft.  
Then action with approval.  
Only then controlled autonomy.

The goal is not to let the AI ​​run wild.

The goal is to build a reliable system, with rules, limits, logs and supervision.