# Plano de Curso â€” Design + VÃ­deo com IA

**Combinando Claude Design (claude.ai/design) + Hyperframes Student Kit**
**DuraÃ§Ã£o estimada:** 8 mÃ³dulos Ã— 2â€“3h = 20â€“24h de estudo ativo
**Formato:** autodirigido com projetos prÃ¡ticos progressivos
**Idioma:** PortuguÃªs (BR)
**Data do plano:** 2026-04-19

---

## VisÃ£o geral

Este curso ensina a produÃ§Ã£o visual ponta-a-ponta com IA â€” do briefing estÃ¡tico (landing page, deck, protÃ³tipo) ao vÃ­deo motion-graphics finalizado â€” integrando duas ferramentas complementares:

1. **Claude Design** (claude.ai/design) â€” gera designs estÃ¡ticos ship-ready: landing pages, pitch decks, scroll-driven sites, protÃ³tipos clicÃ¡veis de app.
2. **Hyperframes Student Kit** (cchyperframes) â€” pipeline de vÃ­deo em HTML + GSAP com 12 projetos finalizados para engenharia reversa (short-form TikTok, promos SaaS, aulas educacionais, hype films de marca).

A lÃ³gica Ã© clara: **primeiro o aluno aprende a pensar visualmente em estÃ¡tico**, onde o feedback Ã© rÃ¡pido e o custo de iteraÃ§Ã£o Ã© baixo. **Depois leva o mesmo raciocÃ­nio para movimento**, onde o ritmo, o Ã¡udio e a ediÃ§Ã£o adicionam camadas. No final, produz uma campanha completa: landing page + pitch deck + vÃ­deo promo, tudo consistente no sistema de marca.

---

## PÃºblico-alvo

- Empreendedores e fundadores que precisam produzir materiais visuais profissionais sem contratar estÃºdio
- Estudantes de design, marketing digital e produÃ§Ã£o de conteÃºdo
- Automatizadores da AI Automation Society que querem fechar o ciclo "estratÃ©gia â†’ arte â†’ vÃ­deo" com IA
- Criadores de curso e edtechs que precisam de vÃ­deo-aulas com motion graphics

**NÃ£o Ã© para:** quem sÃ³ quer editar vÃ­deo em timeline tradicional (Premiere, CapCut). Este curso ensina um pipeline *programÃ¡tico* â€” HTML + GSAP â€” que permite iteraÃ§Ã£o determinÃ­stica e reuso de componentes.

---

## PrÃ©-requisitos

### TÃ©cnicos
- **Node 20+** instalado
- **FFmpeg** no PATH
- **Chrome** atualizado
- **~5 GB de disco livre**
- Conta em **claude.ai** (acesso ao Claude Design)
- Editor de cÃ³digo (**VS Code** recomendado)
- Git bÃ¡sico

### Conhecimento
- HTML/CSS bÃ¡sico (saber o que Ã© uma tag, uma classe, um seletor)
- JavaScript bÃ¡sico (saber ler um arquivo sem assustar)
- Terminal bÃ¡sico (`cd`, `ls`, `mkdir`)
- Sem conhecimento de motion graphics Ã© OK â€” o curso constrÃ³i isso do zero

### Opcional (recomendado)
- **Claude Code** instalado â€” desbloqueia as skills `/hyperframes`, `/design-designer`, `/gsap` automaticamente
- Conhecimento prÃ©vio de Figma ou Canva (ajuda a comparar com o fluxo Claude Design)

---

## Filosofia pedagÃ³gica

1. **Aprender pela engenharia reversa.** Todo mÃ³dulo comeÃ§a com um artefato finalizado (um `final.mp4`, uma landing page rendered). O aluno assiste â†’ abre o cÃ³digo â†’ modifica â†’ re-renderiza â†’ compara.
2. **Design antes de movimento.** EstÃ¡tico primeiro â€” porque ritmo e sincronia sÃ£o camadas sobre uma base visual que jÃ¡ precisa funcionar parada.
3. **Marca como sistema, nÃ£o decoraÃ§Ã£o.** O aluno constrÃ³i um `DESIGN.md` prÃ³prio no mÃ³dulo 2 e carrega ele por todo o curso.
4. **IteraÃ§Ã£o rÃ¡pida > perfeiÃ§Ã£o.** Draft render â†’ feedback â†’ re-render. Nunca um render "final" que nunca foi preview-ado ao vivo.
5. **MOTION_PHILOSOPHY.md Ã© a bÃ­blia.** Antes de qualquer brainstorm de vÃ­deo, lÃª-se as 10 Leis e o checklist prÃ©-voo.

