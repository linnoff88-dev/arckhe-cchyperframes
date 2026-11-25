# Plano de Curso ê¢â¬â Design + VêÂ­deo com IA

**Combinando Claude Design (claude.ai/design) + Hyperframes Student Kit**
**DuraêÂ§êÂ£o estimada:** 8 mêÂ³dulos êâ 2ê¢â¬â3h = 20ê¢â¬â24h de estudo ativo
**Formato:** autodirigido com projetos prêÂ¡ticos progressivos
**Idioma:** PortuguêÂªs (BR)
**Data do plano:** 2026-04-19

---

## VisêÂ£o geral

Este curso ensina a produêÂ§êÂ£o visual ponta-a-ponta com IA ê¢â¬â do briefing estêÂ¡tico (landing page, deck, protêÂ³tipo) ao vêÂ­deo motion-graphics finalizado ê¢â¬â integrando duas ferramentas complementares:

1. **Claude Design** (claude.ai/design) ê¢â¬â gera designs estêÂ¡ticos ship-ready: landing pages, pitch decks, scroll-driven sites, protêÂ³tipos clicêÂ¡veis de app.
2. **Hyperframes Student Kit** (cchyperframes) ê¢â¬â pipeline de vêÂ­deo em HTML + GSAP com 12 projetos finalizados para engenharia reversa (short-form TikTok, promos SaaS, aulas educacionais, hype films de marca).

A lêÂ³gica êÂ© clara: **primeiro o aluno aprende a pensar visualmente em estêÂ¡tico**, onde o feedback êÂ© rêÂ¡pido e o custo de iteraêÂ§êÂ£o êÂ© baixo. **Depois leva o mesmo raciocêÂ­nio para movimento**, onde o ritmo, o êÂ¡udio e a ediêÂ§êÂ£o adicionam camadas. No final, produz uma campanha completa: landing page + pitch deck + vêÂ­deo promo, tudo consistente no sistema de marca.

---

## PêÂºblico-alvo

- Empreendedores e fundadores que precisam produzir materiais visuais profissionais sem contratar estêÂºdio
- Estudantes de design, marketing digital e produêÂ§êÂ£o de conteêÂºdo
- Automatizadores da AI Automation Society que querem fechar o ciclo "estratêÂ©gia ê¢â â arte ê¢â â vêÂ­deo" com IA
- Criadores de curso e edtechs que precisam de vêÂ­deo-aulas com motion graphics

**NêÂ£o êÂ© para:** quem sêÂ³ quer editar vêÂ­deo em timeline tradicional (Premiere, CapCut). Este curso ensina um pipeline *programêÂ¡tico* ê¢â¬â HTML + GSAP ê¢â¬â que permite iteraêÂ§êÂ£o determinêÂ­stica e reuso de componentes.

---

## PrêÂ©-requisitos

### TêÂ©cnicos
- **Node 20+** instalado
- **FFmpeg** no PATH
- **Chrome** atualizado
- **~5 GB de disco livre**
- Conta em **claude.ai** (acesso ao Claude Design)
- Editor de cêÂ³digo (**VS Code** recomendado)
- Git bêÂ¡sico

### Conhecimento
- HTML/CSS bêÂ¡sico (saber o que êÂ© uma tag, uma classe, um seletor)
- JavaScript bêÂ¡sico (saber ler um arquivo sem assustar)
- Terminal bêÂ¡sico (`cd`, `ls`, `mkdir`)
- Sem conhecimento de motion graphics êÂ© OK ê¢â¬â o curso constrêÂ³i isso do zero

### Opcional (recomendado)
- **Claude Code** instalado ê¢â¬â desbloqueia as skills `/hyperframes`, `/design-designer`, `/gsap` automaticamente
- Conhecimento prêÂ©vio de Figma ou Canva (ajuda a comparar com o fluxo Claude Design)

---

## Filosofia pedagêÂ³gica

1. **Aprender pela engenharia reversa.** Todo mêÂ³dulo comeêÂ§a com um artefato finalizado (um `final.mp4`, uma landing page rendered). O aluno assiste ê¢â â abre o cêÂ³digo ê¢â â modifica ê¢â â re-renderiza ê¢â â compara.
2. **Design antes de movimento.** EstêÂ¡tico primeiro ê¢â¬â porque ritmo e sincronia sêÂ£o camadas sobre uma base visual que jêÂ¡ precisa funcionar parada.
3. **Marca como sistema, nêÂ£o decoraêÂ§êÂ£o.** O aluno constrêÂ³i um `DESIGN.md` prêÂ³prio no mêÂ³dulo 2 e carrega ele por todo o curso.
4. **IteraêÂ§êÂ£o rêÂ¡pida > perfeiêÂ§êÂ£o.** Draft render ê¢â â feedback ê¢â â re-render. Nunca um render "final" que nunca foi preview-ado ao vivo.
5. **MOTION_PHILOSOPHY.md êÂ© a bêÂ­blia.** Antes de qualquer brainstorm de vêÂ­deo, lêÂª-se as 10 Leis e o checklist prêÂ©-voo.

