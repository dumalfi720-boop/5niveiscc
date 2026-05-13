# Nível 5 — Arquiteto

O **Nível 5** é quando Claude deixa de ser apenas uma ferramenta que você abre para trabalhar e passa a funcionar como **infraestrutura autônoma**.

Aqui, Claude pode rodar tarefas mesmo quando você não está na frente do computador, reagir a eventos, executar rotinas, revisar código, enviar notificações e coordenar agentes.

> No Nível 4, Claude trabalha como uma equipe técnica quando você aciona.  
> No Nível 5, Claude trabalha como um sistema autônomo, com regras, gatilhos e supervisão.

## O que caracteriza o Nível 5

O Nível 5 é marcado por:

- rotinas na nuvem;
- automações acionadas por eventos;
- hooks de segurança;
- canais externos de controle;
- execução sem interface humana;
- agentes especializados;
- controle de orçamento;
- monitoramento;
- confiança gradual.

Esse é o nível em que Claude vira uma espécie de **operação sempre ligada**.

## A grande mudança do Nível 5

A mudança principal é sair de:

> “Claude, faça esta tarefa agora.”

Para:

> “Claude, execute esta tarefa automaticamente quando este evento acontecer.”

Exemplos:

- quando abrirem um pull request, Claude revisa;
- toda segunda-feira, Claude faz auditoria de dependências;
- todo dia às 8h, Claude gera um resumo do backlog;
- quando uma reunião for marcada, Claude prepara um briefing;
- quando um relatório chegar, Claude processa e envia um resumo.

Aqui você deixa de operar Claude manualmente e passa a desenhar **sistemas de trabalho autônomos**.

## Para que serve na prática

### 1. Rodar rotinas na nuvem

As **Cloud Routines** são configurações salvas que rodam no ambiente da nuvem, sem depender do seu computador ligado.

No Nível 3, tarefas agendadas ainda dependiam do desktop aberto.

No Nível 5, a rotina pode rodar independentemente.

Exemplos práticos:

```text
Toda segunda-feira às 8h, revise as dependências do projeto e gere um relatório.
```

```text
Todo dia às 17h, resuma o que mudou no repositório e envie para mim.
```

```text
Toda sexta-feira, analise tarefas pendentes e gere uma lista de prioridades para a próxima semana.
```

Uso real: Claude passa a executar rotinas previsíveis sem você precisar lembrar.

### 2. Acionar Claude por eventos

No Nível 5, Claude pode ser acionado por acontecimentos externos.

Exemplos:

- novo pull request no GitHub;
- nova issue;
- novo arquivo em uma pasta;
- nova linha em uma planilha;
- novo e-mail recebido;
- formulário preenchido;
- reunião criada no calendário;
- chamada de API;
- mensagem em um canal.

Exemplo prático:

```text
Quando um novo pull request for aberto, revise o código e publique comentários com:
1. Possíveis bugs
2. Problemas de segurança
3. Pontos de melhoria
4. Sugestões de testes
```

Esse tipo de automação muda o papel de Claude: ele deixa de ser reativo a você e passa a ser reativo ao sistema.

## 3. Usar hooks como trilhos de segurança

**Hooks** são regras que disparam antes, durante ou depois de certas ações.

Eles servem para controlar riscos.

### Pre-tool-use hook

Roda antes de Claude usar uma ferramenta ou executar um comando.

Serve para bloquear ações perigosas.

```text
Antes de qualquer comando que apague arquivos, peça confirmação humana.
Bloqueie automaticamente comandos como rm -rf, delete recursive ou reset hard.
```

### Post-edit hook

Roda depois que Claude edita arquivos.

Serve para formatar, validar ou registrar mudanças.

```text
Depois de qualquer edição de código:
1. Rode o formatador
2. Rode lint
3. Registre os arquivos alterados
```

### Stop hook

Roda quando uma tarefa termina.

Serve para notificar você.

```text
Quando a tarefa terminar, envie uma mensagem no Slack com:
1. O que foi feito
2. Arquivos alterados
3. Testes executados
4. Pendências
```

### Response hook

Roda quando Claude responde.

Serve para alertar você quando precisa voltar à sessão.

```text
Quando Claude precisar de aprovação humana, envie uma notificação.
```

## 4. Criar canais de controle

**Channels** permitem controlar Claude fora do terminal ou do app principal.

Exemplos de canais:

