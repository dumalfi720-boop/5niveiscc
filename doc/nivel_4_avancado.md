# Nível 4 — Avançado

O **Nível 4** começa quando Claude deixa de ser apenas um executor de tarefas e passa a funcionar como uma **equipe técnica coordenada**, especialmente usando **Claude Code**.

Aqui, o foco não é mais só pedir respostas, criar arquivos ou organizar pastas. O foco passa a ser construir, revisar, testar, versionar e melhorar sistemas reais.

> No Nível 3, Claude faz tarefas no computador.  
> No Nível 4, Claude trabalha como uma equipe técnica em projetos estruturados.

## O que caracteriza o Nível 4

O Nível 4 é marcado por:

- Claude Code;
- trabalho em projetos de software;
- controle de versão;
- planejamento antes da execução;
- múltiplas sessões em paralelo;
- subagentes especializados;
- testes e validação;
- comandos personalizados;
- melhoria contínua do contexto do projeto.

Aqui Claude deixa de ser “um assistente” e começa a parecer uma pequena equipe de engenharia.

## A grande mudança do Nível 4

A mudança principal é sair de:

> “Claude, execute esta tarefa.”

Para:

> “Claude, planeje, implemente, teste, valide e me entregue uma solução revisável.”

No Nível 3, você delega tarefas.  
No Nível 4, você delega **ciclos técnicos completos**.

## Para que serve na prática

### 1. Criar sistemas e ferramentas reais

Exemplos:

- dashboards;
- sites;
- landing pages;
- sistemas internos;
- automações com backend;
- integrações com APIs;
- aplicativos simples;
- painéis administrativos;
- ferramentas para clientes;
- scripts robustos;
- extensões;
- protótipos funcionais.

Exemplo de pedido:

```text
Crie uma ferramenta interna para controlar propostas comerciais.

Preciso de:
1. Cadastro de clientes
2. Status da proposta
3. Valor estimado
4. Próxima ação
5. Filtro por etapa
6. Exportação em CSV

Antes de implementar, analise a estrutura do projeto e me apresente um plano.
```

### 2. Trabalhar com planejamento antes da execução

Um erro comum é pedir para Claude sair codando imediatamente.

No Nível 4, você usa **modo de planejamento**.

A lógica é:

1. Claude analisa o projeto.
2. Identifica arquivos relevantes.
3. Propõe um plano.
4. Faz perguntas se necessário.
5. Você aprova.
6. Só então ele executa.

Prompt prático:

```text
Antes de alterar qualquer arquivo, entre em modo planejamento.

Analise o projeto e me entregue:
1. O que precisa ser feito
2. Quais arquivos serão alterados
3. Riscos
4. Perguntas importantes
5. Plano passo a passo

Não implemente nada até eu aprovar.
```

Isso reduz erros, alterações desnecessárias e retrabalho.

## 3. Usar o arquivo `claude.md`

O `claude.md` é um dos elementos mais importantes do Nível 4.

Ele funciona como um **manual do projeto** que Claude lê no início de cada sessão.

### O que colocar no `claude.md`

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
```

### Regra prática

Mantenha o `claude.md` curto.

Idealmente:

- claro;
- objetivo;
- atualizado;
- com menos de 200 linhas;
- sem excesso de detalhes.

Se tiver informações longas, coloque em arquivos separados, por exemplo:

```text
/docs/regras-de-negocio.md
/docs/design-system.md
/docs/api.md
```

E no `claude.md`, apenas referencie:

```markdown
Para regras de negócio detalhadas, consulte @docs/regras-de-negocio.md.
```

## 4. Atualizar o `claude.md` quando Claude errar

Sempre que Claude cometer um erro repetível, peça:

```text
Atualize o claude.md com uma regra para evitar esse erro no futuro.
```

Exemplo:

```text
Você criou este componente na pasta errada.

Atualize o claude.md dizendo que componentes reutilizáveis devem ficar em /src/components e páginas completas devem ficar em /src/pages.
```

Com o tempo, o projeto fica mais inteligente e Claude erra menos.

## 5. Usar subagentes especializados

Subagentes são como especialistas dentro da equipe.

Você pode ter agentes para:

- testes;
- segurança;
- documentação;
- revisão de código;
- UX;
- performance;
- acessibilidade;
- arquitetura;
- banco de dados;
- integração com APIs.

Exemplo prático:

```text
Use um subagente de revisão de código para analisar esta implementação.