---

## Estrutura do curso

### MêÂ³dulo 0 ê¢â¬â Setup e Fundamentos (2h)

**Objetivos:**
- Instalar e verificar o ambiente (`npx hyperframes doctor`)
- Clonar o repo `cchyperframes` e rodar o primeiro preview
- Entender a diferenêÂ§a entre Claude Design (estêÂ¡tico) e Hyperframes (vêÂ­deo)
- VisêÂ£o geral do que sêÂ£o motion graphics, kinetic typography, shaders, GSAP

**Entregas:**
- Ambiente rodando com `npx hyperframes preview` num dos projetos
- Screenshot da Studio aberta em `may-shorts-19`
- Breve texto (1 parêÂ¡grafo): em quais projetos reais vocêÂª usarêÂ¡ esse pipeline?

**Materiais:**
- README.md (seêÂ§êÂ£o "Como rodar os exemplos passo a passo")
- `npx hyperframes doctor`
- VêÂ­deo introdutêÂ³rio ao motion graphics (link externo sugerido)

---

### MêÂ³dulo 1 ê¢â¬â Claude Design: do briefing ao primeiro render (3h)

**Objetivos:**
- Dominar a skill `/design-designer` como ferramenta de estruturaêÂ§êÂ£o de briefing
- Entender o que Claude Design pede nos bastidores: feeling, audience, fidelity, option count, design system, brand context
- Gerar sua primeira landing page no claude.ai/design
- Usar o recurso **Tweaks** para iterar sem re-prompt

**Conceitos-chave:**
- Fidelidade: lo-fi vs hi-fi
- VariaêÂ§êÂµes "safe to wild" (4 variaêÂ§êÂµes padrêÂ£o do Claude Design)
- Context imports: Figma, GitHub, screenshots ê¢â¬â por que Claude Design pede
- Os 7 banimentos padrêÂ£o: sem lorem ipsum, sem êÂ­cones genêÂ©ricos de startup de IA, sem referêÂªncias a concorrentes

**ExercêÂ­cio prêÂ¡tico:**
1. Escolha um produto/serviêÂ§o real (seu ou de cliente fictêÂ­cio)
2. Rode o interview do `/design-designer` respondendo as 10 perguntas
3. Cole o prompt gerado no claude.ai/design
4. PeêÂ§a 4 variaêÂ§êÂµes (safe ê¢â â wild)
5. Escolha uma e itere com Tweaks (3 tweaks: cor, tipo, intensidade de motion)

**Entregas:**
- Screenshot das 4 variaêÂ§êÂµes
- PNG ou link da versêÂ£o final escolhida
- Breve reflexêÂ£o: qual variaêÂ§êÂ£o ficou mais ousada? Por quêÂª?

**Materiais:**
- Skill `/design-designer` (SKILL.md)
- Sistema de prompts do Claude Design (citado na skill)
- Site: https://claude.ai/design

---

### MêÂ³dulo 2 ê¢â¬â Construindo seu Sistema de Marca (2h)

**Objetivos:**
- Escrever seu prêÂ³prio `DESIGN.md` (nêÂ£o editar o `DESIGN.ais-example.md`)
- Definir: paleta de cores em hex, tipografia (headline + body), regras de motion, "o que NêÆO fazer"
- Criar seu `assets/brand-tokens.css` com custom properties CSS
- Entender o acoplamento de marca: quais projetos do kit têÂªm AIS hardcoded (pesado) e quais sêÂ£o neutros (mêÂ­nimos)

**Conceitos-chave:**
- Design tokens: cores, fontes, espaêÂ§amento, raios, sombras
- CSS custom properties (`--brand-primary`, `--brand-accent`, etc.)
- Por que Claude Design precisa de hex codes reais (nêÂ£o "azul bonito")
- Varredura de find-and-fix: `grep -rEn` para caêÂ§ar hardcoding antigo