---

## Estrutura do curso

### MÃ³dulo 0 â€” Setup e Fundamentos (2h)

**Objetivos:**
- Instalar e verificar o ambiente (`npx hyperframes doctor`)
- Clonar o repo `cchyperframes` e rodar o primeiro preview
- Entender a diferenÃ§a entre Claude Design (estÃ¡tico) e Hyperframes (vÃ­deo)
- VisÃ£o geral do que sÃ£o motion graphics, kinetic typography, shaders, GSAP

**Entregas:**
- Ambiente rodando com `npx hyperframes preview` num dos projetos
- Screenshot da Studio aberta em `may-shorts-19`
- Breve texto (1 parÃ¡grafo): em quais projetos reais vocÃª usarÃ¡ esse pipeline?

**Materiais:**
- README.md (seÃ§Ã£o "Como rodar os exemplos passo a passo")
- `npx hyperframes doctor`
- VÃ­deo introdutÃ³rio ao motion graphics (link externo sugerido)

---

### MÃ³dulo 1 â€” Claude Design: do briefing ao primeiro render (3h)

**Objetivos:**
- Dominar a skill `/design-designer` como ferramenta de estruturaÃ§Ã£o de briefing
- Entender o que Claude Design pede nos bastidores: feeling, audience, fidelity, option count, design system, brand context
- Gerar sua primeira landing page no claude.ai/design
- Usar o recurso **Tweaks** para iterar sem re-prompt

**Conceitos-chave:**
- Fidelidade: lo-fi vs hi-fi
- VariaÃ§Ãµes "safe to wild" (4 variaÃ§Ãµes padrÃ£o do Claude Design)
- Context imports: Figma, GitHub, screenshots â€” por que Claude Design pede
- Os 7 banimentos padrÃ£o: sem lorem ipsum, sem Ã­cones genÃ©ricos de startup de IA, sem referÃªncias a concorrentes

**ExercÃ­cio prÃ¡tico:**
1. Escolha um produto/serviÃ§o real (seu ou de cliente fictÃ­cio)
2. Rode o interview do `/design-designer` respondendo as 10 perguntas
3. Cole o prompt gerado no claude.ai/design
4. PeÃ§a 4 variaÃ§Ãµes (safe â†’ wild)
5. Escolha uma e itere com Tweaks (3 tweaks: cor, tipo, intensidade de motion)

**Entregas:**
- Screenshot das 4 variaÃ§Ãµes
- PNG ou link da versÃ£o final escolhida
- Breve reflexÃ£o: qual variaÃ§Ã£o ficou mais ousada? Por quÃª?

**Materiais:**
- Skill `/design-designer` (SKILL.md)
- Sistema de prompts do Claude Design (citado na skill)
- Site: https://claude.ai/design

---

### MÃ³dulo 2 â€” Construindo seu Sistema de Marca (2h)

**Objetivos:**
- Escrever seu prÃ³prio `DESIGN.md` (nÃ£o editar o `DESIGN.ais-example.md`)
- Definir: paleta de cores em hex, tipografia (headline + body), regras de motion, "o que NÃƒO fazer"
- Criar seu `assets/brand-tokens.css` com custom properties CSS
- Entender o acoplamento de marca: quais projetos do kit tÃªm AIS hardcoded (pesado) e quais sÃ£o neutros (mÃ­nimos)

**Conceitos-chave:**
- Design tokens: cores, fontes, espaÃ§amento, raios, sombras
- CSS custom properties (`--brand-primary`, `--brand-accent`, etc.)
- Por que Claude Design precisa de hex codes reais (nÃ£o "azul bonito")
- Varredura de find-and-fix: `grep -rEn` para caÃ§ar hardcoding antigo

