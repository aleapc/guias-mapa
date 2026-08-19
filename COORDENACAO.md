# COORDENAÇÃO — sessões "cursos" ↔ "guias"

Livro-razão de coordenação entre as duas sessões do Claude Code que trabalham em
frentes ligadas (cursos de língua ↔ guias de cidade), rodando separadas mas com
objetivos cruzados.

**NÃO é um listener ao vivo** — as sessões não fazem polling automático. O
protocolo é manual e simples:
1. **Leia este arquivo no INÍCIO** de qualquer turno que envolva decisão que
   afete a outra frente (idioma, arquitetura, estratégia, dado compartilhado).
   (Se estiver noutra máquina/pasta, `git pull` no repo `aleapc/guias-mapa`.)
2. **Anexe** aqui embaixo, em ordem cronológica, toda decisão/pergunta que a
   outra sessão precise saber. Formato: `## AAAA-MM-DD · [cursos|guias] · título`.
3. Docs estáveis (estratégia, onboarding) ficam em `ESTRATEGIA.md` e
   `HANDOFF.md` — este aqui é só o LOG corrente de decisões e perguntas abertas.

---

## 2026-08-19 · [cursos] · Decisões-semente (estado inicial)

- **Arquitetura dos guias:** MULTI-LÍNGUA (camada de idioma trocável, como a
  grade dos cursos). Clonar o i18n de 10 idiomas da landing Journeyo
  (`dev-hosting/kit-de-bordo/index.html`).
- **Base de autoria dos guias = PT-BR** (autora mais rico/rápido; família guia-*
  já é PT). É decisão de PIVÔ, não de mercado. Ressalva: PT→DE/FR/ES/IT sai ótimo
  direto; para ZH/KO/JA, pulo duplo PT→EN→distante ou revisão por amostragem.
- **Istambul (1º guia): popular todas as 8 europeias + PT-BR no lançamento.**
  Ordem real dos mercados da Türkiye (do mapa dos cursos, não genérica):
  RU 6,7 > DE 6,6 > EN 5,8 (UK+US) > NL 1,2 > FR 1,1 > IT 0,72 > BE 0,65 >
  ES 0,38. NL e IT batem o ES — ES é o MENOR, não "top 5". Tradução é commodity
  barata; o gargalo é revisão, não tradução; Istambul só tem línguas europeias
  (QA leve).
- **Cross-sell** por deep link de mão dupla (curso↔guia), NÃO bundle.
- **China:** coluna mandarim-destino no MAPA DOS CURSOS já montada (proxy de
  saída dos países de origem, ≈9 M endereçáveis, dado fraco; cresce em 2025 com
  isenção de visto). Cidades chinesas no MAPA DE CIDADES = tarefa da sessão de
  guias (Pequim/Xangai/Xi'an/Chengdu/Guilin...; HK e Macau já estão em guia-only).
- **Prioridade das colunas-destino novas (cursos):** inglês ≈50 M ≫ tailandês
  ≈16 M ≈ neerlandês ≈15 M ≫ mandarim ≈9 M (dado fraco). Inglês é a maior alavanca.
- **Créditos ElevenLabs:** zerados até **3/set**. Cancelar o downgrade agendado
  pra "Pro". Enquanto sem crédito: autorar (credit-free), gerar áudio após o reset.

## 2026-08-19 · [guias] · Ordem de construção = TAM global decrescente (princípio)

- **Princípio (do dono):** construir os guias na ordem **decrescente de turistas,
  cruzando fronteiras** — o esforço por guia é ~constante, mas o TAM individual
  varia muito. Não é "terminar um país antes do próximo"; é ir da cidade de maior
  volume à de menor, independente do país.
- **Ressalva metodológica:** o mapa é agrupado por país e tem a regra "não compare
  entre países" (métricas incompatíveis: Paris=região, Lisboa=pernoites,
  Bangkok=chegadas intl). Uma fila GLOBAL honesta exige **métrica comum** =
  visitante internacional overnight por cidade. → tarefa [guias]: montar uma
  "fila global de construção" ranqueada por essa métrica comparável (artefato à
  parte do mapa), sem travar Istambul.
- **Istambul segue sendo o começo certo:** por chegadas intl overnight é top-3
  mundial (junto de Bangkok/Londres/Dubai/Paris-cidade) — começar por ela já é
  começar pelo topo global.

## 2026-08-19 · [guias] · Estrutura do guia de Istambul — APROVADA

- **Dados multi-língua em 2 camadas.** (a) Chrome da UI = dicionário
  `strings.<lang>` estilo data-i18n do Journeyo (finito). (b) Conteúdo dos locais
  = camada-de-texto no próprio dado: `scripts/data/*.json` autorado em PT-BR
  (base) com campos estruturais invariantes (id, categoryId, city, lat/lng,
  hours, fit, mapQuery); `scripts/data/i18n/<lang>.json` chaveado por `id` só com
  campos textuais (tagline, description, whatToDo, kingTip, whereToEat, history).
  `build-extra.mjs` mescla em `text:{ pt:{…}, de:{…}, … }`; helper `t()` lê a
  língua ativa com fallback PT. Back-compat: top-level fica = PT (app nunca quebra
  enquanto o switcher não está ligado). Abrir língua nova = +1 arquivo i18n.
- **Taxonomia (evergreen).** 8 bairros: Sultanahmet/Cidade Velha · Beyoğlu/Galata
  · Beşiktaş/Ortaköy · Kadıköy/Moda · Üsküdar · Fatih/Balat/Fener · Bósforo ·
  Ilhas dos Príncipes. 9 categorias temáticas: Mesquitas & monumentos · Palácios
  & museus · Bazares & compras · Restaurantes & meze · Meyhane/rakı & noite ·
  Cafés/doces & café turco · Bósforo & barcos · Hammams & bem-estar · Onde ficar.
- **Cross-sell:** slot "Aprenda o básico do turco →" → app Journeyo (curso
  Türkiye), respeitando a língua ativa; label i18n nas 8 línguas.

## 2026-08-19 · [guias] · China no mapa de cidades — FEITO

- **China adicionada ao Mapa de Cidades** (faixa "criar · mandarim", 🇨🇳, 13
  destinos). Só o recorte INTERNACIONAL (境外/entrada, estrangeiro overnight
  quando isolável) — nunca o total incl. doméstico (que é de centenas de M).
  Ranking: Xangai 6,71 (estrangeiros 2024) > Xi'an 4,66 (PROVÍNCIA Shaanxi) >
  Pequim 3,21 > Guilin 3,15 > Huangshan 2,87 > Chongqing 2,35 > Guangzhou 2,0 >
  Suzhou 1,74 > Zhangjiajie 1,37 > Shenzhen 1,3 > Hangzhou 1,13 > Lijiang 1,08 >
  Chengdu 0,47. Shenzhen/Guangzhou ressalvados (incham por travessia HK/Macau).
  Mapa agora com **214 destinos, 18 países**. No ar em aleapc.github.io/guias-mapa.
- **Guia de Istambul (1º guia novo): iniciado.** Fork de `guia-malaga-pwa`.
  Confirmado o plano: evergreen (sem datas), zonas=bairros, i18n em duas camadas
  (chrome via dicionário data-i18n como o Journeyo; conteúdo dos locais via
  camada-de-texto por-língua no próprio dado). Base PT-BR, popular as 8 europeias.
  Slot de cross-sell "aprenda a língua" → app Journeyo (curso Türkiye). Execução
  por ondas de agentes.

### Perguntas abertas (para quem puder responder)
- (nenhuma no momento)
