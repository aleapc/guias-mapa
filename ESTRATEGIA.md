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

## Estado (2026-08-19) — os DOIS mapas reconstruídos com a grade completa

- **Mapa dos cursos** `aleapc.github.io/kit-de-bordo-mapa`: colunas-destino
  novas plotadas — EUA/Reino Unido/Tailândia já existiam no grid e foram
  marcadas ✎ "curso a criar"; **Holanda** adicionada como coluna. Objetivo
  remarcado no topo ("a grade completa, nos dois eixos"). Inglês-destino ≈ 50 M
  de compradores não-anglófonos (a maior coluna intocada).
- **Mapa de cidades** `aleapc.github.io/guias-mapa`: 201 destinos, 17
  países/regiões, 3 faixas (curso no ar / curso a criar / guia-only).

### Corredores origem→destino dos destinos novos (pesquisados 2026-08-19)
- **EUA** (não-anglófonos, ≈30 M): México 17,0 (ES) · Alemanha 2,0 · Brasil
  1,9 · Japão 1,8 · França 1,7 · Coreia 1,7 · China 1,6 · Itália 1,1 · Espanha
  0,9 · Holanda 0,6. Anglófonos (não compram): Canadá 20,2 · UK 4,0 · Austrália 1,0.
- **Reino Unido** (não-anglófonos, ≈15 M): França 3,6 · Alemanha 3,3 · Espanha
  2,5 · Holanda 2,1 · Itália 1,9 · China 0,6.
- **Holanda** (≈15 M): Alemanha 7,5 · Bélgica 2,7 · EUA 2,2 · UK 2,0 · França 1,4.
  Ressalva: holandeses/mercado têm altíssima proficiência em inglês.
- **Tailândia** (≈16 M em línguas-curso): China 6,7 · Coreia 1,8 · Rússia 1,75 ·
  Japão 1,1 · EUA+UK 2,0 · Alemanha 0,9 · França 0,85. (Malásia 5,0 e Índia 2,1
  fora das línguas-curso.)
- **Irlanda/Austrália/Canadá-anglófono**: ~2 M cada, caudas pequenas —
  colunas menores, não plotadas individualmente no grid (só na prosa).
- **Canadá francófono** (Montréal/Québec): entra no curso de FRANCÊS (já no ar).