**ExercêÂ­cio prêÂ¡tico:**
1. Leia `DESIGN.ais-example.md` como referêÂªncia
2. Escreva seu prêÂ³prio `DESIGN.md` com: paleta, tipografia, motion rules, banimentos
3. Crie `assets/brand-tokens.css` com suas custom properties
4. Teste: cole no Claude Design o hex da sua marca e peêÂ§a uma nova landing page
5. Compare ê¢â¬â ela respeitou o sistema?

**Entregas:**
- `DESIGN.md` da sua marca (mêÂ­nimo 80 linhas)
- `brand-tokens.css` com ao menos 6 custom properties
- Nova landing page no Claude Design aplicando seu sistema

**Materiais:**
- `DESIGN.ais-example.md` (referêÂªncia)
- `assets/brand-tokens.css` (exemplo AIS)
- README seêÂ§êÂ£o "Customizando para sua marca"

---

### MêÂ³dulo 3 ê¢â¬â MOTION_PHILOSOPHY: a estêÂ©tica do movimento (3h)

**Objetivos:**
- Ler o `MOTION_PHILOSOPHY.md` completo ê¢â¬â inclusive seêÂ§êÂµes 0 (10 Leis) e 4 (checklist prêÂ©-voo)
- Entender por que a mêÂ©dia de cena êÂ© 1.5s, fundo preto + grid + vinheta + grain, texto chrome-gradient com halo glow, transiêÂ§êÂµes com motion blur
- Desconstruir o vêÂ­deo-gold-standard (Infinite Global Payments 30s) frame a frame
- Aplicar as "7 regras mêÂ­nimas" numa cena de teste

**Conceitos-chave:**
- As 10 Leis (seêÂ§êÂ£o 0 do MOTION_PHILOSOPHY)
- Regra dos trêÂªs (sempre em trios: trêÂªs beats, trêÂªs cores, trêÂªs cortes)
- Callback narrativo: o fim referencia o comeêÂ§o
- Outro breathing (4ê¢â¬â6s de respiro no final)
- "What Would Infinite Do?" ê¢â¬â o teste de 10 perguntas antes de mostrar ao cliente

**ExercêÂ­cio prêÂ¡tico:**
1. Assista o `final.mp4` de `may-shorts-19` com o `MOTION_PHILOSOPHY.md` aberto ao lado
2. Identifique: onde aparece cada uma das 10 Leis? Anote timestamps
3. Rode o checklist prêÂ©-voo contra o vêÂ­deo
4. Agora crie 1 cena nova (6s) em HTML + GSAP aplicando as 7 regras mêÂ­nimas

**Entregas:**
- AnotaêÂ§êÂ£o timestamp-a-timestamp do `may-shorts-19` com 10 Leis mapeadas
- Arquivo `minha-cena-teste.html` com uma cena de 6s renderizada
- Resposta ao "What Would Infinite Do?" (10 perguntas) sobre sua cena

**Materiais:**
- `MOTION_PHILOSOPHY.md` ê¢â¬â leitura completa
- `video-projects/may-shorts-19/final.mp4`
- Skill `/hyperframes` (para sintaxe)

---

### MêÂ³dulo 4 ê¢â¬â Primeiro vêÂ­deo completo (3h)

**Objetivos:**
- Clonar o projeto mais neutro (`claude-edit-intro`) e adaptêÂ¡-lo para SUA marca
- Executar o loop completo: edit ê¢â â lint ê¢â â preview (Studio) ê¢â â draft render ê¢â â verify frames ê¢â â final render
- Usar o Contrato de Render (11 regras) sem quebrar nada
- Fazer a verificaêÂ§êÂ£o visual de frames antes de entregar

**Conceitos-chave:**
- As 11 regras do Render Contract (CLAUDE.md)
- `window.__timelines` ê¢â¬â como cada composiêÂ§êÂ£o registra sua timeline GSAP
- `data-start`, `data-duration`, `data-track-index` ê¢â¬â semêÂ¢ntica de timing
- Sub-composiêÂ§êÂµes via `<template>` + `data-composition-src`
- Por que `<video>` nunca leva `class="clip"` nem anima width/height diretamente

**ExercêÂ­cio prêÂ¡tico:**
1. `cd video-projects` e `cp -r claude-edit-intro meu-primeiro-video`
2. Rode `npx hyperframes preview` ê¢â¬â veja funcionar como base
3. Troque: logo, cores (via brand-tokens.css), tipografia, texto dos têÂ­tulos
4. Rode `npx hyperframes lint` ê¢â¬â conserte todos os erros
5. `npx hyperframes render --quality draft` ê¢â â verifique 3 frames com FFmpeg
6. `npx hyperframes render --quality standard` ê¢â¬â entrega o `final.mp4`