Ele deve verificar:
1. Bugs prováveis
2. Problemas de segurança
3. Código duplicado
4. Falhas de performance
5. Pontos que precisam de testes
```

Outro exemplo:

```text
Use um subagente de documentação para criar uma explicação clara de como este módulo funciona.
```

## 6. Trabalhar com sessões paralelas

No Nível 4, você pode ter várias sessões de Claude trabalhando ao mesmo tempo, cada uma em uma tarefa isolada.

Exemplo:

- sessão 1: cria nova feature;
- sessão 2: corrige bug;
- sessão 3: escreve testes;
- sessão 4: melhora documentação;
- sessão 5: revisa segurança.

Isso aumenta muito a produtividade, mas exige organização.

## 7. Usar worktrees

Worktrees permitem que cada sessão trabalhe em um espaço isolado, sem sobrescrever arquivos de outra sessão.

Exemplo:

```text
claude-worktree nova-feature-clientes
claude-worktree corrigir-bug-login
claude-worktree testes-dashboard
```

Com isso, você evita que duas sessões mexam nos mesmos arquivos ao mesmo tempo.

## 8. Usar branches com clareza

Exemplos de nomes:

```text
feature/dashboard-clientes
fix/login-error
docs/api-readme
test/propostas-flow
refactor/components-table
```

Prompt útil:

```text
Crie uma branch para esta tarefa com nome claro.
Implemente a mudança nela.
Ao terminar, gere um resumo para pull request.
```

## 9. Criar pull requests melhores

Peça para Claude gerar:

- resumo da mudança;
- arquivos alterados;
- motivo da alteração;
- riscos;
- como testar;
- screenshots, se aplicável;
- próximos passos.

Modelo prático:

```text
Prepare a descrição do pull request com:

1. Resumo
2. O que foi alterado
3. Por que foi alterado
4. Como testar
5. Riscos conhecidos
6. Checklist final
```

## 10. Usar loop de verificação

O **loop de verificação** é essencial.

Não basta Claude dizer que terminou. Ele precisa testar.

Peça sempre:

```text
Antes de me entregar, verifique seu próprio trabalho.

Rode os testes disponíveis.
Se for interface, abra no navegador, confira visualmente e tire screenshots.
Se encontrar erro, corrija e teste novamente.
Só me entregue quando passar na validação.
```

Exemplo:

```text
Implemente a tela de cadastro de clientes.

Depois:
1. Rode lint
2. Rode testes
3. Abra a aplicação
4. Teste o fluxo manualmente
5. Verifique se não quebrou a tela de propostas
6. Gere um resumo final com evidências
```

## 11. Usar comandos personalizados

Se você repete um prompt mais de duas vezes, transforme em comando.

Exemplos:

```text
/revisar-codigo
/criar-pr
/gerar-testes
/documentar-modulo
/verificar-seguranca
/commit-push-pr
```

Exemplo de comando `/criar-pr`:

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
```

## 12. Usar `/compact` para controlar contexto

Sessões longas ficam pesadas.

Use antes de o contexto ficar cheio.

Exemplo:

```text
Compacte o histórico mantendo:
1. Objetivo do projeto
2. Decisões tomadas
3. Arquivos alterados
4. Pendências
5. Regras importantes
```

## 13. Usar `/context`

Use quando a sessão parecer pesada ou confusa.

```text
Mostre onde o contexto está sendo consumido e sugira o que pode ser compactado ou movido para documentação.
```

## 14. Usar `/rewind` quando a tentativa deu errado

Quando Claude entra por um caminho ruim, volte ao ponto anterior em vez de corrigir infinitamente dentro do mesmo contexto.

## 15. Usar `/branch` para testar alternativas

```text
Crie uma branch para testar uma solução simples.
Depois criaremos outra branch para testar uma solução mais robusta.
```

## 16. Usar `/btw` para perguntas paralelas

```text
/btw O que esta função faz?
```

Assim você tira uma dúvida sem mudar a direção da tarefa principal.

## 17. Usar output styles

Você pode adaptar o estilo de resposta conforme a tarefa.

Exemplos:

- revisor de código;
- arquiteto técnico;
- professor;
- modo direto;
- documentador;
- analista de segurança.

Exemplo:

```text
Use um estilo de resposta como revisor técnico sênior: direto, crítico e focado em riscos.
```

## Processo ideal para uma tarefa no Nível 4

### Etapa 1 — Preparar contexto

```text
Leia o claude.md e os arquivos relevantes antes de responder.
```

### Etapa 2 — Planejar

```text
Antes de implementar, apresente o plano e espere minha aprovação.
```

### Etapa 3 — Implementar

```text
Implemente somente o que foi aprovado.
```

### Etapa 4 — Testar

```text
Rode testes, lint e verificações disponíveis.
```

