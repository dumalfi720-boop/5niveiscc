# Os 5 Níveis do Claude Code

Curso completo em PT-BR cobrindo os 5 níveis de domínio do Claude — do Entusiasta ao Arquiteto — com cheat codes entre cada nível e uma prova final de 50 questões.

Formato visual: **INEMA.CLUB** (dark-first, responsivo, light mode obrigatório, tailwindcss via CDN, sem build).

## Estrutura

```
index.html                    # Capa + diagnóstico de 10 perguntas + cards das 6 trilhas
assets/capa.png               # Imagem da capa
curso/
├── trilha1/  (Emerald)       # Nível 1 — Entusiasta
│   ├── index.html
│   ├── modulo-1-1.html       # Dominando o básico
│   └── modulo-1-2.html       # Cheat Code: primeiro Projeto
├── trilha2/  (Blue)          # Nível 2 — Iniciante
│   ├── index.html
│   ├── modulo-2-1.html       # Projetos, Memória, Conectores
│   └── modulo-2-2.html       # Cheat Code: parar de copiar e colar
├── trilha3/  (Purple)        # Nível 3 — Intermediário
│   ├── index.html
│   ├── modulo-3-1.html       # Co-work: Claude na sua máquina
│   ├── modulo-3-2.html       # Estrutura de pastas
│   └── modulo-3-3.html       # Cheat Code: automação como serviço
├── trilha4/  (Amber)         # Nível 4 — Avançado
│   ├── index.html
│   ├── modulo-4-1.html       # Claude Code: o motor
│   ├── modulo-4-2.html       # Movimentos de alto impacto
│   └── modulo-4-3.html       # Cheat Code: parar de babar Claude
├── trilha5/  (Teal)          # Nível 5 — Arquiteto
│   ├── index.html
│   ├── modulo-5-1.html       # Claude como infraestrutura
│   ├── modulo-5-2.html       # Autônomos com responsabilidade
│   └── modulo-5-3.html       # O que vender + descobrir
└── trilha6/  (Rose)          # Prova Final
    ├── index.html            # Briefing da prova
    └── modulo-6-1.html       # 50 questões interativas + gabarito comentado
```

## Como abrir

Abra `index.html` no navegador. Sem build, sem servidor, sem dependências.

## Conteúdo

- **20 páginas HTML** (1 landing + 6 trilhas + 13 módulos)
- **80+ tópicos** com 3 seções cada (O que é / Por que aprender / Conceitos-chave)
- **Diagnóstico inicial** (10 perguntas) que aponta a trilha de entrada
- **Prova final** (50 questões, 10 por nível) com gabarito comentado e link pra módulo da resposta errada

## Base

- "Every Level of Claude Explained" (transcript em `/doc/resumo.txt`)
- Versões PT-BR em `/doc/nivel_*.md`
- Validação web (Maio/2026): Code w/ Claude, hooks, routines, dreaming, outcomes
- Design system [INEMA.CLUB](https://inema.club)