**Entregas:**
- Projeto `meu-primeiro-video/` completo dentro de `video-projects/`
- `renders/final.mp4` rodando
- Screenshots de 3 frames-chave com a marca aplicada
- Auto-avaliaêÂ§êÂ£o: rodou o pre-flight do MOTION_PHILOSOPHY?

**Materiais:**
- CLAUDE.md (seêÂ§êÂµes "Render Contract" e "Visual Verification")
- Skill `/hyperframes` e `/hyperframes-cli`
- Projeto base: `claude-edit-intro`

---

### MêÂ³dulo 5 ê¢â¬â Pitch Deck + VêÂ­deo Sizzle (3h)

**Objetivos:**
- Criar um pitch deck de 7 slides no Claude Design usando seu sistema de marca
- Criar um sizzle reel de 15s no Hyperframes que vende o mesmo produto
- Entender como os dois outputs conversam: visual consistency entre estêÂ¡tico e movimento
- Usar o fluxo `/website-to-hyperframes` para transformar sua landing page em base de vêÂ­deo

**Conceitos-chave:**
- Pitch deck architecture: TêÂ­tulo ê¢â â Problema ê¢â â Why Now ê¢â â O que fazemos ê¢â â TraêÂ§êÂ£o ê¢â â Time ê¢â â PrêÂ³ximos passos
- Aspect ratio: 16:9 para deck, 16:9 ou 9:16 para sizzle
- Scroll-stop hook nos 2 primeiros segundos
- Callback visual: slide 1 e cena 1 do vêÂ­deo compartilham uma motif

**ExercêÂ­cio prêÂ¡tico:**
1. Use `/design-designer` para gerar um prompt de pitch deck 7-slides
2. Rode no claude.ai/design e finalize
3. Extraia: palette, headline typeface, body typeface, um visual motif
4. Abra `video-projects/hyperframes-sizzle` como referêÂªncia
5. Crie um novo projeto `sizzle-<seu-produto>/` e adapte
6. Inclua o motif do deck em pelo menos 1 cena do vêÂ­deo
7. Render draft ê¢â â verify ê¢â â render standard

**Entregas:**
- PDF ou PNGs dos 7 slides
- `sizzle-<seu-produto>/renders/final.mp4` (15s)
- Documento curto: "como o deck conversa com o vêÂ­deo?" (1 parêÂ¡grafo)

**Materiais:**
- Skill `/website-to-hyperframes`
- `video-projects/hyperframes-sizzle/` (referêÂªncia)
- Skill `/design-designer`

---

### MêÂ³dulo 6 ê¢â¬â Short-form vertical com talking-head (3h)

**Objetivos:**
- Produzir um short 9:16 estilo TikTok/Reels/Shorts com rosto + motion graphics sincronizado
- Usar a skill `/short-form-video` com o playbook do May Shorts 19
- Sincronizar legendas karaokêÂª com transcriêÂ§êÂ£o automêÂ¡tica (`npx hyperframes transcribe`)
- Gerar narraêÂ§êÂ£o on-device com TTS (`npx hyperframes tts`)

**Conceitos-chave:**
- Face-mode choreography: full-screen vs bottom-half
- êÂudio-sync scene timing: motion graphics colam em beats da fala
- Karaoke captions: cada palavra acende no timing correto
- As 10 regras de qualidade do `/short-form-video`

**ExercêÂ­cio prêÂ¡tico:**
1. Grave um talking-head de 30ê¢â¬â45s em MP4 (celular serve)
2. Re-encode com FFmpeg: `ffmpeg -i raw.mov -c:v libx264 -crf 20 -c:a aac -movflags +faststart assets/clip.mp4`
3. `npx hyperframes transcribe assets/clip.mp4 --model small.en --json` ê¢â â timestamps por palavra
4. `cp -r may-shorts-19 meu-short` e adapte
5. Monte legendas karaokêÂª sincronizadas
6. Adicione 3ê¢â¬â5 cenas de motion graphics entre beats do discurso
7. Render draft ê¢â â frames verify ê¢â â render standard

**Entregas:**
- `meu-short/renders/final.mp4` (vertical 1080êâ1920, 30ê¢â¬â45s)
- Screenshots de 5 frames mostrando: talking-head, motion cena, legenda karaokêÂª, call-to-action
- Auto-avaliaêÂ§êÂ£o: as 10 regras da skill foram respeitadas?

