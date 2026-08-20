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

## 2026-08-20 · [cursos] · curso-reinounido-fr: abre a sub-coluna inglês BRITÂNICO
- **Autoria concluída**: França→Reino Unido (3,6 M), a maior célula a criar
  depois das já abertas. Scaffold clonado do `curso-eua-es` (reúso da camada-
  alvo inglesa), guia re-derivada pro FRANCÊS, alvo adaptado de americano
  pra **britânico** (vozes Alice/George, vocabulário the bill/loo/queue/
  takeaway/lift, nunca "the subway" — no UK é passagem de pedestre).
- **Fatos-âncora (fonte)**: trânsito pela esquerda + "LOOK RIGHT" pintado no
  asfalto; contactless/TfL (cartão estrangeiro FUNCIONA, ao contrário do
  PINNEN holandês); libra≠euro; pub (pedir e pagar no balcão); service
  charge discricionário ~12,5% (contraste com o *service compris* francês);
  **correção real que a pesquisa trouxe**: o turista francês usa o PRÓPRIO
  cartão CEAM/EHIC, não um "GHIC" (esse é do residente britânico).
- **Modelo**: Fase 1 **Opus 5 · Alto** (1ª vez usando o Opus 5 nesta sessão,
  antes era 4.8) + Fase 2 Sonnet 5 · Médio + frota (4 agentes). Marca:
  «Cheers!». Termo do método: «la formule».
- **Consequência estratégica**: as próximas células →Reino Unido (Alemanha
  3,3 M, Espanha 2,6 M, Itália 1,9 M, Países Baixos 2,0 M) viram derivações
  baratas — reusam a camada-alvo britânica que este SKU acabou de criar.
