# Nível 3 — Intermediário

O **Nível 3** começa quando Claude deixa de ser apenas um ambiente de conversa e passa a **executar tarefas práticas no computador**, com acesso controlado a arquivos, pastas, skills e rotinas.

É o ponto em que você começa a pensar menos em “me dê uma resposta” e mais em:

> “Claude, faça esse trabalho para mim.”

## O que caracteriza o Nível 3

No Nível 1, Claude responde perguntas.

No Nível 2, Claude trabalha com projetos, memória e documentos.

No **Nível 3**, Claude começa a atuar como um **colega operacional**, capaz de organizar arquivos, executar fluxos, aplicar modelos, gerar entregáveis e repetir processos com menos supervisão.

Exemplo simples:

Você não pede apenas:

> “Como eu organizo essa pasta?”

Você pede:

> “Organize essa pasta por tipo de arquivo, renomeie os documentos seguindo este padrão e gere um resumo do que encontrou.”

## A grande mudança do Nível 3

A mudança principal é sair de:

> “Claude, me diga o que fazer.”

Para:

> “Claude, vá lá e faça.”

Isso muda completamente o valor da ferramenta, porque ela passa a economizar não só tempo de pensamento, mas também **tempo de execução**.

## Para que serve na prática

### 1. Organizar arquivos e pastas

Uma das aplicações mais úteis do Nível 3 é deixar Claude trabalhar com arquivos reais.

Exemplos práticos:

- “Analise esta pasta de PDFs e separe por assunto.”
- “Renomeie os arquivos usando o padrão: data_cliente_tipo.”
- “Crie uma pasta para cada cliente e mova os arquivos correspondentes.”
- “Leia os documentos e gere um índice com resumo de cada um.”
- “Encontre arquivos duplicados ou mal nomeados.”

Uso real: você transforma uma pasta bagunçada em uma estrutura organizada.

### 2. Processar documentos

Claude pode ajudar a analisar, resumir, converter e reorganizar documentos.

Exemplos:

- “Leia todos os PDFs desta pasta e gere um resumo executivo.”
- “Extraia as principais decisões desses documentos.”
- “Transforme esses textos em um relatório.”
- “Compare estes dois documentos e destaque diferenças.”
- “Crie uma versão final mais clara e profissional.”

Uso real: você delega leitura, triagem e organização de informação.

### 3. Criar entregáveis a partir de arquivos

No Nível 3, Claude pode produzir arquivos mais completos com base em materiais existentes.

Exemplos:

- “Com base nesses PDFs, crie uma apresentação de 10 slides.”
- “Transforme essas anotações em um documento formal.”
- “Monte uma planilha com os dados encontrados nesses arquivos.”
- “Crie um resumo em Markdown com links para os arquivos originais.”
- “Gere uma proposta comercial usando este briefing e este modelo.”

Uso real: Claude pega materiais brutos e transforma em algo utilizável.

### 4. Usar skills reutilizáveis

Skills são instruções ou fluxos padronizados que Claude pode repetir.

Pense em skills como “receitas de trabalho”.

Exemplos de skills:

- relatório semanal;
- análise de contrato;
- resumo de reunião;
- revisão de proposta;
- criação de apresentação;
- análise de planilha;
- organização de pasta;
- geração de roteiro;
- checklist de entrega.

A vantagem é que você não precisa explicar o processo completo toda vez.

Você pode dizer:

- “Use a skill de relatório semanal para gerar o relatório desta pasta.”
- “Use o fluxo de proposta comercial com esses arquivos.”

## Exemplo prático de skill simples

Uma skill pode dizer:

```text
Quando eu pedir um relatório semanal:

1. Leia os arquivos da pasta indicada.
2. Separe informações por cliente.
3. Liste atividades realizadas.
4. Liste pendências.
5. Destaque riscos.
6. Gere um resumo executivo.
7. Salve o resultado na pasta de saída.
```

Depois, em vez de explicar tudo, você só pede:

> “Gere o relatório semanal da pasta Projeto X.”

### 5. Automatizar tarefas recorrentes