**Materiais:**
- Skill `/short-form-video`
- `video-projects/may-shorts-19/` (referêÂªncia mêÂ¡xima)
- Comandos: `npx hyperframes transcribe` e `npx hyperframes tts`

---

### MêÂ³dulo 7 ê¢â¬â Promo de produto SaaS 30ê¢â¬â60s (4h)

**Objetivos:**
- Produzir um promo de produto SaaS no estilo Infinite Payments / Linear
- Usar intensivamente o catêÂ¡logo do registry: `x-post`, `ui-3d-reveal`, `app-showcase`, shader transitions
- Aplicar o MOTION_PHILOSOPHY.md integralmente ê¢â¬â esta êÂ© a prova final da estêÂ©tica
- Renderizar em qualidade `high` com `--docker` para output determinêÂ­stico arquivêÂ¡vel

**Conceitos-chave:**
- Estrutura têÂ­pica de SaaS promo: hook ê¢â â problema ê¢â â soluêÂ§êÂ£o (produto em aêÂ§êÂ£o) ê¢â â prova social ê¢â â CTA
- Uso de blocos do registry: quando um bloco pronto êÂ© melhor que reinventar
- Shader transitions: `glitch`, `whip-pan`, `cARCKHêtic-zoom`, `light-leak`, `sdf-iris`
- Kinetic typography: chrome gradient + halo glow + motion blur
- Outro breathing: hold de 4ê¢â¬â6s com o logo + URL

**ExercêÂ­cio prêÂ¡tico:**
1. Escolha: `clickup-demo` (mais longo) ou `linear-promo-30s` (mais apertado) como base
2. Substitua o produto pelo seu
3. Instale 3+ blocos do catêÂ¡logo que vocêÂª nêÂ£o usou ainda: `npx hyperframes add <name>`
4. Rode o pre-flight do MOTION_PHILOSOPHY **trêÂªs vezes** durante a produêÂ§êÂ£o
5. Draft render ê¢â â preview gate com alguêÂ©m que nunca viu o projeto
6. Final render em `--quality high --docker`

**Entregas:**
- Projeto completo em `video-projects/promo-<seu-produto>/`
- `renders/final-high.mp4` em qualidade archival
- Lista dos 3+ blocos do registry que vocêÂª adicionou
- Resposta ao "What Would Infinite Do?" (10 perguntas) sobre o resultado

**Materiais:**
- `MOTION_PHILOSOPHY.md` (relêÂª tudo)
- Skills `/hyperframes`, `/gsap`, `/hyperframes-registry`
- `video-projects/clickup-demo/` ou `linear-promo-30s/` (referêÂªncias)

---

### MêÂ³dulo 8 ê¢â¬â Projeto Final Integrado (4h)

**Objetivos:**
- Produzir uma **campanha completa** para um produto/serviêÂ§o (real ou ficcional) com 3 peêÂ§as consistentes:
  1. **Landing page** (Claude Design)
  2. **Pitch deck** 7ê¢â¬â10 slides (Claude Design)
  3. **VêÂ­deo promo** 30ê¢â¬â60s (Hyperframes)
- Garantir consistêÂªncia visual e narrativa entre as 3 peêÂ§as
- Publicar as peêÂ§as: landing no Vercel, deck em PDF, vêÂ­deo no YouTube ou social

**Rubrica de avaliaêÂ§êÂ£o (autoavaliaêÂ§êÂ£o):**

| CritêÂ©rio | Pontos | O que significa |
|---|---|---|
| **Sistema de marca aplicado consistentemente** | 25 | Mesmas cores, mesma tipografia, mesmo motif visual nas 3 peêÂ§as |
| **Narrativa coerente** | 20 | Landing ê¢â â Deck ê¢â â VêÂ­deo contam a mesma histêÂ³ria, cada um no seu formato |
| **Motion discipline** | 20 | Pre-flight do MOTION_PHILOSOPHY passou; nenhuma das 10 Leis quebrada |
| **Qualidade têÂ©cnica** | 15 | Lint zero erros; render em `standard`; nenhum frame quebrado |
| **Scroll-stop hook** | 10 | Primeiros 2s do vêÂ­deo e primeira dobra da landing prendem atenêÂ§êÂ£o |
| **Callback narrativo** | 10 | Fim referencia inêÂ­cio em pelo menos 2 peêÂ§as |