**ExercÃ­cio prÃ¡tico:**
1. Leia `DESIGN.ais-example.md` como referÃªncia
2. Escreva seu prÃ³prio `DESIGN.md` com: paleta, tipografia, motion rules, banimentos
3. Crie `assets/brand-tokens.css` com suas custom properties
4. Teste: cole no Claude Design o hex da sua marca e peÃ§a uma nova landing page
5. Compare â€” ela respeitou o sistema?

**Entregas:**
- `DESIGN.md` da sua marca (mÃ­nimo 80 linhas)
- `brand-tokens.css` com ao menos 6 custom properties
- Nova landing page no Claude Design aplicando seu sistema

**Materiais:**
- `DESIGN.ais-example.md` (referÃªncia)
- `assets/brand-tokens.css` (exemplo AIS)
- README seÃ§Ã£o "Customizando para sua marca"

---

### MÃ³dulo 3 â€” MOTION_PHILOSOPHY: a estÃ©tica do movimento (3h)

**Objetivos:**
- Ler o `MOTION_PHILOSOPHY.md` completo â€” inclusive seÃ§Ãµes 0 (10 Leis) e 4 (checklist prÃ©-voo)
- Entender por que a mÃ©dia de cena Ã© 1.5s, fundo preto + grid + vinheta + grain, texto chrome-gradient com halo glow, transiÃ§Ãµes com motion blur
- Desconstruir o vÃ­deo-gold-standard (Infinite Global Payments 30s) frame a frame
- Aplicar as "7 regras mÃ­nimas" numa cena de teste

**Conceitos-chave:**
- As 10 Leis (seÃ§Ã£o 0 do MOTION_PHILOSOPHY)
- Regra dos trÃªs (sempre em trios: trÃªs beats, trÃªs cores, trÃªs cortes)
- Callback narrativo: o fim referencia o comeÃ§o
- Outro breathing (4â€“6s de respiro no final)
- "What Would Infinite Do?" â€” o teste de 10 perguntas antes de mostrar ao cliente

**ExercÃ­cio prÃ¡tico:**
1. Assista o `final.mp4` de `may-shorts-19` com o `MOTION_PHILOSOPHY.md` aberto ao lado
2. Identifique: onde aparece cada uma das 10 Leis? Anote timestamps
3. Rode o checklist prÃ©-voo contra o vÃ­deo
4. Agora crie 1 cena nova (6s) em HTML + GSAP aplicando as 7 regras mÃ­nimas

**Entregas:**
- AnotaÃ§Ã£o timestamp-a-timestamp do `may-shorts-19` com 10 Leis mapeadas
- Arquivo `minha-cena-teste.html` com uma cena de 6s renderizada
- Resposta ao "What Would Infinite Do?" (10 perguntas) sobre sua cena

**Materiais:**
- `MOTION_PHILOSOPHY.md` â€” leitura completa
- `video-projects/may-shorts-19/final.mp4`
- Skill `/hyperframes` (para sintaxe)

---

### MÃ³dulo 4 â€” Primeiro vÃ­deo completo (3h)

**Objetivos:**
- Clonar o projeto mais neutro (`claude-edit-intro`) e adaptÃ¡-lo para SUA marca
- Executar o loop completo: edit â†’ lint â†’ preview (Studio) â†’ draft render â†’ verify frames â†’ final render
- Usar o Contrato de Render (11 regras) sem quebrar nada
- Fazer a verificaÃ§Ã£o visual de frames antes de entregar

**Conceitos-chave:**
- As 11 regras do Render Contract (CLAUDE.md)
- `window.__timelines` â€” como cada composiÃ§Ã£o registra sua timeline GSAP
- `data-start`, `data-duration`, `data-track-index` â€” semÃ¢ntica de timing
- Sub-composiÃ§Ãµes via `<template>` + `data-composition-src`
- Por que `<video>` nunca leva `class="clip"` nem anima width/height diretamente

**ExercÃ­cio prÃ¡tico:**
1. `cd video-projects` e `cp -r claude-edit-intro meu-primeiro-video`
2. Rode `npx hyperframes preview` â€” veja funcionar como base
3. Troque: logo, cores (via brand-tokens.css), tipografia, texto dos tÃ­tulos
4. Rode `npx hyperframes lint` â€” conserte todos os erros
5. `npx hyperframes render --quality draft` â†’ verifique 3 frames com FFmpeg
6. `npx hyperframes render --quality standard` â€” entrega o `final.mp4`

