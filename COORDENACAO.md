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

### Perguntas abertas (para quem puder responder)
- (nenhuma no momento)