No Nível 3, você começa a agendar ou repetir tarefas com menos esforço.

Exemplos:

- “Todo dia às 8h, gere um resumo das tarefas de hoje.”
- “Toda sexta, prepare um relatório semanal.”
- “Toda segunda, revise a pasta de clientes e me diga o que está pendente.”
- “Uma vez por mês, organize os arquivos novos da pasta de downloads.”

Essas rotinas ainda podem depender do computador ligado e do aplicativo aberto, mas já representam um salto enorme.

### 6. Controlar tarefas pelo celular

Com recursos de controle remoto ou mobile, você pode acionar tarefas mesmo longe do computador.

Exemplos:

- “Estou no celular. Peça para Claude organizar os arquivos do projeto.”
- “Dispare a rotina de resumo semanal.”
- “Peça para preparar o material da reunião de amanhã.”

Uso real: você envia o comando pelo celular e Claude trabalha no desktop.

### 7. Usar Claude Design

Neste nível, Claude também começa a ajudar em tarefas visuais e de produto.

Você pode pedir:

- “Crie um protótipo de landing page para esse serviço.”
- “Monte um design de apresentação com base nesta identidade visual.”
- “Crie um one-page para explicar esta oferta.”
- “Desenhe a estrutura de uma página de captura.”
- “Crie um layout inicial para um dashboard.”

A diferença é que Claude não só escreve o conteúdo, mas ajuda a montar a estrutura visual e o fluxo.

### 8. Usar Computer Use

Quando uma ferramenta não tem conector direto, Claude pode interagir visualmente com ela, como uma pessoa.

Exemplos:

- clicar em botões;
- preencher formulários;
- navegar em telas;
- copiar informações;
- enviar comandos;
- alternar abas.

Uso prático:

> “Abra essa aplicação, entre na tela de relatórios, baixe o arquivo mais recente e salve na pasta do projeto.”

Esse é um grande salto, porque Claude começa a operar interfaces.

## Como configurar bem o Nível 3

O segredo do Nível 3 é dar estrutura para Claude trabalhar com segurança.

Você precisa criar uma organização clara.

### Estrutura recomendada de pastas

```text
/Claude_Workspace
  /00_sobre_mim
  /01_templates
  /02_projetos
  /03_entradas
  /04_processando
  /05_outputs
  /06_arquivo
```

### O que colocar em cada pasta

#### `00_sobre_mim`

Informações fixas sobre você, seu negócio, seu estilo e suas preferências.

Exemplos:

- quem você é;
- o que faz;
- como prefere respostas;
- tipos de clientes;
- tom de voz;
- regras importantes.

#### `01_templates`

Modelos que Claude pode usar, mas não deve alterar.

Exemplos:

- modelo de proposta;
- modelo de relatório;
- modelo de apresentação;
- modelo de e-mail;
- modelo de contrato;
- identidade visual.

Regra importante:

> “Nunca edite arquivos da pasta templates. Apenas copie e use como base.”

#### `02_projetos`

Pastas separadas para cada projeto ou cliente.

```text
/02_projetos
  /cliente_A
  /cliente_B
  /conteudo
  /estudos
  /propostas
```

#### `03_entradas`

Arquivos brutos que Claude deve processar.

Exemplos:

- PDFs;
- transcrições;
- prints;
- planilhas;
- documentos;
- áudios transcritos.

#### `04_processando`

Área temporária para trabalho em andamento.

#### `05_outputs`

Onde Claude deve salvar entregáveis finais.

Exemplos:

- relatórios;
- apresentações;
- resumos;
- planilhas;
- documentos prontos;
- checklists.

#### `06_arquivo`

Materiais antigos ou finalizados.

## Instrução prática para Claude no Nível 3

```text
Antes de começar qualquer tarefa, leia primeiro a pasta 00_sobre_mim.

Regras:
1. Nunca edite arquivos da pasta 01_templates.
2. Quando precisar usar um template, faça uma cópia.
3. Use a pasta 03_entradas para arquivos brutos.
4. Use a pasta 04_processando para rascunhos.
5. Salve entregáveis finais em 05_outputs.
6. Ao terminar, gere um resumo do que foi feito.
7. Se houver risco de apagar, sobrescrever ou mover arquivos importantes, peça confirmação antes.
```