- Discord;
- Telegram;
- iMessage;
- Slack;
- webhooks;
- painel interno;
- app próprio.

### Canal de mão única

Um evento externo aciona Claude.

```text
Quando uma reunião for criada no calendário, acione Claude para preparar um briefing.
```

### Canal de mão dupla

Você conversa com Claude por outro canal.

Exemplo no Telegram:

```text
Revise o PR mais recente do projeto X e me mande um resumo.
```

Claude executa no ambiente configurado e responde no próprio canal.

## 5. Rodar em modo headless

**Headless mode** significa rodar Claude sem uma interface de conversa aberta.

Você passa uma instrução, Claude executa, devolve resultado e pode encaminhar para outro sistema.

Exemplo conceitual:

```text
claude -p "Analise os erros do log e gere um resumo"
```

Possíveis usos:

- enviar resultado para Slack;
- gravar em arquivo;
- alimentar outro agente;
- criar relatório;
- atualizar painel;
- registrar em sistema de monitoramento.

Esse formato é útil quando Claude vira parte de um fluxo automatizado.

## 6. Usar Agent SDK

O **Agent SDK** permite criar produtos ou sistemas próprios usando Claude como motor.

Em vez de usar Claude apenas como usuário, você passa a construir ferramentas sobre ele.

Exemplos:

- agente de atendimento;
- agente de análise documental;
- agente de revisão de código;
- agente financeiro;
- agente de relatórios;
- agente de pesquisa;
- agente de operações internas.

Exemplo prático:

Você cria um sistema onde o usuário envia um PDF, e o agente:

1. lê o documento;
2. extrai informações importantes;
3. compara com uma política interna;
4. gera parecer;
5. salva resultado;
6. avisa o responsável.

## 7. Usar controle remoto

O controle remoto permite acompanhar ou acionar sessões a partir de outro dispositivo.

Exemplos:

- iniciar tarefa pelo celular;
- acompanhar execução no navegador;
- aprovar uma etapa fora do computador;
- receber QR code ou link de acesso;
- continuar monitorando enquanto está longe.

Uso real:

```text
Verifique se os testes passaram e me avise se precisar de aprovação.
```

## 8. Consolidar memória

No Nível 5, memória mal organizada vira risco.

Com o tempo, agentes podem acumular:

- informações contraditórias;
- dados antigos;
- duplicatas;
- decisões ultrapassadas;
- referências vagas como “ontem” ou “semana passada”.

A consolidação de memória serve para limpar e organizar isso.

Exemplos do que ela faz:

- remove fatos contraditórios;
- junta informações duplicadas;
- transforma datas relativas em datas reais;
- arquiva informações obsoletas;
- mantém apenas regras úteis;
- reduz ruído entre sessões.

Prompt prático:

```text
Revise os arquivos de memória deste projeto.

Tarefas:
1. Remova duplicatas.
2. Marque informações contraditórias.
3. Atualize datas relativas para datas absolutas.
4. Separe fatos atuais de históricos.
5. Gere um resumo das mudanças.
```

## 9. Definir orçamento de tarefa

Em agentes autônomos, custo e tempo podem sair do controle.

Por isso, o Nível 5 exige **task budgets**: limites para uma execução.

Exemplo:

```text
Execute esta análise com orçamento máximo de 80.000 tokens.
Priorize:
1. Segurança
2. Bugs críticos
3. Testes ausentes
4. Documentação apenas se sobrar orçamento
```

A ideia é fazer o agente se autorregular:

- pensar melhor no início;
- evitar loops;
- priorizar o mais importante;
- encerrar com resumo;
- não gastar indefinidamente.

## 10. Criar equipes de agentes

No Nível 5, você pode usar múltiplos agentes especializados coordenados por um agente líder.

Exemplo de equipe:

- agente líder;
- agente de segurança;
- agente de testes;
- agente de documentação;
- agente de UX;
- agente de performance;
- agente de arquitetura.

Diferente de subagentes simples, uma equipe pode compartilhar descobertas, dividir tarefas e comparar conclusões.

Exemplo prático:

```text
Monte uma equipe de agentes para revisar este novo módulo.

Papéis:
1. Arquiteto: avalia estrutura geral
2. Segurança: procura vulnerabilidades
3. Testes: verifica cobertura
4. UX: avalia fluxo do usuário
5. Documentação: confere clareza

O agente líder deve consolidar as conclusões e entregar um plano priorizado.
```