**Entregas:**
- Projeto `meu-primeiro-video/` completo dentro de `video-projects/`
- `renders/final.mp4` rodando
- Screenshots de 3 frames-chave com a marca aplicada
- Auto-avaliaÃ§Ã£o: rodou o pre-flight do MOTION_PHILOSOPHY?

**Materiais:**
- CLAUDE.md (seÃ§Ãµes "Render Contract" e "Visual Verification")
- Skill `/hyperframes` e `/hyperframes-cli`
- Projeto base: `claude-edit-intro`

---

### MÃ³dulo 5 â€” Pitch Deck + VÃ­deo Sizzle (3h)

**Objetivos:**
- Criar um pitch deck de 7 slides no Claude Design usando seu sistema de marca
- Criar um sizzle reel de 15s no Hyperframes que vende o mesmo produto
- Entender como os dois outputs conversam: visual consistency entre estÃ¡tico e movimento
- Usar o fluxo `/website-to-hyperframes` para transformar sua landing page em base de vÃ­deo

**Conceitos-chave:**
- Pitch deck architecture: TÃ­tulo â†’ Problema â†’ Why Now â†’ O que fazemos â†’ TraÃ§Ã£o â†’ Time â†’ PrÃ³ximos passos
- Aspect ratio: 16:9 para deck, 16:9 ou 9:16 para sizzle
- Scroll-stop hook nos 2 primeiros segundos
- Callback visual: slide 1 e cena 1 do vÃ­deo compartilham uma motif

**ExercÃ­cio prÃ¡tico:**
1. Use `/design-designer` para gerar um prompt de pitch deck 7-slides
2. Rode no claude.ai/design e finalize
3. Extraia: palette, headline typeface, body typeface, um visual motif
4. Abra `video-projects/hyperframes-sizzle` como referÃªncia
5. Crie um novo projeto `sizzle-<seu-produto>/` e adapte
6. Inclua o motif do deck em pelo menos 1 cena do vÃ­deo
7. Render draft â†’ verify â†’ render standard

**Entregas:**
- PDF ou PNGs dos 7 slides
- `sizzle-<seu-produto>/renders/final.mp4` (15s)
- Documento curto: "como o deck conversa com o vÃ­deo?" (1 parÃ¡grafo)

**Materiais:**
- Skill `/website-to-hyperframes`
- `video-projects/hyperframes-sizzle/` (referÃªncia)
- Skill `/design-designer`

---

### MÃ³dulo 6 â€” Short-form vertical com talking-head (3h)

**Objetivos:**
- Produzir um short 9:16 estilo TikTok/Reels/Shorts com rosto + motion graphics sincronizado
- Usar a skill `/short-form-video` com o playbook do May Shorts 19
- Sincronizar legendas karaokÃª com transcriÃ§Ã£o automÃ¡tica (`npx hyperframes transcribe`)
- Gerar narraÃ§Ã£o on-device com TTS (`npx hyperframes tts`)

**Conceitos-chave:**
- Face-mode choreography: full-screen vs bottom-half
- Ãudio-sync scene timing: motion graphics colam em beats da fala
- Karaoke captions: cada palavra acende no timing correto
- As 10 regras de qualidade do `/short-form-video`

**ExercÃ­cio prÃ¡tico:**
1. Grave um talking-head de 30â€“45s em MP4 (celular serve)
2. Re-encode com FFmpeg: `ffmpeg -i raw.mov -c:v libx264 -crf 20 -c:a aac -movflags +faststart assets/clip.mp4`
3. `npx hyperframes transcribe assets/clip.mp4 --model small.en --json` â†’ timestamps por palavra
4. `cp -r may-shorts-19 meu-short` e adapte
5. Monte legendas karaokÃª sincronizadas
6. Adicione 3â€“5 cenas de motion graphics entre beats do discurso
7. Render draft â†’ frames verify â†’ render standard

**Entregas:**
- `meu-short/renders/final.mp4` (vertical 1080Ã—1920, 30â€“45s)
- Screenshots de 5 frames mostrando: talking-head, motion cena, legenda karaokÃª, call-to-action
- Auto-avaliaÃ§Ã£o: as 10 regras da skill foram respeitadas?

