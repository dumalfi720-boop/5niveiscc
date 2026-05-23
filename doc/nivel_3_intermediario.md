# Level 3 — Intermediate

**Level 3** begins when Claude stops being just a conversation environment and starts **performing practical tasks on the computer**, with controlled access to files, folders, skills and routines.

It’s the point where you start thinking less about “give me an answer” and more about:

> “Claude, do this job for me.”

## What characterizes Level 3

In Level 1, Claude answers questions.

At Level 2, Claude works with projects, memory and documents.

At **Level 3**, Claude begins to act as an **operational colleague**, capable of organizing files, executing flows, applying models, generating deliverables and repeating processes with less supervision.

Simple example:

You don't just ask:

> “How do I organize this folder?”

You ask:

> “Organize this folder by file type, rename the documents following this pattern and generate a summary of what you found.”

## The big change in Level 3

The main change is to move away from:

> “Claude, tell me what to do.”

For:

> “Claude, go out there and do it.”

This completely changes the value of the tool, because it saves not only thinking time, but also **execution time**.

## What is it for in practice

### 1. Organize files and folders

One of the most useful applications of Level 3 is to let Claude work with real files.

Practical examples:

- “Analyze this folder of PDFs and separate them by subject.”
- “Rename the files using the pattern: data_cliente_tipo.”
- “Create a folder for each client and move the corresponding files.”
- “Read the documents and generate an index with a summary of each one.”
- “Find duplicate or misnamed files.”

Actual use: you transform a messy folder into an organized structure.

### 2. Process documents

Claude can help analyze, summarize, convert and reorganize documents.

Examples:

- “Read all PDFs in this folder and generate an executive summary.”
- “Extract the main decisions from these documents.”
- “Turn these texts into a report.”
- “Compare these two documents and highlight differences.”
- “Create a clearer and more professional final version.”

Actual use: you delegate reading, sorting and organizing information.

### 3. Create deliverables from files

At Level 3, Claude can produce more complete files based on existing materials.

Examples:

- “Based on these PDFs, create a 10-slide presentation.”
- “Turn these notes into a formal document.”
- “Build a spreadsheet with the data found in these files.”
- “Create a summary in Markdown with links to the original files.”
- “Generate a commercial proposal using this brief and this template.”

Actual use: Claude takes raw materials and turns them into something usable.

### 4. Use reusable skills

Skills are standardized instructions or flows that Claude can repeat.

Think of skills as “job recipes”.

Examples of skills:

- weekly report;
- contract analysis;
- meeting summary;
- proposal review;
- presentation creation;
- spreadsheet analysis;
- folder organization;
- script generation;
- delivery checklist.

The advantage is that you don't need to explain the complete process every time.

You can say:

- “Use the weekly report skill to generate the report for this folder.”
- “Use the business proposal flow with these files.”

## Practical example of a simple skill

A skill can say:```text
Quando eu pedir um relatório semanal:

1. Leia os arquivos da pasta indicada.
2. Separe informações por cliente.
3. Liste atividades realizadas.
4. Liste pendências.
5. Destaque riscos.
6. Gere um resumo executivo.
7. Salve o resultado na pasta de saída.
```Then, instead of explaining everything, you just ask:

> “Generate the weekly report from the Project X folder.”

### 5. Automate recurring tasks

At Level 3, you start scheduling or repeating tasks with less effort.

Examples:

- “Every day at 8am, generate a summary of today’s tasks.”
- “Every Friday, prepare a weekly report.”
- “Every Monday, review the client folder and tell me what is pending.”
- “Once a month, organize new files in the downloads folder.”

These routines may still depend on the computer being turned on and the application open, but they already represent a huge leap forward.

### 6. Control tasks via cell phone

With remote or mobile control features, you can trigger tasks even away from the computer.

Examples:

- “I'm on my cell phone. Ask Claude to organize the project files.”
- “Trigger the weekly summary routine.”
- “Ask me to prepare the material for tomorrow’s meeting.”

Actual use: you send the command on your cell phone and Claude works on the desktop.

### 7. Use Claude Design

At this level, Claude also begins helping with visual and product tasks.

You can order:

- “Create a landing page prototype for this service.”
- “Put together a presentation design based on this visual identity.”
- “Create a one-page to explain this offer.”
- “Design the structure of a capture page.”
- “Create an initial layout for a dashboard.”

The difference is that Claude not only writes the content, but helps put together the visual structure and flow.

### 8. Computer Use

When a tool does not have a direct connector, Claude can interact visually with it, like a person.

Examples:

- click on buttons;
- fill out forms;
- navigate screens;
- copy information;
- send commands;
- switch tabs.

Practical use:

> “Open this application, enter the reports screen, download the most recent file and save it in the project folder.”

This is a big leap, because Claude starts operating interfaces.

## How to configure Level 3 well

The secret of Level 3 is to provide structure for Claude to work safely.

You need to create a clear organization.

### Recommended folder structure```text
/Claude_Workspace
  /00_sobre_mim
  /01_templates
  /02_projetos
  /03_entradas
  /04_processando
  /05_outputs
  /06_arquivo