## 11. Descobrir e reaproveitar o que já existe

No Nível 5, a habilidade mais importante não é criar tudo do zero.

É saber encontrar e adaptar:

- skills existentes;
- MCP servers;
- templates;
- automações prontas;
- repositórios open-source;
- exemplos de agentes;
- integrações comunitárias.

A lógica é:

> Primeiro descubra se já existe algo parecido. Depois adapte ao seu contexto.

Isso economiza tempo e reduz erro.

## Como implementar o Nível 5 com segurança

O maior desafio do Nível 5 não é técnico.

É **confiança**.

Você não deve começar dando autonomia total para Claude em tarefas críticas.

Comece pequeno.

### Etapa 1 — Rotina de baixo risco

Exemplo:

```text
Todo dia às 8h, gere um resumo das tarefas pendentes e envie apenas para mim.
```

Características de uma boa primeira rotina:

- não envia nada para clientes;
- não altera arquivos importantes;
- não apaga nada;
- não faz deploy;
- apenas lê, resume e informa.

### Etapa 2 — Rotina com validação humana

Exemplo:

```text
Quando um pull request for aberto:
1. Revise o código.
2. Gere comentários sugeridos.
3. Não publique automaticamente.
4. Envie para minha aprovação.
```

Aqui Claude trabalha, mas você aprova antes.

### Etapa 3 — Ação automática limitada

Exemplo:

```text
Quando uma tarefa for concluída:
1. Atualize o status no quadro.
2. Envie resumo para o canal interno.
3. Não altere código.
4. Não envie mensagem externa.
```

### Etapa 4 — Autonomia maior

Somente depois de semanas de execução confiável, você libera ações mais fortes.

Exemplo:

```text
Se o PR alterar apenas documentação:
1. Revise automaticamente.
2. Rode checks.
3. Comente aprovação se tudo estiver correto.
```

## Exemplo prático completo: revisão automática de PR

### Objetivo

Claude revisar pull requests automaticamente.

### Gatilho

Novo PR aberto no GitHub.

### Fluxo

1. Claude recebe evento do PR.
2. Lê arquivos alterados.
3. Verifica riscos.
4. Roda checklist de revisão.
5. Gera comentários.
6. Envia para aprovação humana ou publica conforme regra.
7. Registra resumo.

### Regras de segurança

```text
Regras:
1. Nunca aprove PRs automaticamente se houver alteração em autenticação, pagamento ou permissões.
2. Nunca rode comandos destrutivos.
3. Se detectar segredo, token ou credencial, pare e avise imediatamente.
4. Se houver mudança em banco de dados, peça revisão humana.
5. Se os testes falharem, não aprove.
```

## Exemplo prático completo: briefing automático de reunião

### Objetivo

Preparar briefing antes de reuniões.

### Gatilho

Nova reunião no calendário ou reunião do dia seguinte.

### Fluxo

1. Claude identifica participantes.
2. Busca documentos relacionados.
3. Resume histórico.
4. Lista pendências.
5. Sugere perguntas.
6. Gera um briefing.
7. Envia para você antes da reunião.

### Prompt da rotina

```text
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
```

## Exemplo prático completo: relatório semanal autônomo

### Objetivo

Gerar relatório semanal sem intervenção manual.

### Gatilho

Toda sexta-feira às 16h.

### Fluxo

1. Verificar tarefas concluídas.
2. Verificar pendências.
3. Agrupar por projeto.
4. Destacar riscos.
5. Gerar relatório.
6. Enviar para revisão.

### Prompt da rotina

```text
Toda sexta-feira às 16h, gere um relatório semanal.

Formato:
1. Resumo executivo
2. Entregas da semana
3. Pendências
4. Riscos
5. Próximas ações
6. Itens que precisam da minha decisão

Não envie para clientes. Envie apenas para mim.
```

## Checklist de segurança do Nível 5

Antes de colocar uma rotina autônoma para rodar, confirme:

- qual é o gatilho;
- qual é o escopo;
- quais dados ela pode acessar;
- quais ações ela pode executar;
- quais ações são proibidas;
- quando deve pedir aprovação humana;
- como você será notificado;
- onde os logs serão salvos;
- como interromper a rotina;
- como revisar o histórico;
- qual é o orçamento de tokens;
- qual é o plano em caso de erro.

## Regras práticas para automações autônomas