## Exemplos práticos de uso

### Exemplo 1: Organizar downloads

```text
Organize minha pasta de downloads.

Tarefas:
1. Separe arquivos por tipo: PDFs, imagens, planilhas, documentos e outros.
2. Renomeie arquivos quando o nome estiver confuso.
3. Não apague nada.
4. Crie um resumo com o que foi encontrado.
5. Salve o resumo em outputs.
```

### Exemplo 2: Relatório semanal

```text
Gere o relatório semanal do projeto Cliente A.

Use os arquivos da pasta do cliente.
Organize o relatório em:
1. Resumo executivo
2. Atividades realizadas
3. Pendências
4. Riscos
5. Próximos passos

Salve o resultado em outputs como relatório_semana_atual.md.
```

### Exemplo 3: Preparar reunião

```text
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
```

### Exemplo 4: Criar apresentação

```text
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
```

### Exemplo 5: Criar fluxo de atendimento

```text
Analise estes documentos e crie um fluxo de atendimento ao cliente.

Entregue:
1. Etapas do atendimento
2. Responsável por cada etapa
3. Mensagens padrão
4. Pontos de automação possíveis
5. Checklist operacional
```

## O que muda no seu trabalho

No Nível 3, você começa a delegar blocos inteiros de trabalho.

Antes:

Você lia arquivos, organizava dados, copiava trechos, montava documentos e salvava manualmente.

Agora:

Você define o resultado, dá acesso ao material e Claude executa boa parte do processo.

## Cuidados importantes

### 1. Dê permissões com cuidado

Claude só deve acessar pastas necessárias.

Evite dar acesso amplo demais sem necessidade.

Melhor:

> “Trabalhe apenas nesta pasta do projeto.”

Pior:

> “Use meu computador inteiro.”

### 2. Proteja templates

Templates devem ser somente leitura na prática.

Sempre diga:

> “Não edite os templates. Faça cópias.”

### 3. Nunca deixe apagar arquivos sem confirmação

Inclua sempre esta regra:

> “Não apague nada sem minha confirmação.”

### 4. Peça relatório final

Ao concluir, Claude deve dizer:

- o que fez;
- quais arquivos leu;
- quais arquivos criou;
- onde salvou;
- quais problemas encontrou;
- o que precisa de revisão humana.

### 5. Comece com tarefas de baixo risco

Não comece automatizando algo sensível.

Comece com:

- organizar cópias de arquivos;
- gerar resumos;
- criar rascunhos;
- montar checklists;
- comparar documentos;
- preparar materiais internos.

Depois avance para tarefas mais importantes.

## Como saber que você domina o Nível 3

Você está no Nível 3 quando:

- Claude consegue trabalhar com suas pastas;
- você usa skills para tarefas repetidas;
- você tem estrutura de entradas e outputs;
- você gera entregáveis com menos intervenção;
- você usa Claude para organizar arquivos;
- você agenda tarefas simples;
- você aciona trabalhos pelo desktop ou celular;
- você começa a pensar em processos, não apenas prompts.

## Resultado esperado

No Nível 3, você pode economizar **10 horas ou mais por semana**, principalmente em tarefas operacionais.

Você ganha:

- organização;
- execução;
- padronização;
- repetição de processos;
- geração de entregáveis;
- menos retrabalho;
- mais capacidade de atender clientes;
- base para vender automações simples.

## Limite do Nível 3

O limite é que ainda falta rigor técnico completo.

Claude pode executar tarefas, mas para sistemas mais complexos você ainda precisa de:

- controle de versão;
- revisão de código;
- ambientes isolados;
- testes;
- branches;
- subagentes especializados;
- validação mais robusta.

Quando você começa a precisar de engenharia real, múltiplas sessões paralelas e projetos técnicos mais sérios, entra no **Nível 4 — Avançado**, com Claude Code.