- **Portão estendido**: G6 (anti-estereótipo) não tinha NENHUM gentílico
  britânico na regra francesa — "les Britanniques sont réservés" passava
  verde. Estendido + testado (10/10, incl. distinguir "à l'anglaise" [modo,
  dispara] de "passer à l'anglais" [trocar de língua, não dispara — 3 falsos-
  positivos reais achados no curso-espanha-fr publicado, corrigidos).
- **Achado catalog-wide, corrigido parcialmente**: o fallback de voz do
  navegador (`speech.ts`) estava hard-coded pra espanhol em praticamente
  todo o catálogo — confirmado em SKUs JÁ PUBLICADOS (curso-alemanha-en,
  curso-turquia-en). Corrigido nos 5 SKUs desta sessão (parametrizado por
  `targetLang`); resto do catálogo fica como tarefa separada — ver memória
  `kit-de-bordo-fallback-voz-hardcoded`.
- **Validado**: PASSA, zero erro. GitHub: `github.com/aleapc/curso-reinounido-fr`.

## 2026-08-20 · [cursos] · China: DESPRIORIZADA como origem, mantida como destino
- **Decisão do dono.** Motivo de DISTRIBUIÇÃO, não só de dado: vender app
  PARA chinês é travado. **Google Play não existe na China** (só lojas locais
  Huawei/Xiaomi/Tencent, exigem entidade+ICP). **Apple China App Store** exige
  **filing ICP (备案)** desde 2023-24 — sem entidade jurídica chinesa não se
  publica. PWA dribla as lojas mas esbarra no Great Firewall (GitHub Pages
  instável na China). Como o plano é converter os PWAs em **apps nativos** pra
  as stores, a trava chinesa morde de cheio.
- **Consequência:** as linhas de comprador chinês (`-zh`) já construídas
  (curso-japao-zh, curso-italia-zh, curso-espanha-zh…) herdam esse problema de
  monetização. Não é perda — o áudio-alvo delas é reusado a custo zero pelas
  outras origens — mas **não priorizar publicação/marketing da coluna `-zh`**.
- **China como DESTINO segue valendo** (coluna mandarim-destino do mapa,
  turista estrangeiro→China: o comprador é alemão/coreano/etc. e compra na
  loja do próprio país). Aposta real da China é essa.
- **Impacto p/ [guias]:** um guia de cidade chinesa (Pequim/Xangai…) é vendido
  a estrangeiros nas lojas deles — OK. Só evitar depender de alcançar o
  usuário DENTRO da China.

---

## 2026-08-20 · [cursos] · curso-holanda-de: 2º destino novo, texto fechado e no GitHub
- **Autoria concluída** do `curso-holanda-de` (survival Neerlandês → Países
  Baixos, guia em ALEMÃO). 2ª maior alavanca a criar do mapa depois do inglês:
  **Alemanha→Países Baixos = 7,54 M**, a maior célula "a criar" isolada, e o
  **neerlandês como língua-ALVO pela 1ª vez** no catálogo. 36 ep + 36 quiz +
  moldes.json (10 operacionais + 3 sociais) + config + casca.
- **Scaffold do espelho exato `curso-alemanha-nl`** (NL→Alemanha), papéis de
  voz invertidos: guia alemã Juli/Thomas, alvo neerlandês Noa/Wim.
- **Par mais PRÓXIMO do catálogo** (duas germânicas ocidentais vizinhas): o
  neerlandês é o destino morfologicamente mais fácil — sem caso, «een»
  invariável, estrutura V2 pronta. O custo do aluno migra de montar a frase
  para a **ARMADILHA DO COGNATO** (falso amigo: mogen≠mögen, eng≠eng,
  brutaal≠brutal) e a pronúncia (g/ch, ui, ij). Marca do produto: «Zeg het
  maar!»; termo do método: «Baustein».
- **Modelo:** Fase 1 Opus 4.8 Alto (FUNDACAO com pesquisa sourced dos
  diferenciais NL — PINNEN é o fato nº1 — + moldes + ouro B06); Fase 2
  Sonnet 5 Médio + frota (35 partes + 3 sociais). Mesmo padrão do curso-eua-es.
- **Correções de lei/robustez:** WANN-IST movido de I01 (M2) → B18 (M1),
  mesma violação §5.1 do eua-es; reclassifiquei 2 politeners que ocupavam
  indevidamente o teto social; adicionei entrada 'nl' à tabela MARCAS do G14
  (par de MAIOR risco de vazamento do catálogo por proximidade DE↔NL).
- **Percalço:** um blip de rede ("connection lost") derrubou os 4 agentes da
  Fase 2 quase juntos, com pouca gravação; relançados, fecharam limpo.
- **Validado:** esqueleto/estrutura/tom → **PASSA**, zero erro. No GitHub:
  `github.com/aleapc/curso-holanda-de`. Falta voz-guia/alvo (reset ElevenLabs
  3/set) e deploy. Mapa marca "em obra" (◐).

## 2026-08-20 · [cursos] · curso-eua-es: texto fechado, validado e no GitHub
- **Autoria concluída** do 1º SKU da coluna inglês-destino: `curso-eua-es`
  (survival English → EUA, guia em espanhol mexicano). **Par estruturalmente
  inédito** — inglês como língua-ALVO pela 1ª vez no catálogo (sempre foi
  guia). 36 episódios + 36 quizzes + `moldes.json` (10 moldes operacionais)
  + config (vozes invertidas do curso-espelho `curso-mexico-en`).
- **Modelo em 2 fases, confirmado como padrão pra próximos destinos novos:**
  Fase 1 (Opus 4.8 · Alto) autorou `moldes.json` + o episódio-ouro B06 —
  a decisão estrutural inédita (como "inglês ensinado, guiado em espanhol
  mexicano" soa na prática) e o padrão de campo/tom que os outros 35
  replicam. Fase 2 (Sonnet 5 · Médio + frota, 4 agentes por módulo) autorou
  as 35 partes restantes, replicando o padrão. Fase 2.1 (1 agente focado)
  corrigiu um portão de densidade (G3) que ficou abaixo do piso.
- **Correção de lei aplicada durante a Fase 1:** o roster original (do
  FUNDACAO.md) dava casa a 2 moldes operacionais (WHAT-TIME, WENT-WRONG)
  dentro de M2/APROVEITO — contra o PRODUTO §5.1 ("todo operacional nasce
  em M1; M2 só troca encaixe, exceto 3 sociais nomeados"). Corrigido:
  WHAT-TIME→B18, WENT-WRONG→B16 (M1); I01/I06 viraram redisparo, não casa.
- **Validado:** `valida-esqueleto`/`valida-estrutura`/`valida-tom` → **PASSA**,
  zero erro. No GitHub: `github.com/aleapc/curso-eua-es`, branch `main`.
- **Falta para publicar:** voz-guia/alvo (aguarda reset ElevenLabs 3/set) e
  `deploy.sh`. Mapa marca "em obra" (◐), não "no ar".

## 2026-08-20 · [cursos] · KO/ZH→Japão: texto fechado, validado e no GitHub
- **Autoria concluída** dos dois SKUs em produção do mapa: `curso-japao-ko` e
  `curso-japao-zh` (36 episódios + 36 quizzes + moldes.json + bolso.json +
  chrome/casca cada, 75 arquivos por SKU). Scaffold clonado de `curso-japao`
  (EN→Japão), reusando 100% a camada-alvo japonesa (áudio + arte); só a
  camada de guia (coreano/mandarim) foi traduzida — modelo Sonnet 5 Medium
  + frota, confirmando a regra de derivação (sem Opus, sem pesquisa
  contrastiva fonética profunda — esse nível só existe no exemplar alemão).
- **Validado:** `npm run estrutura` e `npm run casca` verdes nos dois.
  Corrigido um resíduo de clone que os dois carregavam (chrome/`<title>`/meta-
  description ainda em inglês — "Japan survival Japanese" — apesar do
  conteúdo já estar traduzido; ver [[kit-de-bordo-residuo-de-clone]]).
- **No GitHub:** repos `aleapc/curso-japao-ko` e `aleapc/curso-japao-zh`
  criados, branch `main` com o código-fonte, push feito.
- **Falta para publicar:** voz-guia (coreana/mandarim — aguarda o reset de
  créditos ElevenLabs em 3/set) e rodar `deploy.sh` (gh-pages). Status no
  mapa continua "em obra" (◐), não "no ar" — texto pronto ≠ SKU publicado.
- **Achado de processo:** a autoria em frota gerou bastante trabalho
  duplicado (vários sub-agentes traduzindo os mesmos arquivos em paralelo,
  detectado via "arquivo modificado no disco desde a última leitura") — não
  causou dano (conteúdo final correto nos dois casos), mas gastou mais
  tokens que o necessário. Um orquestrador ficou preso num loop achando que
  faltava trabalho já concluído; precisou de verificação manual externa
  para destravar.

## 2026-08-20 · [cursos] · Saneamento: 20 SKUs sem git local, código-fonte nunca versionado
- **Achado (antes de autorar KO/ZH→Japão):** 20 pastas em
  `kit-de-bordo-worktrees/` (toda a frota derivada a partir de ~11/ago —
  curso-japao, curso-espanha-ko/zh, curso-italia-ko/zh, curso-portugal-*,
  curso-alemanha-*, curso-franca-*, curso-turquia-ru, curso-eua-es) não
  tinham `.git` local. Os repos remotos só tinham o branch `gh-pages`
  (build compilado); o código-fonte (moldes.json, episódios, docs) nunca
  tinha sido versionado — existia só como arquivos soltos no disco, sem
  backup. `curso-eua-es` nem repo remoto tinha.
- **Corrigido:** `git init` + commit + push de um branch `main` novo em
  cada uma das 20 (18 linkadas a remotos já existentes; `curso-eua-es`
  ganhou repo novo `github.com/aleapc/curso-eua-es`). Convenção mantida:
  `main` = fonte, `gh-pages` = build (deploy.sh recria a árvore órfã, não
  mexe no `main`). Nenhum áudio/binário entrou — `.gitignore` já filtrava.
- **Se a sessão de guias tiver o mesmo padrão** (worktrees de `guia-*` sem
  `.git`, remoto só com um branch de build), vale o mesmo saneamento —
  checar com `for d in */; do [ -d "$d/.git" ] && echo TEM || echo SEM $d; done`.

## 2026-08-20 · [cursos] · Mac ligado com listener ativo + namespace da ponte de imagens

- **Mac está ligado agora**, com o loop de polling do `kit-imagens` ativo
  (`git pull` a cada ~2 min, lendo `pedidos/*.json`). Documentação completa do
  protocolo já existe no próprio repo — **leiam antes de pedir a 1ª imagem**:
  `E:\dev-d\kit-imagens\README.md` (mecânica pedido↔entrega) e
  `METODO-OPERACAO.md` (como o Mac opera o ChatGPT, formatos, trava anti-
  pseudo-texto). O repo é o mesmo bridge que já produziu Japão (36/36).
- **Como encomendar (qualquer uma das 3 pontas — cursos, guias, Mac):**
  soltar `pedidos/<curso>.json` (lista fechada de ids/arquivos, contrato) +
  `.md` legível no repo `kit-imagens`, git push. O Mac descobre sozinho no
  próximo pull (sem lock, sem "done" — o disco em `entregues/<curso>/` é a
  fonte da verdade; idempotente, retoma sozinho se cair no meio).
- **Namespace — a trava contra troca de imagens entre as duas sessões do PC:**
  o campo `"curso"` do pedido = o nome da pasta em `entregues/` = **chave
  única em TODO o repo**, compartilhada pelas 3 pontas. Prefixos já em uso
  pela sessão [cursos]: `destino-*` (acervo-alvo, ex. `destino-japao`),
  `curso-*` (legado), `mexico-regen`. **A sessão [guias] usa prefixo
  `guia-<cidade>` e NUNCA toca em `destino-*`/`curso-*`** (ex.:
  `guia-istambul`, não `istambul` nem `destino-istambul` — evita colidir com
  um destino de curso de mesmo nome). Antes de criar um pedido novo, `git
  pull` + conferir que o nome não existe em `entregues/` nem em `pedidos/`.
- **Disciplina de push no bridge (as 3 pontas):** sempre `git pull --rebase -q`
  antes de `git push` no `kit-imagens` — é como o Mac já opera
  (`METODO-OPERACAO.md`), e evita que um push de uma ponta apague o commit
  de outra. Cada imagem é um commit próprio; não amend, não force-push.
- **Nada pedido por [cursos] agora:** KO→Japão e ZH→Japão (o SKU em
  andamento) reusam 100% do acervo `entregues/destino-japao/` já fechado —
  zero imagem nova, só a camada de guia coreana/mandarim.

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

## 2026-08-20 · [guias] · Londres PUBLICADO 🎉 (4º guia no ar)

- **No ar:** https://aleapc.github.io/guia-londres/ (repo `aleapc/guia-londres`).
  Selo no mapa; KPI 3→4 guias. **114 locais** nos 8 áreas (Westminster, City &
  Tower, South Bank, West End/Soho, Kensington, Camden, Shoreditch, Greenwich),
  **8 idiomas**. Fork do guia-istambul; camada local = Reino Unido (999, Oyster/
  Tube, libra, Heathrow, dirige à esquerda). Verificado ao vivo em italiano.
- **Cross-sell:** "Aprenda o básico do inglês → Journeyo". O curso de INGLÊS-
  destino ainda é "a criar" (aponta pra landing) — o guia **semeia** a demanda
  dele, exatamente o que a ESTRATEGIA prevê. **[cursos]:** Londres é munição pra
  priorizar a coluna inglês-destino (a maior alavanca, ~50 M).
- **Fotos:** pedido `guia-londres` (~114) publicado no `kit-imagens` (nº 16).
- **Método (achado):** o agente de tradução DE de 114 locais **estourou o teto de
  64 K tokens de saída** num Write único e depois **caiu por "connection lost" em
  respostas grandes**. Cura: chunk de ~28 locais por agente (2 arquivos) → robusto.
  Adendo à regra "1 agente por arquivo": **e mantenha a saída pequena** (<~30
  locais/write). Vale pros SKUs de curso também.
- **Fila de imagens do Mac agora:** guia-istambul (123) → guia-paris (111) →
  guia-londres (114). Atualizei o STATUS.md.

## 2026-08-20 · [guias] · Mac orientado + fila de imagens (para [cursos] enxergar)

- O Mac estava parado ("aguarda orientação") porque o `kit-imagens/STATUS.md`
  estava defasado (fila antiga dos cursos, 05/ago) e não citava os pedidos novos.
  **Reescrevi o `STATUS.md`** com a fila real: **produzir `guia-istambul` (123) →
  depois `guia-paris` (111)**; expliquei o FORMATO NOVO (guia de cidade: cada id é
  um local específico com prompt próprio no `.md`, NÃO a grade de 36 cenas do curso;
  `.webp` 1200×800; mesma disciplina anti-texto do Japão).
- **[cursos]: não empurrem um STATUS.md conflitante** — se precisarem de imagens,
  acrescentem à fila (append no STATUS) em vez de sobrescrever, e avisem aqui. Por
  ora, como vocês mesmos anotaram, [cursos] não tem pedido de imagem pendente
  (KO/ZH→Japão reusam o acervo japonês). Então o Mac trabalha só a fila de guias.
- Guia de Londres (4º) em produção nesta sessão (conteúdo pronto; traduções +
  publicação a seguir). Quando publicar, entra a fila `guia-londres`.

## 2026-08-20 · [guias] · Paris PUBLICADO 🎉 (3º guia no ar)

- **No ar:** https://aleapc.github.io/guia-paris/ (repo `aleapc/guia-paris`,
  `main`=fonte, `gh-pages`=build). Selo no mapa; KPI 2→3 guias.
- **~110 locais** nos 8 quartiers (Cité/Louvre, Marais, Latin, Eiffel/Champs,
  Montmartre, Ópera, Canal/Bastille, Versalhes), **8 idiomas** (pt+de/en/ru/nl/
  fr/it/es). Fork do guia-istambul → herdou o runtime i18n inteiro; camada local
  refeita p/ França (112, Navigo/Métro, euro, CDG, frases em francês, roteiro por
  quartier). Verificado ao vivo em alemão.
- **Cross-sell:** "Aprenda o básico do francês → Journeyo". O curso de FRANCÊS já
  está no ar → **a recíproca (link no curso → https://aleapc.github.io/guia-paris/)
  é de vocês [cursos]**, quando quiserem; casa na hora, como Istambul/Türkiye.
- **Fotos:** pedido `guia-paris` (~110) publicado no `kit-imagens` — o Mac produz.
- **v1 (fast-follow, igual Istambul):** prosa longa das telas utilitárias + o
  fitLabel/insights ainda em PT nas 8; o núcleo (browse + detalhe) é multilíngue.
- **Método:** confirmei o padrão de trabalho-duplicado que vocês relataram — 2
  agentes escrevendo o mesmo arquivo clobbaram um `de.json` p/ `{}`; a cura é
  1 agente por arquivo (single-pass) + `TaskStop` nos zumbis. Já aplicado aqui.
- **Próxima cidade (TAM-global decrescente):** Londres (maior inglês-destino
  limpo, semeia o curso de inglês) ou Bangkok (nº1 mundial, mas overlap com o
  guia-tailandia). A definir com o dono.

## 2026-08-20 · [guias] · Istambul PUBLICADO 🎉 (2º guia no ar)

- **No ar:** https://aleapc.github.io/guia-istambul/ (repo `aleapc/guia-istambul`,
  `main`=fonte, `gh-pages`=build). Selo "guia no ar" já no mapa; KPI 1→2 guias.
- **123 locais** nos 8 bairros, **8 idiomas** (pt base + de/en/ru/nl/fr/it/es,
  123 cada) — conteúdo E chrome principal multi-língua, switcher no menu +
  auto-detecção. Cross-sell "Aprenda turco → Journeyo" (en/de/ru linkam o curso
  na língua do comprador; demais → landing). Evergreen, clima real de Istambul.
- **Para [cursos]:** a recíproca do cross-sell é de vocês — quando quiserem, um
  link no curso Türkiye do Journeyo → https://aleapc.github.io/guia-istambul/ .
- **v1 — limitação conhecida (fast-follow):** telas utilitárias secundárias
  (bolso/úteis/voos/roteiro) têm o texto LONGO ainda só em PT; o núcleo (browse
  de locais por categoria/bairro + detalhe) é multi-língua nas 8.
- **Fotos:** faltam (app cai no gradiente+emoji). Próximo: encomendar ao Mac via
  `kit-imagens` com pedido `guia-istambul` (prefixo da sessão [guias], conforme a
  entrada do Mac acima) — 123 ids. Ainda NÃO pedido.
- **Próxima cidade** pela ordem TAM-global: candidatas Bangkok / Londres / Dubai
  / Paris-cidade (a "fila global comparável" segue como artefato a montar).

## 2026-08-20 · [guias] · Istambul: Phase 0b feito, indo até publicar

- **Phase 0b (evergreen + de-Málaga) concluído** (commit 7d2b52c no repo local
  guia-istambul): removida a personalização do casal; clima/datas → evergreen
  (rótulo de estação); toda a camada local reescrita p/ Türkiye (alerts das 4
  estações, plan, usefulInfo/112/Istanbulkart/lira, bolso com frases em TURCO,
  voos Brasil→IST, roteiro de 5 dias por bairro, úteis PT↔TR). App lê 100% como
  Istambul, build verde.
- **Agora indo até CONCLUIR a cidade** (sem parar): runtime i18n (switcher +
  navigator.language + chrome nas 8 línguas) · slot cross-sell "Aprenda turco"
  → Journeyo · ícones · ~150 locais (ondas de agentes Sonnet por bairro) ·
  traduções nas 8 europeias · criar repo aleapc/guia-istambul + publicar · selo
  no mapa. Modelo: fio principal Opus/médio, ondas de conteúdo/tradução → Sonnet.
- Nota p/ [cursos]: quando Istambul publicar, o cross-sell aponta pro curso
  Türkiye do Journeyo; a recíproca (link no curso → guia) fica do lado de vocês
  quando fizer sentido.

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

## 2026-08-19 · [cursos] · Começou a autoria da coluna inglês-destino
- 1º SKU: **curso-eua-es** (survival English → EUA, guia espanhol/mexicano),
  escolhido por TAM (México→EUA ≈17 M, maior corredor do mapa).
- Inglês como ALVO é novidade estrutural (targetLang:'en', 1ª vez).
- Fundação autorada (roster de 10 moldes + fatos-diferencial com fonte) em
  kit-de-bordo-worktrees/curso-eua-es/docs/FUNDACAO.md e na memória
  curso-eua-fundacao. Falta scaffold + 36 episódios (credit-free até 3/set).
- Sem impacto direto na sessão de guias — registro pra visibilidade.

## 2026-08-20 · [cursos] · CORREÇÃO: México desinflado; curso-eua-es reordenado
- **Achado com fonte (US NTTO/I-94 2024 + Banxico 2023):** o corredor
  México→EUA NÃO é 17 M de turista-comprador. Os 52 M de saídas do México =
  16 M overnight (quase tudo p/ EUA) + 36 M fronteiriços same-day (inglês alto,
  fora do encaixe). Dos que ficam nos EUA: **3,5 M de avião** (lazer real) +
  13,4 M terrestres (fronteiriços, inglês alto). **TAM honesto de survival-EN
  ≈ 3,5 M, não 17 M.** A entrada de 2026-08-19 (linha 100) está corrigida.
- **Consequência de priorização:** a coluna inglês cai de ≈50 M → **≈34 M**
  (EUA 17,3 + Reino Unido 16,3). Segue sendo a maior coluna-destino, mas o
  corredor-âncora era inflado. O **cluster KO/ZH→Japão (15,8 M, dado limpo,
  áudio-alvo japonês JÁ pronto)** é agora o próximo SKU mais valioso E mais
  barato — acima de continuar o curso-eua-es (que precisa de camada-alvo
  inglesa NOVA). Decisão de qual autorar primeiro ainda com o dono.
- **Mapa dos cursos atualizado e no ar:** México adicionado como 16ª origem
  (matriz 16×17); curso-eua-es marcado "em obra" (◐); KPIs recalibrados
  (59,5% no ar = 223,5 de 375,8 M; universo cresceu +165 M com a fronteira).

## 2026-08-20 · [guias] · Roma PUBLICADA (5º guia de cidade)
- **No ar:** https://aleapc.github.io/guia-roma/ (repo `aleapc/guia-roma`,
  `main`=fonte, `gh-pages`=build via `deploy.ps1`, BASE_PATH=/guia-roma).
- Fork do guia-istambul. **108 locais** em 8 rioni (Roma Antiga, Vaticano,
  Centro Storico, Piazza di Spagna, Trastevere, Monti, Villa Borghese,
  Testaccio) + 8 categorias temáticas. **8 idiomas** (pt/de/en/ru/nl/fr/it/es).
  Info-local Itália (Euro, 112, ATAC/Roma Pass, Leonardo Express, nasoni,
  código de vestimenta no Vaticano, ZTL). Cross-sell → **curso de italiano**
  no Journeyo (curso já no ar → recíproca imediata). Verificado ao vivo em
  italiano (página do Coliseu renderiza traduzida, sem erros de console).
- **Selo no mapa + KPI 4→5** (Málaga, Istambul, Paris, Londres, Roma).
- **Janela de degradação da API (connection-lost em respostas grandes):**
  writes de 108 chaves caíam repetidamente; a cura foi **partir em 2 metades
  de 54** (mesmo padrão do alemão de Londres) — sobrevivem à conexão instável.
  Regra reforçada: tradução por agente deve manter SAÍDA ≲54 itens/write.
- **Bug de dado corrigido:** `rom_piazza_del_popolo` estava duplicado (borghese
  + spagna, mesmas coords) → removida a duplicata; 109→108 locais únicos.
- **Fila de fotos do Mac (kit-imagens):** guia-istambul (123) → guia-paris (111)
  → guia-londres (114) → **guia-roma (108)** — pedido nº 17.
- **Próxima cidade** (TAM-global decrescente): a definir com o dono
  (candidatas: Dubai, Nova York, Bangkok — este último pesa overlap com
  guia-tailandia).

## 2026-08-20 · [guias] · Bangkok PUBLICADA (6º guia de cidade)
- **No ar:** https://aleapc.github.io/guia-bangkok/ (repo `aleapc/guia-bangkok`,
  `main`=fonte, `gh-pages`=build via `deploy.ps1`, BASE_PATH=/guia-bangkok).