```### What to put in each folder

####`00_sobre_mim`Fixed information about you, your business, your style and your preferences.

Examples:

- who you are;
- what it does;
- how you prefer answers;
- types of customers;
- tone of voice;
- important rules.

####`01_templates`Templates that Claude can use, but must not change.

Examples:

- proposal model;
- report template;
- presentation template;
- email template;
- contract model;
- visual identity.

Important rule:

> “Never edit files in the templates folder. Just copy and use as a base.”

####`02_projetos`Separate folders for each project or client.```text
/02_projetos
  /cliente_A
  /cliente_B
  /conteudo
  /estudos
  /propostas
```

#### `03_entradas`Raw files that Claude must process.

Examples:

- PDFs;
- transcriptions;
- prints;
- spreadsheets;
- documents;
- transcribed audios.

####`04_processando`Temporary area for work in progress.

####`05_outputs`Where Claude must save final deliverables.

Examples:

- reports;
- presentations;
- summaries;
- spreadsheets;
- ready documents;
- checklists.

####`06_arquivo`Old or finished materials.

## Practical instruction for Claude at Level 3```text
Antes de começar qualquer tarefa, leia primeiro a pasta 00_sobre_mim.

Regras:
1. Nunca edite arquivos da pasta 01_templates.
2. Quando precisar usar um template, faça uma cópia.
3. Use a pasta 03_entradas para arquivos brutos.
4. Use a pasta 04_processando para rascunhos.
5. Salve entregáveis finais em 05_outputs.
6. Ao terminar, gere um resumo do que foi feito.
7. Se houver risco de apagar, sobrescrever ou mover arquivos importantes, peça confirmação antes.
```## Practical examples of use

### Example 1: Organize downloads```text
Organize minha pasta de downloads.

Tarefas:
1. Separe arquivos por tipo: PDFs, imagens, planilhas, documentos e outros.
2. Renomeie arquivos quando o nome estiver confuso.
3. Não apague nada.
4. Crie um resumo com o que foi encontrado.
5. Salve o resumo em outputs.
```### Example 2: Weekly report```text
Gere o relatório semanal do projeto Cliente A.

Use os arquivos da pasta do cliente.
Organize o relatório em:
1. Resumo executivo
2. Atividades realizadas
3. Pendências
4. Riscos
5. Próximos passos

Salve o resultado em outputs como relatório_semana_atual.md.
```### Example 3: Prepare meeting```text
Prepare um briefing para minha reunião de amanhã.

Leia:
- notas do projeto
- últimos documentos
- pendências abertas
- mensagens relevantes, se disponíveis

Gere:
1. Resumo do contexto
2. Principais decisões anteriores
3. Pontos de atenção
4. Perguntas para fazer na reunião
5. Próximas ações sugeridas
```### Example 4: Create presentation```text
Com base nos arquivos desta pasta, crie uma apresentação de 8 slides.

Estrutura:
1. Título
2. Problema
3. Contexto
4. Solução proposta
5. Benefícios
6. Plano de execução
7. Próximos passos
8. Encerramento

Use linguagem clara e profissional.
Salve a apresentação em outputs.
```### Example 5: Create service flow```text
Analise estes documentos e crie um fluxo de atendimento ao cliente.

Entregue:
1. Etapas do atendimento
2. Responsável por cada etapa
3. Mensagens padrão
4. Pontos de automação possíveis
5. Checklist operacional
```## What changes in your work

At Level 3, you start delegating entire blocks of work.

Before:

You read files, organize data, copy excerpts, assemble documents and save manually.

Now:

You define the result, give access to the material and Claude carries out much of the process.

## Important precautions

### 1. Give permissions carefully

Claude should only access necessary folders.

Avoid giving too broad access unnecessarily.

Best:

> “Work only in this project folder.”

Worst:

> “Use my entire computer.”

### 2. Protect templates

Templates should be read-only in practice.

Always say:

> “Do not edit the templates. Make copies.”

### 3. Never delete files without confirmation

Always include this rule:

> “Do not delete anything without my confirmation.”

### 4. Request final report

When concluding, Claude should say:

- what you did;
- which files you read;
- which files you created;
- where you saved it;
- what problems you encountered;
- which needs human review.

### 5. Start with low-risk tasks

Don't start by automating something sensitive.

Start with:

- organize copies of files;
- generate summaries;
- create drafts;
- assemble checklists;
- compare documents;
- prepare internal materials.

Then move on to more important tasks.

## How to know that you have mastered Level 3

You are at Level 3 when:

- Claude can work with his folders;
- you use skills for repeated tasks;
- you have a structure of inputs and outputs;
- you generate deliverables with less intervention;
- you use Claude to organize files;
- you schedule simple tasks;
- you trigger jobs via desktop or cell phone;
- you start thinking in processes, not just prompts.

## Expected result

At Level 3, you can save **10 hours or more per week**, mainly on operational tasks.

You get:

- organization;
- execution;
- standardization;
- repetition of processes;
- generation of deliverables;
- less rework;
- more ability to serve customers;
- basis for selling simple automations.

## Level 3 Limit

The limit is that there is still a lack of complete technical rigor.

Claude can perform tasks, but for more complex systems you still need:

- version control;
- code review;
- isolated environments;
- tests;
- branches;
- specialized subagents;
- more robust validation.

When you start needing real engineering, multiple parallel sessions, and more serious technical projects, enter **Level 4 — Advanced**, with Claude Code.