**Entregas:**
- Link da landing page publicada
- PDF do pitch deck
- MP4 do vêÂ­deo em qualidade `standard` (1080p lossless)
- Documento de 1 pêÂ¡gina: "decisêÂµes de design explicadas" ê¢â¬â por que essa paleta, por que esse ritmo, por que esse hook
- Repo no GitHub com todos os arquivos (exceto `renders/` pesados, que ficam no gitignore)

**Materiais:**
- Tudo que foi aprendido nos mêÂ³dulos 1ê¢â¬â7
- Todas as skills relevantes: `/design-designer`, `/hyperframes`, `/short-form-video`, `/website-to-hyperframes`, `/gsap`, `/hyperframes-registry`, `/hyperframes-cli`
- CLAUDE.md completo (render contract + visual verification)

---

## Recursos e referêÂªncias

### DocumentaêÂ§êÂ£o oficial
- Hyperframes: https://hyperframes.heygen.com (`llms.txt` para êÂ­ndice completo)
- Claude Design: https://claude.ai/design (sem docs pêÂºblicas; skill `/design-designer` resume o system prompt)
- GSAP: https://greensock.com/docs
- FFmpeg: https://ffmpeg.org/documentation.html

### Skills do Claude Code usadas no curso
| Skill | MêÂ³dulos |
|---|---|
| `/design-designer` | 1, 2, 5, 8 |
| `/hyperframes` | 3ê¢â¬â8 |
| `/hyperframes-cli` | 0, 4, 6, 7, 8 |
| `/gsap` | 3, 4, 7 |
| `/hyperframes-registry` | 5, 7, 8 |
| `/short-form-video` | 6, 8 |
| `/website-to-hyperframes` | 5, 8 |

### Projetos do kit usados como referêÂªncia
| MêÂ³dulo | Projeto de referêÂªncia |
|---|---|
| 3 | `may-shorts-19` (gold standard curto) |
| 4 | `claude-edit-intro` (base neutra) |
| 5 | `hyperframes-sizzle` (sizzle reel) |
| 6 | `may-shorts-19` e `may-shorts-18` (shorts verticais) |
| 7 | `clickup-demo`, `linear-promo-30s` (promos SaaS) |
| 8 | qualquer combinaêÂ§êÂ£o ê¢â¬â êÂ© projeto original |

### Leituras obrigatêÂ³rias (por ordem)
1. `README.md` (este repo)
2. `CLAUDE.md` ê¢â¬â especialmente seêÂ§êÂµes "Render Contract" e "Visual Verification"
3. `MOTION_PHILOSOPHY.md` ê¢â¬â integral
4. `DESIGN.ais-example.md` ê¢â¬â como exemplo para escrever o seu
5. Skill `/design-designer` (SKILL.md) ê¢â¬â entender a mente do Claude Design

---

## Formato de entrega e suporte

**Modalidade sugerida:** cohort de 4ê¢â¬â8 semanas com encontros semanais de 90min + trabalho autodirigido nos mêÂ³dulos.

**Ferramentas de suporte:**
- Discord ou Slack da turma para revisêÂµes entre pares
- Office hours semanais com o instrutor (1h)
- GitHub Classroom para entregas (cada aluno tem fork do kit)
- Reviews cruzadas: cada aluno avalia 2 projetos de colegas por mêÂ³dulo

**CertificaêÂ§êÂ£o (opcional):**
Aluno que entregar os 8 projetos (M0ê¢â¬âM8) com nota ê¢â°Â¥70 na rubrica do M8 recebe certificado de conclusêÂ£o.

---

## PrêÂ³ximos passos apêÂ³s o curso

- **NêÂ­vel avanêÂ§ado:** estudar os projetos AIS pesados (`aisoc-hype`, `aisoc-app-release`, `golden-ratio-demo`) e reconstruir um do zero para sua marca
- **ProduêÂ§êÂ£o em escala:** montar pipeline com `hyperframes producer` para renders em batch via API
- **IntegraêÂ§êÂ£o com n8n/ClickUp:** automatizar geraêÂ§êÂ£o de briefings + renders via webhook (ver skills `/n8n-*`)
- **FormaêÂ§êÂ£o de instrutor:** pegar este plano e adaptar para seu prêÂ³prio pêÂºblico

---

*Plano construêÂ­do combinando o conteêÂºdo do `cchyperframes` (Hyperframes Student Kit) com a skill `design-designer` para Claude Design (claude.ai/design). IterêÂ¡vel ê¢â¬â contribuiêÂ§êÂµes e ajustes bem-vindos.*