- Fork do guia-istambul. **108 locais** em 8 bairros (Rattanakosin, Thonburi,
  Chinatown/Yaowarat, Dusit, Siam/Pathumwan, Sukhumvit, Silom/Sathorn,
  Chatuchak/Ari) + **10 categorias temáticas** (surgiram 2 novas na autoria:
  parques e cultura). **8 idiomas** (pt/de/en/ru/nl/fr/it/es). Info-local
  Tailândia (baht ฿, 191/1669, BTS/MRT/Rabbit, barco Chao Phraya,
  Suvarnabhumi/Don Mueang, código de templo, lèse-majesté, frases em tailandês).
  Cross-sell → **curso de tailandês** (ainda "a criar" → o guia SEMEIA a demanda,
  modelo Londres). Verificado ao vivo em italiano (Wat Pho renderiza traduzido).
- **Escolhida pelo MAPA:** por chegadas intl (métrica de guia de cidade) Bangkok
  é o nº 1 do mundo (32,4 M). O overlap com `guia-tailandia` NÃO se aplica —
  aquele é um guia de VIAGEM DATADA (casal, 19/11-05/12/2026, país inteiro,
  Bangkok = 1 de 7 zonas). Este é o produto EVERGREEN de cidade. Reúso: a prosa
  PT de ~17 marcos de Bangkok foi semeada a partir do guia-tailandia (contentExtra).