**Materiais:**
- Skill `/short-form-video`
- `video-projects/may-shorts-19/` (referÃªncia mÃ¡xima)
- Comandos: `npx hyperframes transcribe` e `npx hyperframes tts`

---

### MÃ³dulo 7 â€” Promo de produto SaaS 30â€“60s (4h)

**Objetivos:**
- Produzir um promo de produto SaaS no estilo Infinite Payments / Linear
- Usar intensivamente o catÃ¡logo do registry: `x-post`, `ui-3d-reveal`, `app-showcase`, shader transitions
- Aplicar o MOTION_PHILOSOPHY.md integralmente â€” esta Ã© a prova final da estÃ©tica
- Renderizar em qualidade `high` com `--docker` para output determinÃ­stico arquivÃ¡vel

**Conceitos-chave:**
- Estrutura tÃ­pica de SaaS promo: hook â†’ problema â†’ soluÃ§Ã£o (produto em aÃ§Ã£o) â†’ prova social â†’ CTA
- Uso de blocos do registry: quando um bloco pronto Ã© melhor que reinventar
- Shader transitions: `glitch`, `whip-pan`, `cARCKHÉtic-zoom`, `light-leak`, `sdf-iris`
- Kinetic typography: chrome gradient + halo glow + motion blur
- Outro breathing: hold de 4â€“6s com o logo + URL

**ExercÃ­cio prÃ¡tico:**
1. Escolha: `clickup-demo` (mais longo) ou `linear-promo-30s` (mais apertado) como base
2. Substitua o produto pelo seu
3. Instale 3+ blocos do catÃ¡logo que vocÃª nÃ£o usou ainda: `npx hyperframes add <name>`
4. Rode o pre-flight do MOTION_PHILOSOPHY **trÃªs vezes** durante a produÃ§Ã£o
5. Draft render â†’ preview gate com alguÃ©m que nunca viu o projeto
6. Final render em `--quality high --docker`

**Entregas:**
- Projeto completo em `video-projects/promo-<seu-produto>/`
- `renders/final-high.mp4` em qualidade archival
- Lista dos 3+ blocos do registry que vocÃª adicionou
- Resposta ao "What Would Infinite Do?" (10 perguntas) sobre o resultado

**Materiais:**
- `MOTION_PHILOSOPHY.md` (relÃª tudo)
- Skills `/hyperframes`, `/gsap`, `/hyperframes-registry`
- `video-projects/clickup-demo/` ou `linear-promo-30s/` (referÃªncias)

---

### MÃ³dulo 8 â€” Projeto Final Integrado (4h)

**Objetivos:**
- Produzir uma **campanha completa** para um produto/serviÃ§o (real ou ficcional) com 3 peÃ§as consistentes:
  1. **Landing page** (Claude Design)
  2. **Pitch deck** 7â€“10 slides (Claude Design)
  3. **VÃ­deo promo** 30â€“60s (Hyperframes)
- Garantir consistÃªncia visual e narrativa entre as 3 peÃ§as
- Publicar as peÃ§as: landing no Vercel, deck em PDF, vÃ­deo no YouTube ou social

**Rubrica de avaliaÃ§Ã£o (autoavaliaÃ§Ã£o):**

| CritÃ©rio | Pontos | O que significa |
|---|---|---|
| **Sistema de marca aplicado consistentemente** | 25 | Mesmas cores, mesma tipografia, mesmo motif visual nas 3 peÃ§as |
| **Narrativa coerente** | 20 | Landing â†’ Deck â†’ VÃ­deo contam a mesma histÃ³ria, cada um no seu formato |
| **Motion discipline** | 20 | Pre-flight do MOTION_PHILOSOPHY passou; nenhuma das 10 Leis quebrada |
| **Qualidade tÃ©cnica** | 15 | Lint zero erros; render em `standard`; nenhum frame quebrado |
| **Scroll-stop hook** | 10 | Primeiros 2s do vÃ­deo e primeira dobra da landing prendem atenÃ§Ã£o |
| **Callback narrativo** | 10 | Fim referencia inÃ­cio em pelo menos 2 peÃ§as |

