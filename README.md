# Hyperframes Editor â€” EdiÃ§Ã£o Estudante

<div align="center">
  <img src="capa/logo.svg" alt="Arckhé AI" height="48" />
  <p><strong>Arckhé AI</strong></p>
</div>


Uma bancada de trabalho para construir pipelines de vÃ­deo motion-graphics em **HTML + GSAP puros**, alimentada pelo [Hyperframes](https://hyperframes.heygen.com). Doze projetos de vÃ­deo finalizados que vocÃª pode clonar, varrer a timeline, destrinchar e reconstruir como seus.

> Isto **nÃ£o** Ã© um stack de vÃ­deo Remotion / React / Next.js. Cada composiÃ§Ã£o neste repositÃ³rio Ã© um arquivo HTML comum com uma timeline GSAP pausada anexada a `window.__timelines`. A CLI do Hyperframes cuida de lint, preview e render.

---

## Para quem Ã© isso

Estudantes que querem aprender como vÃ­deos promocionais e short-form profissionais sÃ£o construÃ­dos de ponta a ponta â€” storyboard, sistema de marca, motion graphics, sincronia de Ã¡udio, pipeline de render â€” atravÃ©s de engenharia reversa de projetos reais. Todo projeto aqui entregou (ou quase entregou). Varra as composiÃ§Ãµes, leia os docs de HANDOFF/STORYBOARD, assista ao `final.mp4`, depois mude coisas e veja o que quebra.

## PrÃ©-requisitos

- **Node 20+** â€” rode `node --version` para verificar
- **FFmpeg** no seu `PATH` â€” necessÃ¡rio para extraÃ§Ã£o e reencode de Ã¡udio
- **Chrome (mais recente)** â€” Hyperframes renderiza via Chromium headless
- **~5 GB de disco livre** â€” node_modules Ã© grande; renders sÃ£o maiores ainda
- **16 GB de RAM recomendado** para preview fluido no Studio com mÃºltiplos blocos de shader

Rode `npx hyperframes doctor` apÃ³s `npm install` â€” ele reporta o que estÃ¡ faltando.

## InÃ­cio rÃ¡pido

```bash
git clone <url-do-seu-fork> hyperframes-editor
cd hyperframes-editor
npm install

# Opcional â€” apenas se quiser usar as integraÃ§Ãµes ClickUp / OpenAI
cp .env.example .env
# ...depois edite .env com suas prÃ³prias chaves

# Abra o Studio em um dos projetos inclusos
cd video-projects/may-shorts-19
npx hyperframes preview    # http://localhost:3002
```

O Studio recarrega automaticamente ao salvar o arquivo. Varra a timeline, inspecione cenas, mude cores, veja re-renderizar ao vivo.

## Como rodar os exemplos passo a passo

Guia prÃ¡tico para quem estÃ¡ comeÃ§ando do zero com o Hyperframes.

### 1. Instalar dependÃªncias (uma vez sÃ³, na raiz)

```bash
cd cchyperframes
npm install
```

### 2. Verificar o ambiente

Confirma se Node 20+, FFmpeg e Chrome estÃ£o instalados e acessÃ­veis:

```bash
npx hyperframes doctor
```

### 3. Entrar num projeto

Cada pasta em `video-projects/` Ã© um projeto independente com seu prÃ³prio `index.html`, `assets/` e `compositions/`.

```bash
cd video-projects/may-shorts-19      # ou qualquer outro projeto
```

### 4. Preview ao vivo no Studio (hot reload)

```bash
npx hyperframes preview              # abre http://localhost:3002
```

O Studio recarrega automaticamente ao salvar qualquer arquivo. Varra a timeline, mude cores, teste animaÃ§Ãµes em tempo real.

### 5. Lint antes de renderizar

```bash
npx hyperframes lint
```

Zero erros antes de partir para o render. Warnings vocÃª pode sobreviver com.

### 6. Render rÃ¡pido de rascunho (1â€“3 min, pixelado)

```bash
npx hyperframes render --quality draft --output renders/draft.mp4
```

Use para validaÃ§Ã£o rÃ¡pida de pacing e sincronia.

### 7. Render final (1080p visualmente lossless)

```bash
npx hyperframes render --quality standard --output renders/final.mp4
```

Este Ã© o render que se entrega.

### Por onde comeÃ§ar (ordem recomendada)

| NÃ­vel | Projeto | Por quÃª |
|---|---|---|
| **Iniciante** | `claude-edit-intro` | Intro estilo promo com mÃ­nimo hardcoding de marca â€” template inicial fÃ¡cil de entender. |
| **Polido** | `may-shorts-19` | Vertical TikTok com talking-head + motion graphics + legendas karaokÃª. A skill `/short-form-video` foi escrita em torno dele. |
| **Produto SaaS** | `clickup-demo` | Demo de 60s com uso pesado de blocos do registry (x-post, ui-3d-reveal). Mostra a curva de iteraÃ§Ã£o. |
| **Motion avanÃ§ado** | `linear-promo-30s` | Promo de 30s na estÃ©tica Infinite Payments. Entregue como draft â€” terminÃ¡-lo Ã© um bom exercÃ­cio. |

Abra o `final.mp4` de cada projeto primeiro para ver o alvo, depois o `index.html` lado a lado para entender como foi construÃ­do.

### Dicas importantes

- **Sempre rode os comandos de dentro da pasta do projeto** (nÃ£o da raiz do workspace). A CLI lÃª `hyperframes.json` e `meta.json` do diretÃ³rio atual.
- **Leia `MOTION_PHILOSOPHY.md`** antes de brainstormar sua primeira cena â€” as 10 Leis (seÃ§Ã£o 0) e o checklist prÃ©-voo (seÃ§Ã£o 4) sÃ£o o que separa "renderizou" de "estÃ¡ bom".
- **Se o Studio travar em 0s**, force refresh no navegador (Ctrl+Shift+R) ou abra uma sub-composiÃ§Ã£o especÃ­fica: `http://localhost:3002/?comp=<sub-comp-id>`.
- **Se um render falhar no meio**, rode `npx hyperframes doctor` para ver o que estÃ¡ faltando.

## Estrutura do repositÃ³rio

```
hyperframes-editor/
â”œâ”€â”€ README.md                    â† vocÃª estÃ¡ aqui
â”œâ”€â”€ LICENSE                      â† MIT (veja nota sobre assets de marca)
â”œâ”€â”€ .env.example                 â† copie para .env, preencha com suas chaves
â”œâ”€â”€ CLAUDE.md                    â† guia completo do workspace para usuÃ¡rios do Claude Code
â”œâ”€â”€ AGENTS.md                    â† notas sobre delegaÃ§Ã£o a agentes
â”œâ”€â”€ MOTION_PHILOSOPHY.md         â† a estÃ©tica de motion que este repo almeja
â”œâ”€â”€ DESIGN.ais-example.md        â† a spec de marca da AIS â€” seu exemplo trabalhado
â”œâ”€â”€ assets/                      â† exemplos de marca compartilhados (logo AIS + tokens)
â”‚   â”œâ”€â”€ AIS Logo PNG.png
â”‚   â”œâ”€â”€ AIS Background.png
â”‚   â”œâ”€â”€ AIS Brand Guideline Small.jpg
â”‚   â””â”€â”€ brand-tokens.css         â† custom props CSS que toda comp pode importar
â”œâ”€â”€ docs/                        â† specs e planos mais longos
â”œâ”€â”€ scripts/                     â† scripts de preflight no nÃ­vel do workspace
â”œâ”€â”€ .claude/                     â† skills do Claude Code (slash commands drop-in)
â”‚   â”œâ”€â”€ launch.json
â”‚   â””â”€â”€ skills/                  â† /hyperframes, /gsap, /make-a-video, etc.
â”œâ”€â”€ package.json
â””â”€â”€ video-projects/              â† os 13 projetos
    â””â”€â”€ <projeto>/
        â”œâ”€â”€ index.html           â† ponto de entrada da composiÃ§Ã£o raiz
        â”œâ”€â”€ compositions/        â† sub-comps carregadas via data-composition-src
        â”œâ”€â”€ assets/              â† vÃ­deo, Ã¡udio, imagens, transcriÃ§Ãµes
        â”œâ”€â”€ final.mp4            â† a saÃ­da alvo â€” assista isto primeiro
        â”œâ”€â”€ renders/             â† seu rascunho local de render (no gitignore)
        â”œâ”€â”€ hyperframes.json     â† config da CLI (caminhos relativos a esta pasta)
        â”œâ”€â”€ meta.json            â† id / nome / dimensÃµes / fps
        â””â”€â”€ (STORYBOARD.md, HANDOFF.md, NOTES.md conforme aplicÃ¡vel)
```

## Os 12 projetos, em um relance

Comece abrindo cada `final.mp4` para ver o alvo, depois abra `index.html` para ver como foi construÃ­do.

### Vertical short-form (9:16, 1080Ã—1920)
| Projeto | O que Ã© |
|---|---|
| `may-shorts-19` | Talking-head estilo TikTok + motion graphics + legendas karaokÃª. Este tem o maior polimento â€” a skill `/short-form-video` foi escrita em torno dele. |
| `may-shorts-18` | Short anterior na mesma sÃ©rie. Compare v2 com may-shorts-19 para ver o que foi refinado. |

### Landscape short-form (16:9)
| Projeto | O que Ã© |
|---|---|
| `may-shorts-6` | Corte landscape de um talking-head short, mesmo padrÃ£o de produÃ§Ã£o da sÃ©rie vertical. |

### Promos de produto
| Projeto | O que Ã© |
|---|---|
| `clickup-demo` | Demo de produto SaaS de 60s â€” uso pesado de blocos do registry (x-post, ui-3d-reveal). Cinco versÃµes de render mostram a curva de iteraÃ§Ã£o. |
| `linear-promo-30s` | Promo de 30s estilo Linear na estÃ©tica Infinite Payments. Foi entregue como draft â€” terminÃ¡-lo Ã© um bom exercÃ­cio para estudante. Veja `NOTES.md`. |
| `hyperframes-sizzle` | Sizzle reel Hyperframes Ã— Claude Code. Usa o fluxo `/website-to-hyperframes`. |
| `first-agent-promo` | Filme de lanÃ§amento "Your First AI Agent" de 32s. Usa abordagem React-via-Babel em vez do padrÃ£o HTML â€” um contra-exemplo Ãºtil. |

### Aulas educacionais
| Projeto | O que Ã© |
|---|---|
| `aisoc-lesson-5-1` | VÃ­deo-aula completo (face-cam + motion graphics). Veja CLAUDE.md para o pipeline de nova aula (transcrever â†’ MG sincronizado por palavra â†’ seÃ§Ãµes). |
| `golden-ratio-demo` | Aula AIS sobre proporÃ§Ã£o em layout. Entregue como draft polido â€” veja `NOTES.md` para o que ficou em aberto. |
| `claude-edit-intro` | Intro estilo promo para um workflow de ediÃ§Ã£o; mÃ­nimo hardcoding de marca â€” template inicial fÃ¡cil. |

### Hype / lanÃ§amento de marca
| Projeto | O que Ã© |
|---|---|
| `aisoc-hype` | Filme de hype da marca AI Automation Society de 30s â€” o scaffold que muitos outros projetos AIS referenciam. |
| `aisoc-app-release` | Promo de 30s do lanÃ§amento do app mobile AIS. Leia `HANDOFF.md` â€” o Nate documentou cada pegadinha. |

## âš ï¸ Customizando para sua marca

**Esta Ã© a seÃ§Ã£o mais importante.** O repositÃ³rio vem com o branding da AI Automation Society (AIS) embutido como exemplo trabalhado. Antes de usar qualquer coisa disto para seu prÃ³prio trabalho, troque isto:

### A lista de troca global

| Arquivo | O que Ã© | O que fazer |
|---|---|---|
| `assets/brand-tokens.css` | Define `--ais-bg`, `--ais-accent`, `--ais-warn`, variÃ¡veis de fonte | Substitua os valores hex + famÃ­lias de fonte pelos seus. Considere renomear o prefixo das custom props para sua marca (`--acme-bg`, etc.) â€” mas aÃ­ vocÃª vai precisar fazer grep em toda composiÃ§Ã£o pelos nomes antigos. |
| `assets/AIS Logo PNG.png` | Logo usado pelos projetos AIS | Jogue seu prÃ³prio logo; ou mantenha o nome do arquivo para que as referÃªncias existentes funcionem, ou renomeie e faÃ§a grep-replace. |
| `assets/AIS Background.png` | Imagem de fundo ocasionalmente usada em cenas AIS | Mesmo padrÃ£o do logo. |
| `assets/AIS Brand Guideline Small.jpg` | Imagem de referÃªncia para a marca AIS | Delete; substitua por sua prÃ³pria imagem de guideline se tiver uma. |
| `DESIGN.ais-example.md` | Spec completa da marca AIS | **NÃ£o edite.** Use como seu template: copie para a pasta do seu novo projeto como `DESIGN.md` e reescreva cores, fontes, regras de motion e "O que NÃƒO fazer" para sua marca. |

### Acoplamento AIS por projeto

| Projeto | Acoplamento AIS | Tratar como |
|---|---|---|
| `aisoc-hype`, `aisoc-app-release`, `aisoc-lesson-5-1`, `golden-ratio-demo` | **Pesado** â€” valores hex hardcoded nas composiÃ§Ãµes, handle `@aiautomationsociety`, receita de glow do logo AIS, identidade on-camera do Nate em algumas cenas | Apenas referÃªncia. Reconstrua do zero para sua marca. |
| `clickup-demo`, `first-agent-promo`, `hyperframes-sizzle`, `linear-promo-30s`, `may-shorts-*`, `context-session`, `claude-edit-intro` | **MÃ­nimo** | Bons templates iniciais â€” troque os tokens de marca e vocÃª estÃ¡ quase lÃ¡. |

### Varredura de busca-e-correÃ§Ã£o

Depois de trocar os assets globais, rode este grep para achar quaisquer referÃªncias AIS ainda vivendo nas composiÃ§Ãµes:

```bash
# Acha valores hex hardcoded e strings AIS em qualquer lugar de video-projects/
grep -rEn "(#37bdf8|#f09025|#07121c|#195066|aisoc|AIS Logo|@aiautomationsociety)" video-projects/
```

Substitua cada resultado pela custom prop CSS correspondente do seu novo `brand-tokens.css`, ou pelo seu prÃ³prio hex/handle.

## Criando seu prÃ³prio novo projeto de vÃ­deo

1. Escolha um nome em kebab-case: `mkdir video-projects/meu-promo-marca`
2. FaÃ§a o scaffold com a CLI ou copie um irmÃ£o:
   ```bash
   cd video-projects/meu-promo-marca
   npx hyperframes init
   ```
   Ou, mais rÃ¡pido: copie `hyperframes.json` + `meta.json` de um projeto irmÃ£o que vocÃª goste, edite `meta.json` com seu novo id/nome/dimensÃµes, e comece o `index.html` do zero.
3. Instale os assets de marca compartilhados no seu projeto:
   ```bash
   cp ../../assets/brand-tokens.css assets/
   cp ../../assets/SeuLogo.png assets/
   ```
4. Escreva seu `DESIGN.md` (copie o formato de `DESIGN.ais-example.md` da raiz).
5. Construa. Preview. Lint. Render.

## O loop de autoria

```
editar â†’ lint â†’ preview (Studio, ao vivo) â†’ render draft â†’ verificar frames â†’ render final
```

| Passo | Comando | O que verificar |
|---|---|---|
| Lint | `npx hyperframes lint` | Zero erros antes do preview. Warnings sÃ£o sobreviventes. |
| Preview | `npx hyperframes preview` | Varra a timeline, conserte qualquer coisa estranha ao vivo. Hot reload funciona. |
| Render draft | `npx hyperframes render --quality draft --output renders/draft.mp4` | ~1â€“3 minutos. CRF 28 â€” pixelado mas rÃ¡pido. |
| Verificar frames | `ffmpeg -ss <t> -i renders/draft.mp4 -frames:v 1 out.png` | Puxe um frame por cena no momento-herÃ³i. Procure por rostos cortados, texto desalinhado, frames em branco. |
| Render final | `npx hyperframes render --quality standard --output renders/final.mp4` | Visualmente lossless 1080p. Ã‰ este que se entrega. |

> **`MOTION_PHILOSOPHY.md` Ã© sua academia estÃ©tica.** Antes de construir qualquer coisa, leia a seÃ§Ã£o 0 (as 10 Leis) e a seÃ§Ã£o 4 (checklist prÃ©-voo). Este doc Ã© a diferenÃ§a entre "renderizou" e "estÃ¡ bom".

## Ordem de leitura recomendada

1. **Este README** (vocÃª estÃ¡ aqui)
2. **`CLAUDE.md`** â€” guia completo do workspace, convenÃ§Ãµes, skills, contrato de render. Ãštil mesmo se vocÃª nÃ£o usar Claude Code â€” as 11 regras do Contrato de Render valem para qualquer um editando uma composiÃ§Ã£o.
3. **`MOTION_PHILOSOPHY.md`** â€” regras estÃ©ticas. Leia antes de brainstormar sua primeira cena.
4. **`DESIGN.ais-example.md`** â€” exemplo trabalhado de uma spec de marca.
5. **Escolha um projeto genÃ©rico** (`claude-edit-intro` Ã© um bom comeÃ§o). Abra `index.html`, `final.mp4` lado a lado, e a pasta `compositions/`. Leia, varra, modifique, re-renderize.
6. **Depois abra um projeto AIS** â€” vocÃª terÃ¡ o vocabulÃ¡rio para ver quÃ£o longe eles empurram o framework.

## Ecossistema: quem Ã© quem

Antes de mergulhar nas trilhas, vale entender a stack completa. SÃ£o ferramentas em **camadas diferentes**, nÃ£o concorrentes:

### Motores de base (rodam por baixo de tudo)

| Ferramenta | Camada | Para que serve |
|---|---|---|
| **FFmpeg** | Encoding | CLI clÃ¡ssica pra cortar/misturar/encodar Ã¡udio e vÃ­deo. NÃ£o sabe nada de HTML â€” sÃ³ pega frames + Ã¡udio e monta o MP4 final. Ã‰ a engrenagem que todos os outros usam no fim. |
| **Chromium / Puppeteer** | Browser headless | O Chrome sem janela, controlado por cÃ³digo. Renderiza o HTML frame a frame. Remotion e Hyperframes usam por baixo. |
| **Playwright** | AutomaÃ§Ã£o de browser | Primo do Puppeteer voltado pra **testes e scraping**. DÃ¡ pra tirar screenshot e gravar vÃ­deo, mas nÃ£o Ã© feito pra render determinÃ­stico de motion-graphics (sem frame-rate fixo, sem sync de Ã¡udio). |

### Frameworks de vÃ­deo-como-cÃ³digo

| Framework | Linguagem | Quando faz sentido |
|---|---|---|
| **Hyperframes** (este repo) | HTML + GSAP | ComposiÃ§Ãµes declarativas com `data-start`/`data-duration` e um timeline GSAP por cena. TTS (Kokoro) + transcriÃ§Ã£o (Whisper) jÃ¡ vÃªm no CLI. Sem paywall â€” da HeyGen. Studio com hot reload. |
| **Remotion** | React (TSX) | VÃ­deo escrito em componentes com `useCurrentFrame()`. Ecossistema React maduro. Tem paywall comercial acima de certa escala. |
| Motion Canvas / Revideo | TypeScript imperativo | Alternativas para quem quer timelines imperativas (`yield* tween`). |

Ambos os frameworks fazem a mesma coisa por baixo: **abrem Chromium, capturam frame a frame, passam pro FFmpeg**. A diferenÃ§a estÃ¡ na **superfÃ­cie de autoria** (HTML vs JSX) e no ecossistema de blocos prontos.

### Skills (slash commands do Claude Code)

NÃ£o sÃ£o motores de render â€” sÃ£o **prompts empacotados** que ensinam o Claude a usar as ferramentas acima com bom gosto:

- `/hyperframes`, `/hyperframes-cli`, `/hyperframes-registry` â€” autoria e CLI deste framework
- `/gsap` â€” easings, timelines, stagger, ScrollTrigger
- `/remotion` â€” equivalente para o ecossistema React
- `/make-a-video`, `/short-form-video`, `/website-to-hyperframes` â€” playbooks ponta-a-ponta (entrevista â†’ storyboard â†’ render)
- `/frontend-design`, `/canvas-design`, `/theme-factory`, `/brand-guidelines` â€” estÃ©tica de pÃ¡ginas, posteres e artifacts estÃ¡ticos

Skills nÃ£o existem sem as ferramentas subjacentes. Uma skill `/hyperframes` bem usada economiza horas; sem o framework por baixo, Ã© sÃ³ texto.

### Resumo em uma frase

A stack deste workspace Ã© **Hyperframes â†’ Chromium â†’ FFmpeg**, com as skills guiando as decisÃµes estÃ©ticas e de pipeline. Se vocÃª viesse do React, trocaria sÃ³ a camada do meio por **Remotion**.

## Usando Claude Code com este repositÃ³rio

A pasta `.claude/skills/` traz um conjunto de slash commands que encodam padrÃµes especÃ­ficos do framework (registro `window.__timelines`, semÃ¢ntica de atributos `data-*`, CSS compatÃ­vel com shader). Se vocÃª usa o [Claude Code](https://claude.com/claude-code), eles ativam automaticamente:

- `/hyperframes` â€” autoria/ediÃ§Ã£o de composiÃ§Ãµes, legendas, TTS, animaÃ§Ã£o audio-reativa
- `/hyperframes-cli` â€” referÃªncia da CLI (init, add, lint, preview, render, transcribe, tts)
- `/gsap` â€” animaÃ§Ã£o GSAP: timelines, easing, stagger, plugins
- `/hyperframes-registry` â€” instalar blocks/components do catÃ¡logo
- `/website-to-hyperframes` â€” transformar uma URL em composiÃ§Ã£o (captura-para-vÃ­deo em 7 passos)
- `/make-a-video` â€” fluxo iniciante ponta-a-ponta
- `/short-form-video` â€” playbook 9:16 talking-head + motion graphics

NÃ£o usa Claude Code? As skills sÃ£o sÃ³ markdown â€” abra e leia como documentaÃ§Ã£o.

## SoluÃ§Ã£o de problemas

| Sintoma | Primeira coisa a tentar |
|---|---|
| `npx hyperframes` â€” comando nÃ£o encontrado | Rode `npm install` na raiz do repo primeiro |
| Render falha no meio | `npx hyperframes doctor` â€” verifica Node, FFmpeg, Chrome |
| Preview do Studio travado em 0s | Hard-refresh no navegador (Ctrl+Shift+R). Se falhar, tente uma URL de sub-composiÃ§Ã£o especÃ­fica: `http://localhost:3002/?comp=<sub-comp-id>` |
| Erros de lint sobre clips sobrepostos | Dois clips no mesmo `data-track-index` sobrepostos no tempo â€” atribua track indices diferentes ou ajuste `data-start` / `data-duration` |
| Erros de lint sobre `missing_gsap_script` | Todo HTML de sub-composiÃ§Ã£o precisa do seu prÃ³prio `<script src="https://cdn.jsdelivr.net/npm/gsap@3.14.2/dist/gsap.min.js"></script>` antes do seu IIFE â€” GSAP nÃ£o herda do pai |
| VÃ­deo congelado num render, Ã¡udio continua | Um elemento `<video>` foi animado diretamente (nÃ£o anime `width`/`height`/`top`/`left` num `<video>`). Envolva num `<div>` e anime o wrapper. |

Mais: `npx hyperframes docs <tÃ³pico>` (tÃ³picos: `data-attributes`, `gsap`, `rendering`, `examples`, `troubleshooting`, `compositions`).

## CrÃ©ditos e licenÃ§a

- **CÃ³digo e composiÃ§Ãµes** â€” MIT, veja `LICENSE`.
- **Assets de marca AIS** (logo, background, imagem de guideline, tokens AIS) â€” permanecem propriedade da AI Automation Society. Inclusos como exemplo trabalhado; nÃ£o licenciados para reuso. Substitua pelos seus prÃ³prios antes de entregar.
- **Hyperframes** â€” framework Â© HeyGen, docs em https://hyperframes.heygen.com.

ConstruÃ­do por [Nate Herk](https://aiautomationsociety.ai). Divirta-se destrinchando.

---

<div align="center">
  <img src="capa/logo.svg" alt="Arckhé AI" height="32" />
  <p><strong>Arckhé AI</strong></p>
</div>