- **Selo no mapa + KPI 5→6** (Málaga, Istambul, Paris, Londres, Roma, Bangkok).
- **Fila de fotos do Mac:** …guia-roma (108) → **guia-bangkok (108)** — pedido nº 18.
- **API saudável neste build** (sem a degradação de Roma): todas as 6 traduções
  inteiras + DE em metades pousaram; conteúdo (8 zonas) em 1 write cada.
- **Próxima cidade** pelo mapa (chegadas intl, sem selo): **Singapura (16,5 M)**,
  depois Antalya (14,8), Pattaya (10,5), Nova York (8,9).

## 2026-08-20 · [guias] · Singapura PUBLICADA (7º guia de cidade)
- **No ar:** https://aleapc.github.io/guia-singapura/ (repo `aleapc/guia-singapura`,
  `main`=fonte, `gh-pages`=build via `deploy.ps1`, BASE_PATH=/guia-singapura).
- Fork do guia-istambul. **108 locais** em 8 distritos (Marina Bay, Distrito
  Cívico/Colonial, Singapore River & Quays, Chinatown, Little India, Kampong
  Glam & Bugis, Orchard, Sentosa) + **10 categorias temáticas** (iconicos,
  templos, hawker, compras, natureza, museus, rooftops, familia, heritage,
  hospedagem). **8 idiomas** (pt/de/en/ru/nl/fr/it/es). Info-local Singapura
  (SGD S$, MRT/EZ-Link, Changi, leis rígidas, 999/995, água potável,
  inglês/Singlish). Cross-sell → **curso de inglês** (a criar → SEMEIA, como
  Londres — Singapura é inglês-destino). Verificado ao vivo em italiano
  (Marina Bay Sands renderiza traduzido).
- **Escolhida pelo MAPA:** por chegadas intl sem selo, Singapura (16,5 M) é a nº 1.
- **Selo no mapa + KPI 6→7** (Málaga, Istambul, Paris, Londres, Roma, Bangkok, Singapura).
- **Fila de fotos do Mac:** …guia-bangkok (108) → **guia-singapura (108)** — pedido nº 19.
- **Achado de método:** os 2 agentes de tradução DE gravaram o JSON como ARRAY
  (chaves 0,1,2…) em vez de objeto keyed-by-id; o merge colapsou por índice e
  perdeu metade. Cura: relançar com EXEMPLO explícito do formato {"sg_id": {...}}.
  Regra reforçada: no prompt de tradução, mostrar o shape de saída literal.
- **Próxima cidade** pelo mapa (chegadas intl, sem selo): **Antalya (14,8 M, Türkiye)**,
  depois Pattaya (10,5, overlap c/ guia-tailandia), Nova York (8,9).
