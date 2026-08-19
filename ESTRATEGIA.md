# Estratégia — Cursos de línguas + Guias de cidade (Journeyo)

Remarcação dos objetivos em 2026-08-19, depois de perceber que o alvo é a
**grade inteira origem×destino** (o turista nos dois eixos), não só os destinos
que já tinham arte/áudio prontos.

## O alvo

Todo turista em viagem é um par **(origem, língua dele) → (destino, cidade)**.
Para cada um, dois apps a baixar:
- o **curso de língua** do destino (survival da língua de lá, na língua dele);
- o **guia** da cidade específica.

Objetivo unificado: **dominar o preparo pré-viagem** desse turista — cobrir a
grade origem×destino nos cursos e o ranking de cidades nos guias, com
cross-sell bidirecional entre os dois (link no app de curso → guia; link no
guia → app de curso).

## Objetivo 1 — Cursos de línguas (preencher a grade)

- **Linhas = origem** (mercado comprador): EN, DE, FR, IT, NL, ES, ZH, KO, RU,
  PT-BR, JA...
- **Colunas = destino** (a língua que se aprende): FR, ES, TR, IT, DE, JA, EL,
  PT, + **as novas** → **inglês** (US/UK/IE/AU/CA), **neerlandês** (NL),
  **tailandês** (TH).
- **Inglês-destino é a maior alavanca nova:** o maior fluxo receptivo do mundo,
  comprado pelos **não-anglófonos** (ZH→US, DE→UK, KO→US, PT-BR→US...). Reusa
  TODAS as linhas-origem já construídas — é o espelho do que já se faz.
- **Regra de reúso (já provada):** aberta a coluna-destino (áudio-alvo), cada
  linha-origem entra a custo quase zero (a "camada-alvo").
- **Prioridade:** por volume do corredor origem→destino. Abrir inglês-destino
  provavelmente reordena o topo do catálogo inteiro.

## Objetivo 2 — Guias de cidade (cobrir os destinos, com ou sem curso)

- **Um guia por cidade turística relevante do mundo**, priorizado por chegadas
  internacionais — não só cidades de países com curso.
- **Produto autônomo:** vende a qualquer viajante. Onde há curso, cross-sell por
  link. Onde ainda não há (Londres, NYC, Amsterdam, Bangkok, Dubai...), o guia
  vende sozinho **e semeia** a demanda pra abrir aquela coluna de curso.
- Template: clonar `guia-malaga` (o mais evoluído). Ver [[guias-cidade-fork]] /
  `HANDOFF.md`.

## Destinos a adicionar aos dois mapas (decisão de 2026-08-19: "todos")

Marcar como **"curso a criar"** (distinto de "curso no ar"):
- **Bloco anglófono** — EUA, Reino Unido, Irlanda, Austrália, Canadá.
- **Holanda** — Amsterdam (vozes NL já existem no sistema).
- **Tailândia** — Bangkok (já existe o `guia-tailandia` PWA).
- **Guia-only (curso marginal, funcionam em inglês)** — Dubai, Abu Dhabi,
  Singapura, Hong Kong, Doha.

## Estado (2026-08-19)

- Mapa dos cursos: `aleapc.github.io/kit-de-bordo-mapa` (destinos atuais).
- Mapa de cidades: `aleapc.github.io/guias-mapa` (140 destinos, 9 países) —
  a expandir com os destinos novos acima.
- Próximo: pesquisa dos números das cidades novas → reconstruir os dois mapas
  com a grade completa.
