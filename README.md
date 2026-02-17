# Humanizer

Uma skill para Claude Code que remove sinais de escrita gerada por IA, deixando o texto mais natural e humano. Adaptada para português brasileiro.

## Instalação

### Recomendado (clonar direto na pasta de skills do Claude Code)

```bash
mkdir -p ~/.claude/skills
git clone https://github.com/rpiochi/humanizer-pt-br.git ~/.claude/skills/humanizer
```

### Instalação manual (somente o arquivo da skill)

Se você já clonou este repositório (ou baixou o `SKILL.md`), copie o arquivo para a pasta de skills do Claude Code:

```bash
mkdir -p ~/.claude/skills/humanizer-pt-br
cp SKILL.md ~/.claude/skills/humanizer-pt-br/
```

## Uso

No Claude Code, invoque a skill:

```
/humanizer-pt-br

[cole seu texto aqui]
```

Ou peça diretamente:

```
Humanize este texto: [seu texto]
```

## Visão geral

Baseada no guia ["Signs of AI writing" da Wikipedia](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing), mantido pelo WikiProject AI Cleanup, com adaptações específicas para vícios de IA em português brasileiro.

### Insight principal (Wikipedia)

> "LLMs usam algoritmos estatísticos para adivinhar o que vem a seguir. O resultado tende ao resultado estatisticamente mais provável, que se aplica ao maior número de casos."

## 27 padrões detectados (com exemplos antes/depois)

### Padrões de conteúdo

| # | Padrão | Antes | Depois |
|---|--------|-------|--------|
| 1 | **Inflação de importância** | "representando um marco fundamental..." | "foi criado em 1934 para centralizar..." |
| 2 | **Notoriedade sem contexto** | "destaque na Folha, BBC, Valor..." | "em entrevista à Folha em 2024..." |
| 3 | **Gerundismo superficial** | "simbolizando... refletindo... evidenciando..." | Cortar ou trocar por fonte concreta |
| 4 | **Linguagem promocional** | "encravada no coração da deslumbrante..." | "é uma cidade na Chapada Diamantina" |
| 5 | **Atribuição vaga** | "especialistas acreditam..." | "segundo levantamento da Embrapa de 2021..." |
| 6 | **Desafios formulaicos** | "apesar dos desafios... continua prosperando" | Dados objetivos sobre problemas reais |

### Padrões de linguagem

| # | Padrão | Antes | Depois |
|---|--------|-------|--------|
| 7 | **Vocabulário de IA** | "Ademais... cenário... evidenciando..." | "também... continuam comuns" |
| 8 | **Evitar ser/estar** | "funciona como... conta com..." | "é... tem..." |
| 9 | **Paralelismo negativo** | "não se trata apenas de X, mas de Y" | Dizer o ponto diretamente |
| 10 | **Regra de três** | "inovação, inspiração e insights" | Número natural de itens |
| 11 | **Troca de sinônimos** | "protagonista... personagem... heroína" | Repetir o termo mais claro |
| 12 | **Falsas escalas** | "do Big Bang à teia cósmica..." | Listar tópicos diretamente |
| 13 | **Conectivos em excesso** ★ | "Nesse sentido... Dessa forma... Diante disso..." | Conectar frases naturalmente |

### Padrões de estilo

| # | Padrão | Antes | Depois |
|---|--------|-------|--------|
| 14 | **Excesso de travessão** | "instituições — não pessoas —" | Usar vírgulas ou ponto |
| 15 | **Excesso de negrito** | "**OKRs**, **KPIs**" | "OKRs, KPIs" |
| 16 | **Lista com rótulos** | "**Segurança:** ..." | Converter para prosa |
| 17 | **Title Case em títulos** | "Negociações Estratégicas E..." | "Negociações estratégicas e..." |
| 18 | **Emojis** | "🚀 Fase de lançamento" | Remover emojis |
| 19 | **Aspas tipográficas** | `“projeto”` | `"projeto"` |
| 20 | **Anglicismos desnecessários** ★ | "mindset dos stakeholders" | "mentalidade das partes envolvidas" |

### Padrões de comunicação

| # | Padrão | Antes | Depois |
|---|--------|-------|--------|
| 21 | **Artefatos de chatbot** | "Espero que isso ajude!" | Remover completamente |
| 22 | **Aviso de corte** | "até minha última atualização..." | Buscar fonte ou remover |
| 23 | **Tom bajulador** | "Excelente pergunta!" | Responder direto |

### Enchimento e hedging

| # | Padrão | Antes | Depois |
|---|--------|-------|--------|
| 24 | **Frases de enchimento** | "Com o intuito de", "Faz-se necessário pontuar" | "Para", (remover) |
| 25 | **Hedging excessivo** | "poderia potencialmente talvez" | "pode" |
| 26 | **Conclusões genéricas** | "o futuro é promissor" | Plano ou fato específico |
| 27 | **Encerramento motivacional** ★ | "Em um cenário cada vez mais..." | Dados concretos ou tendências reais |

★ = Padrão específico do português brasileiro, sem equivalente no original em inglês.

## Exemplo completo

**Antes (com cara de IA):**
> A nova atualização do software se apresenta como um testemunho do compromisso da empresa com a inovação. Ademais, oferece uma experiência fluida, intuitiva e poderosa — garantindo que os usuários possam atingir seus objetivos. Não se trata apenas de uma atualização, mas de uma revolução na forma como pensamos produtividade. Especialistas acreditam que isso terá impacto duradouro, evidenciando o papel estratégico da empresa no cenário tecnológico em constante evolução.

**Depois (humanizado):**
> A atualização do software trouxe processamento em lote, atalhos de teclado e modo offline. O feedback inicial dos testadores beta foi positivo — a maioria relatou que conclui tarefas mais rápido.

## O que muda em relação ao original em inglês?

Esta adaptação adiciona **3 padrões específicos do português brasileiro** (marcados com ★) que não existem na versão original:

- **Padrão 13 — Conectivos em excesso:** A IA em português abusa de conectivos formais ("Nesse sentido", "Dessa forma", "Diante disso") herdados da cultura de redação escolar e concurso público.
- **Padrão 20 — Anglicismos desnecessários:** A IA mistura inglês em excesso em textos de negócios ("stakeholders", "mindset", "approach") mesmo quando há equivalentes naturais em português.
- **Padrão 27 — Encerramentos motivacionais:** A IA em português tem tendência forte a fechar textos com fórmulas motivacionais vagas ("Em um cenário cada vez mais...", "O potencial é imenso...").

Todos os exemplos usam contextos brasileiros (IBGE, Chapada Diamantina, Embrapa, Pantanal).

## Referências

- [Wikipedia: Signs of AI writing](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing) — Fonte principal
- [WikiProject AI Cleanup](https://en.wikipedia.org/wiki/Wikipedia:WikiProject_AI_Cleanup) — Organização mantenedora

## Histórico de versão

- **1.0.0** — Versão inicial | Tradução da versão 2.1.0 original

## Licença

MIT