**Entregas:**
- Link da landing page publicada
- PDF do pitch deck
- MP4 do vÃ­deo em qualidade `standard` (1080p lossless)
- Documento de 1 pÃ¡gina: "decisÃµes de design explicadas" â€” por que essa paleta, por que esse ritmo, por que esse hook
- Repo no GitHub com todos os arquivos (exceto `renders/` pesados, que ficam no gitignore)

**Materiais:**
- Tudo que foi aprendido nos mÃ³dulos 1â€“7
- Todas as skills relevantes: `/design-designer`, `/hyperframes`, `/short-form-video`, `/website-to-hyperframes`, `/gsap`, `/hyperframes-registry`, `/hyperframes-cli`
- CLAUDE.md completo (render contract + visual verification)

---

## Recursos e referÃªncias

### DocumentaÃ§Ã£o oficial
- Hyperframes: https://hyperframes.heygen.com (`llms.txt` para Ã­ndice completo)
- Claude Design: https://claude.ai/design (sem docs pÃºblicas; skill `/design-designer` resume o system prompt)
- GSAP: https://greensock.com/docs
- FFmpeg: https://ffmpeg.org/documentation.html

### Skills do Claude Code usadas no curso
| Skill | MÃ³dulos |
|---|---|
| `/design-designer` | 1, 2, 5, 8 |
| `/hyperframes` | 3â€“8 |
| `/hyperframes-cli` | 0, 4, 6, 7, 8 |
| `/gsap` | 3, 4, 7 |
| `/hyperframes-registry` | 5, 7, 8 |
| `/short-form-video` | 6, 8 |
| `/website-to-hyperframes` | 5, 8 |

### Projetos do kit usados como referÃªncia
| MÃ³dulo | Projeto de referÃªncia |
|---|---|
| 3 | `may-shorts-19` (gold standard curto) |
| 4 | `claude-edit-intro` (base neutra) |
| 5 | `hyperframes-sizzle` (sizzle reel) |
| 6 | `may-shorts-19` e `may-shorts-18` (shorts verticais) |
| 7 | `clickup-demo`, `linear-promo-30s` (promos SaaS) |
| 8 | qualquer combinaÃ§Ã£o â€” Ã© projeto original |

### Leituras obrigatÃ³rias (por ordem)
1. `README.md` (este repo)
2. `CLAUDE.md` â€” especialmente seÃ§Ãµes "Render Contract" e "Visual Verification"
3. `MOTION_PHILOSOPHY.md` â€” integral
4. `DESIGN.ais-example.md` â€” como exemplo para escrever o seu
5. Skill `/design-designer` (SKILL.md) â€” entender a mente do Claude Design

---

## Formato de entrega e suporte

**Modalidade sugerida:** cohort de 4â€“8 semanas com encontros semanais de 90min + trabalho autodirigido nos mÃ³dulos.

**Ferramentas de suporte:**
- Discord ou Slack da turma para revisÃµes entre pares
- Office hours semanais com o instrutor (1h)
- GitHub Classroom para entregas (cada aluno tem fork do kit)
- Reviews cruzadas: cada aluno avalia 2 projetos de colegas por mÃ³dulo

**CertificaÃ§Ã£o (opcional):**
Aluno que entregar os 8 projetos (M0â€“M8) com nota â‰¥70 na rubrica do M8 recebe certificado de conclusÃ£o.

---

## PrÃ³ximos passos apÃ³s o curso

- **NÃ­vel avanÃ§ado:** estudar os projetos AIS pesados (`aisoc-hype`, `aisoc-app-release`, `golden-ratio-demo`) e reconstruir um do zero para sua marca
- **ProduÃ§Ã£o em escala:** montar pipeline com `hyperframes producer` para renders em batch via API
- **IntegraÃ§Ã£o com n8n/ClickUp:** automatizar geraÃ§Ã£o de briefings + renders via webhook (ver skills `/n8n-*`)
- **FormaÃ§Ã£o de instrutor:** pegar este plano e adaptar para seu prÃ³prio pÃºblico

---

*Plano construÃ­do combinando o conteÃºdo do `cchyperframes` (Hyperframes Student Kit) com a skill `design-designer` para Claude Design (claude.ai/design). IterÃ¡vel â€” contribuiÃ§Ãµes e ajustes bem-vindos.*