```text
Regras gerais:
1. Nunca apague arquivos sem aprovação humana.
2. Nunca envie mensagens externas sem aprovação humana.
3. Nunca faça deploy sem confirmação explícita.
4. Nunca aprove mudanças críticas automaticamente.
5. Sempre registre o que foi feito.
6. Sempre avise quando encontrar erro.
7. Sempre pare em caso de dúvida.
8. Sempre respeite o escopo definido.
```

## Onde o Nível 5 gera mais valor

O Nível 5 é especialmente útil para:

- equipes técnicas;
- agências;
- freelancers avançados;
- empresas com muitos processos repetitivos;
- times que recebem muitos PRs;
- negócios com relatórios recorrentes;
- operações com atendimento e documentos;
- projetos que precisam de monitoramento constante.

## O que vender no Nível 5

Se você trabalha com serviços, o Nível 5 permite vender soluções mais estratégicas.

Exemplos:

- revisão automática de PRs;
- agente de relatório semanal;
- agente de briefing de reuniões;
- monitor de tarefas pendentes;
- auditor de dependências;
- triagem automática de tickets;
- agente de documentação;
- automação de onboarding;
- agente de análise de documentos;
- sistema de alertas inteligentes.

Aqui você não vende “prompt”.

Você vende **infraestrutura de trabalho**.

## Erros comuns no Nível 5

1. Dar autonomia demais cedo demais.
2. Não ter logs.
3. Não ter botão de parada.
4. Não separar ambientes.
5. Não definir limites.
6. Confiar sem observar.
7. Automatizar processos ruins.

## Como saber que você domina o Nível 5

Você está no Nível 5 quando:

- tem rotinas que rodam sem você iniciar manualmente;
- Claude reage a eventos;
- existem hooks de segurança;
- tarefas têm logs e notificações;
- você usa canais externos para acionar ou acompanhar;
- agentes têm escopo claro;
- existem limites de orçamento;
- você começa com baixo risco e aumenta autonomia aos poucos;
- Claude trabalha mesmo quando você não está presente;
- você pensa em sistemas, não em conversas.

## Resultado esperado

No Nível 5, você ganha:

- automação contínua;
- redução de tarefas repetitivas;
- monitoramento ativo;
- respostas mais rápidas a eventos;
- revisão técnica constante;
- relatórios automáticos;
- operação mais escalável;
- menos dependência da sua presença;
- capacidade de criar produtos e serviços mais avançados.

Esse é o nível em que Claude passa a ser uma camada de infraestrutura dentro do trabalho.

## Plano prático de 7 dias para começar o Nível 5

### Dia 1 — Escolha uma rotina simples

Escolha algo de baixo risco.

Exemplo:

```text
Resumo diário das tarefas pendentes.
```

### Dia 2 — Defina escopo

Escreva:

- o que pode ler;
- o que pode fazer;
- o que não pode fazer;
- quando deve parar.

### Dia 3 — Crie o formato de saída

Defina um modelo fixo.

Exemplo:

```text
1. Resumo do dia
2. Pendências
3. Riscos
4. Ações recomendadas
```

### Dia 4 — Adicione notificação

Escolha onde receber:

- e-mail;
- Slack;
- Telegram;
- arquivo;
- painel.

### Dia 5 — Rode manualmente

Antes de automatizar, execute como teste.

### Dia 6 — Agende com supervisão

Faça rodar automaticamente, mas sem enviar para terceiros.

### Dia 7 — Revise logs

Veja:

- acertou?
- exagerou?
- esqueceu algo?
- inventou algo?
- precisa de regra nova?

Depois disso, ajuste e repita por algumas semanas.

## Prompt-base para criar uma rotina Nível 5

```text
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
```

## Resumo do Nível 5

O Nível 5 é o estágio em que Claude deixa de ser “algo que você usa” e passa a ser “algo que opera”.

Ele pode:

- rodar na nuvem;
- responder a eventos;
- acionar fluxos;
- revisar código;
- gerar relatórios;
- preparar reuniões;
- enviar alertas;
- coordenar agentes;
- funcionar como infraestrutura.

Mas o avanço deve ser gradual.

Primeiro leitura.  
Depois rascunho.  
Depois ação com aprovação.  
Só então autonomia controlada.

O objetivo não é deixar a IA solta.

O objetivo é construir um sistema confiável, com regras, limites, logs e supervisão.
