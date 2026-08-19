# HANDOFF — frente "Guias de cidade" (Roteiros de viagem)

Documento de retomada. Se você é uma sessão nova pegando esta frente, leia
isto + a memória `guias-cidade-fork` (em `~/.claude/projects/E--dev-d/memory/`,
se estiver no mesmo diretório de trabalho `E:\dev-d`).

## O que é esta frente

Construir **PWAs de guia turístico por cidade** (família `guia-*` que já existe:
Málaga, Puerto Varas, Peru, Uruguai, Tailândia), agora para as principais
cidades que **casam com os cursos de língua Journeyo** já no ar.

**Modelo de negócio:** NÃO é bundle. Dois produtos independentes, **cross-sell
por deep link de mão dupla** — no app de cursos, um link "conheça o guia de
[cidade]"; no guia, um link "aprenda a língua" apontando pro app Journeyo.

## O que já está pronto

- **Mapa de Cidades no ar:** https://aleapc.github.io/guias-mapa/ (este repo).
  140 destinos turísticos, 9 países, agrupado por país. Decide a ordem de
  construção dos guias — "guiar pelo mapa", como no mapa dos cursos.
- **Málaga já tem guia no ar** (`aleapc/guia-malaga`) — precedente/molde pronto.

## Disciplina do mapa (importante não estragar)

As métricas de turismo **variam por país e não são comparáveis entre países**:
Grécia = pax de aeroporto (~2× chegadas); Alemanha/Portugal = pernoites (inflam
3-5×); Itália = presenze; Japão = taxa-de-visita estimada; México = aeroporto
(Cancún = porta da Riviera Maya inteira). Os badges no mapa dizem a métrica de
cada número; a cor diz a confiança (firme / oficial-ressalvado / estimativa).
**Ordenar e priorizar DENTRO de cada país.** Região ≠ cidade (Paris =
Île-de-France; Palma/Ibiza = aeroporto da ilha; Algarve/Madeira = regiões).

Para o cross-sell, o que importa é o turista **estrangeiro** — destinos
dominados por doméstico (Oaxaca 95%, Guadalajara, Monterrey; interior do Japão)
pesam menos que o volume bruto.

## Próximo passo concreto

Abrir o **primeiro guia novo**. Recomendação pela lógica do mapa: **Istambul**
(dado firme, alto volume, curso Türkiye EN·DE·RU no ar, cidade densa que encaixa
no formato). Paris e Tóquio são os outros dois mais fortes.

**Como forkar (a mecânica do guia):**
1. Clonar `E:\dev-d\_projects\guia-malaga-pwa` → `_projects/guia-<cidade>` (o
   guia-malaga é o mais evoluído: padrão hospedagem/voos + "Minhas reservas"
   on-device; NÃO usar o Puerto Varas, mais antigo). Stack = SvelteKit estático
   + PWA + Leaflet + localforage.
2. Trocar a camada de conteúdo da cidade (pontos, bairros, dicas). Fotos vêm do
   mesmo pipeline do Mac (repo-ponte `kit-imagens`).
3. Adicionar o slot do link "aprenda a língua" → app Journeyo.
4. `gh repo create aleapc/guia-<cidade> --public` → publicar em
   `aleapc.github.io/guia-<cidade>` (convenção: pasta = nome do repo).

## Contexto que vale saber

- Editar a fonte do mapa: `dev-hosting/guias-mapa/index.html` (dados no array
  `PAISES` no `<script>`; commit + push atualiza a página).
- Ambiente PC↔Mac tudo em git (ver memória `sync-entre-maquinas`).
- O app de cursos Journeyo (a outra ponta do cross-sell) está descrito na
  memória `kit-de-bordo-rebrand-journeyo`.