### Etapa 5 — Revisar

```text
Revise seu próprio trabalho e corrija problemas encontrados.
```

### Etapa 6 — Documentar

```text
Atualize documentação se necessário.
```

### Etapa 7 — Entregar

```text
Entregue um resumo final com arquivos alterados, testes feitos e próximos passos.
```

## Prompt completo para Claude Code

```text
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
```

## Exemplos práticos de uso

### Exemplo 1: Criar uma feature

```text
Crie uma área de clientes no sistema.

Requisitos:
1. Listar clientes
2. Cadastrar novo cliente
3. Editar cliente existente
4. Filtrar por status
5. Salvar no banco atual

Antes de implementar, analise a arquitetura e proponha o plano.
```

### Exemplo 2: Corrigir bug

```text
Existe um erro no login quando o usuário tenta recuperar senha.

Investigue:
1. Onde o erro acontece
2. Qual arquivo está envolvido
3. Qual é a causa provável
4. Como corrigir com o menor impacto

Depois implemente a correção e rode os testes.
```

### Exemplo 3: Criar testes

```text
Crie testes para o fluxo de propostas.

Inclua:
1. Cadastro de proposta
2. Alteração de status
3. Validação de campos obrigatórios
4. Filtro por cliente

Não altere a lógica principal sem justificar.
```

### Exemplo 4: Revisão de segurança

```text
Revise este módulo como especialista em segurança.

Verifique:
1. Dados sensíveis expostos
2. Falta de validação
3. Riscos de permissão
4. Dependências perigosas
5. Logs indevidos

Entregue recomendações priorizadas por risco.
```

### Exemplo 5: Refatoração

```text
Refatore este componente sem alterar o comportamento.

Objetivos:
1. Reduzir repetição
2. Melhorar nomes
3. Separar responsabilidades
4. Manter compatibilidade
5. Garantir que os testes continuem passando
```

## Checklist antes de deixar Claude alterar código

Antes de aprovar uma tarefa, confira:

- Claude leu o `claude.md`;
- ele entendeu o objetivo;
- apresentou plano;
- listou arquivos que vai alterar;
- explicou riscos;
- criou branch ou worktree;
- sabe como testar;
- não vai mexer fora do escopo;
- não vai adicionar dependências sem permissão;
- vai entregar resumo final.

## Como isso ajuda em trabalho com clientes

No Nível 4, você já consegue entregar trabalhos de valor maior, porque sai do campo de “automação simples” e entra em **sistemas completos**.

Exemplos de entregas vendáveis:

- sistema interno para controle de atendimento;
- painel de indicadores;
- automação com API;
- portal simples para cliente;
- dashboard de vendas;
- integração entre ferramentas;
- chatbot com base de conhecimento;
- protótipo funcional;
- melhoria de sistema existente;
- revisão técnica de projeto.

## Erros comuns no Nível 4

1. Deixar Claude codar sem plano.
2. Usar uma sessão longa demais.
3. Não testar.
4. Misturar muitas tarefas.
5. Não usar controle de versão.
6. Não documentar decisões.
7. Não atualizar o `claude.md`.

## Como saber que você domina o Nível 4

Você está no Nível 4 quando:

- usa Claude Code com projetos reais;
- tem `claude.md` nos projetos;
- pede plano antes de execução;
- trabalha com branches ou worktrees;
- usa subagentes para revisão, testes e documentação;
- roda validações antes de aceitar entregas;
- cria comandos personalizados;
- consegue trabalhar com várias sessões em paralelo;
- gera PRs bem descritos;
- mantém documentação do projeto atualizada;
- usa Claude como uma equipe técnica, não apenas como assistente.

## Resultado esperado

No Nível 4, você ganha:

- velocidade de desenvolvimento;
- qualidade técnica;
- entregas mais completas;
- capacidade de trabalhar em paralelo;
- redução de retrabalho;
- documentação melhor;
- revisão mais estruturada;
- projetos vendáveis de maior valor.

A promessa deste nível é sair de pequenas tarefas e começar a construir **sistemas reais**.

## Limite do Nível 4

O limite do Nível 4 é que você ainda coordena tudo manualmente.

Você precisa:

- iniciar sessões;
- aprovar etapas;
- revisar resultados;
- disparar comandos;
- monitorar PRs;
- pedir auditorias;
- acompanhar tarefas recorrentes.

Quando você percebe que está repetindo sempre os mesmos ciclos técnicos, chega o momento de avançar para o **Nível 5 — Arquiteto**, onde entram rotinas na nuvem, hooks, agentes autônomos e automações que rodam mesmo quando você não está presente.
