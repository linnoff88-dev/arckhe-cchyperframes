ï»¿# Hyperframes Editor ê¢â¬â EdiêÂ§êÂ£o Estudante

<div align="center">
  <img src="capa/logo.svg" alt="Arckhé AI" height="48" />
  <p><strong>Arckhé AI</strong></p>
</div>


Uma bancada de trabalho para construir pipelines de vêÂ­deo motion-graphics em **HTML + GSAP puros**, alimentada pelo [Hyperframes](https://hyperframes.heygen.com). Doze projetos de vêÂ­deo finalizados que vocêÂª pode clonar, varrer a timeline, destrinchar e reconstruir como seus.

> Isto **nêÂ£o** êÂ© um stack de vêÂ­deo Remotion / React / Next.js. Cada composiêÂ§êÂ£o neste repositêÂ³rio êÂ© um arquivo HTML comum com uma timeline GSAP pausada anexada a `window.__timelines`. A CLI do Hyperframes cuida de lint, preview e render.

---

## Para quem êÂ© isso

Estudantes que querem aprender como vêÂ­deos promocionais e short-form profissionais sêÂ£o construêÂ­dos de ponta a ponta ê¢â¬â storyboard, sistema de marca, motion graphics, sincronia de êÂ¡udio, pipeline de render ê¢â¬â atravêÂ©s de engenharia reversa de projetos reais. Todo projeto aqui entregou (ou quase entregou). Varra as composiêÂ§êÂµes, leia os docs de HANDOFF/STORYBOARD, assista ao `final.mp4`, depois mude coisas e veja o que quebra.

## PrêÂ©-requisitos

- **Node 20+** ê¢â¬â rode `node --version` para verificar
- **FFmpeg** no seu `PATH` ê¢â¬â necessêÂ¡rio para extraêÂ§êÂ£o e reencode de êÂ¡udio
- **Chrome (mais recente)** ê¢â¬â Hyperframes renderiza via Chromium headless
- **~5 GB de disco livre** ê¢â¬â node_modules êÂ© grande; renders sêÂ£o maiores ainda
- **16 GB de RAM recomendado** para preview fluido no Studio com mêÂºltiplos blocos de shader

Rode `npx hyperframes doctor` apêÂ³s `npm install` ê¢â¬â ele reporta o que estêÂ¡ faltando.

## InêÂ­cio rêÂ¡pido

```bash
git clone <url-do-seu-fork> hyperframes-editor
cd hyperframes-editor
npm install

# Opcional ê¢â¬â apenas se quiser usar as integraêÂ§êÂµes ClickUp / OpenAI
cp .env.example .env
# ...depois edite .env com suas prêÂ³prias chaves

# Abra o Studio em um dos projetos inclusos
cd video-projects/may-shorts-19
npx hyperframes preview    # http://localhost:3002
```

O Studio recarrega automaticamente ao salvar o arquivo. Varra a timeline, inspecione cenas, mude cores, veja re-renderizar ao vivo.

## Como rodar os exemplos passo a passo

Guia prêÂ¡tico para quem estêÂ¡ comeêÂ§ando do zero com o Hyperframes.

### 1. Instalar dependêÂªncias (uma vez sêÂ³, na raiz)

```bash
cd cchyperframes
npm install
```

### 2. Verificar o ambiente

Confirma se Node 20+, FFmpeg e Chrome estêÂ£o instalados e acessêÂ­veis:

```bash
npx hyperframes doctor
```

### 3. Entrar num projeto

Cada pasta em `video-projects/` êÂ© um projeto independente com seu prêÂ³prio `index.html`, `assets/` e `compositions/`.

```bash
cd video-projects/may-shorts-19      # ou qualquer outro projeto
```

### 4. Preview ao vivo no Studio (hot reload)

```bash
npx hyperframes preview              # abre http://localhost:3002
```

O Studio recarrega automaticamente ao salvar qualquer arquivo. Varra a timeline, mude cores, teste animaêÂ§êÂµes em tempo real.

### 5. Lint antes de renderizar

```bash
npx hyperframes lint
```

Zero erros antes de partir para o render. Warnings vocêÂª pode sobreviver com.

### 6. Render rêÂ¡pido de rascunho (1ê¢â¬â3 min, pixelado)

```bash
npx hyperframes render --quality draft --output renders/draft.mp4
```

Use para validaêÂ§êÂ£o rêÂ¡pida de pacing e sincronia.

### 7. Render final (1080p visualmente lossless)

```bash
npx hyperframes render --quality standard --output renders/final.mp4
```

Este êÂ© o render que se entrega.

### Por onde comeêÂ§ar (ordem recomendada)

| NêÂ­vel | Projeto | Por quêÂª |
|---|---|---|
| **Iniciante** | `claude-edit-intro` | Intro estilo promo com mêÂ­nimo hardcoding de marca ê¢â¬â template inicial fêÂ¡cil de entender. |
| **Polido** | `may-shorts-19` | Vertical TikTok com talking-head + motion graphics + legendas karaokêÂª. A skill `/short-form-video` foi escrita em torno dele. |
| **Produto SaaS** | `clickup-demo` | Demo de 60s com uso pesado de blocos do registry (x-post, ui-3d-reveal). Mostra a curva de iteraêÂ§êÂ£o. |
| **Motion avanêÂ§ado** | `linear-promo-30s` | Promo de 30s na estêÂ©tica Infinite Payments. Entregue como draft ê¢â¬â terminêÂ¡-lo êÂ© um bom exercêÂ­cio. |

Abra o `final.mp4` de cada projeto primeiro para ver o alvo, depois o `index.html` lado a lado para entender como foi construêÂ­do.

### Dicas importantes

- **Sempre rode os comandos de dentro da pasta do projeto** (nêÂ£o da raiz do workspace). A CLI lêÂª `hyperframes.json` e `meta.json` do diretêÂ³rio atual.
- **Leia `MOTION_PHILOSOPHY.md`** antes de brainstormar sua primeira cena ê¢â¬â as 10 Leis (seêÂ§êÂ£o 0) e o checklist prêÂ©-voo (seêÂ§êÂ£o 4) sêÂ£o o que separa "renderizou" de "estêÂ¡ bom".
- **Se o Studio travar em 0s**, force refresh no navegador (Ctrl+Shift+R) ou abra uma sub-composiêÂ§êÂ£o especêÂ­fica: `http://localhost:3002/?comp=<sub-comp-id>`.
- **Se um render falhar no meio**, rode `npx hyperframes doctor` para ver o que estêÂ¡ faltando.

## Estrutura do repositêÂ³rio

```
hyperframes-editor/
ê¢âÅê¢ââ¬ê¢ââ¬ README.md                    ê¢â Â vocêÂª estêÂ¡ aqui
ê¢âÅê¢ââ¬ê¢ââ¬ LICENSE                      ê¢â Â MIT (veja nota sobre assets de marca)
ê¢âÅê¢ââ¬ê¢ââ¬ .env.example                 ê¢â Â copie para .env, preencha com suas chaves
ê¢âÅê¢ââ¬ê¢ââ¬ CLAUDE.md                    ê¢â Â guia completo do workspace para usuêÂ¡rios do Claude Code
ê¢âÅê¢ââ¬ê¢ââ¬ AGENTS.md                    ê¢â Â notas sobre delegaêÂ§êÂ£o a agentes
ê¢âÅê¢ââ¬ê¢ââ¬ MOTION_PHILOSOPHY.md         ê¢â Â a estêÂ©tica de motion que este repo almeja
ê¢âÅê¢ââ¬ê¢ââ¬ DESIGN.ais-example.md        ê¢â Â a spec de marca da AIS ê¢â¬â seu exemplo trabalhado
ê¢âÅê¢ââ¬ê¢ââ¬ assets/                      ê¢â Â exemplos de marca compartilhados (logo AIS + tokens)
ê¢ââ   ê¢âÅê¢ââ¬ê¢ââ¬ AIS Logo PNG.png
ê¢ââ   ê¢âÅê¢ââ¬ê¢ââ¬ AIS Background.png
ê¢ââ   ê¢âÅê¢ââ¬ê¢ââ¬ AIS Brand Guideline Small.jpg
ê¢ââ   ê¢ââê¢ââ¬ê¢ââ¬ brand-tokens.css         ê¢â Â custom props CSS que toda comp pode importar
ê¢âÅê¢ââ¬ê¢ââ¬ docs/                        ê¢â Â specs e planos mais longos
ê¢âÅê¢ââ¬ê¢ââ¬ scripts/                     ê¢â Â scripts de preflight no nêÂ­vel do workspace
ê¢âÅê¢ââ¬ê¢ââ¬ .claude/                     ê¢â Â skills do Claude Code (slash commands drop-in)
ê¢ââ   ê¢âÅê¢ââ¬ê¢ââ¬ launch.json
ê¢ââ   ê¢ââê¢ââ¬ê¢ââ¬ skills/                  ê¢â Â /hyperframes, /gsap, /make-a-video, etc.
ê¢âÅê¢ââ¬ê¢ââ¬ package.json
ê¢ââê¢ââ¬ê¢ââ¬ video-projects/              ê¢â Â os 13 projetos
    ê¢ââê¢ââ¬ê¢ââ¬ <projeto>/
        ê¢âÅê¢ââ¬ê¢ââ¬ index.html           ê¢â Â ponto de entrada da composiêÂ§êÂ£o raiz
        ê¢âÅê¢ââ¬ê¢ââ¬ compositions/        ê¢â Â sub-comps carregadas via data-composition-src
        ê¢âÅê¢ââ¬ê¢ââ¬ assets/              ê¢â Â vêÂ­deo, êÂ¡udio, imagens, transcriêÂ§êÂµes
        ê¢âÅê¢ââ¬ê¢ââ¬ final.mp4            ê¢â Â a saêÂ­da alvo ê¢â¬â assista isto primeiro
        ê¢âÅê¢ââ¬ê¢ââ¬ renders/             ê¢â Â seu rascunho local de render (no gitignore)
        ê¢âÅê¢ââ¬ê¢ââ¬ hyperframes.json     ê¢â Â config da CLI (caminhos relativos a esta pasta)
        ê¢âÅê¢ââ¬ê¢ââ¬ meta.json            ê¢â Â id / nome / dimensêÂµes / fps
        ê¢ââê¢ââ¬ê¢ââ¬ (STORYBOARD.md, HANDOFF.md, NOTES.md conforme aplicêÂ¡vel)
```

## Os 12 projetos, em um relance

Comece abrindo cada `final.mp4` para ver o alvo, depois abra `index.html` para ver como foi construêÂ­do.

### Vertical short-form (9:16, 1080êâ1920)
| Projeto | O que êÂ© |
|---|---|
| `may-shorts-19` | Talking-head estilo TikTok + motion graphics + legendas karaokêÂª. Este tem o maior polimento ê¢â¬â a skill `/short-form-video` foi escrita em torno dele. |
| `may-shorts-18` | Short anterior na mesma sêÂ©rie. Compare v2 com may-shorts-19 para ver o que foi refinado. |

### Landscape short-form (16:9)
| Projeto | O que êÂ© |
|---|---|
| `may-shorts-6` | Corte landscape de um talking-head short, mesmo padrêÂ£o de produêÂ§êÂ£o da sêÂ©rie vertical. |

### Promos de produto
| Projeto | O que êÂ© |
|---|---|
| `clickup-demo` | Demo de produto SaaS de 60s ê¢â¬â uso pesado de blocos do registry (x-post, ui-3d-reveal). Cinco versêÂµes de render mostram a curva de iteraêÂ§êÂ£o. |
| `linear-promo-30s` | Promo de 30s estilo Linear na estêÂ©tica Infinite Payments. Foi entregue como draft ê¢â¬â terminêÂ¡-lo êÂ© um bom exercêÂ­cio para estudante. Veja `NOTES.md`. |
| `hyperframes-sizzle` | Sizzle reel Hyperframes êâ Claude Code. Usa o fluxo `/website-to-hyperframes`. |
| `first-agent-promo` | Filme de lanêÂ§amento "Your First AI Agent" de 32s. Usa abordagem React-via-Babel em vez do padrêÂ£o HTML ê¢â¬â um contra-exemplo êÂºtil. |

### Aulas educacionais
| Projeto | O que êÂ© |
|---|---|
| `aisoc-lesson-5-1` | VêÂ­deo-aula completo (face-cam + motion graphics). Veja CLAUDE.md para o pipeline de nova aula (transcrever ê¢â â MG sincronizado por palavra ê¢â â seêÂ§êÂµes). |
| `golden-ratio-demo` | Aula AIS sobre proporêÂ§êÂ£o em layout. Entregue como draft polido ê¢â¬â veja `NOTES.md` para o que ficou em aberto. |
| `claude-edit-intro` | Intro estilo promo para um workflow de ediêÂ§êÂ£o; mêÂ­nimo hardcoding de marca ê¢â¬â template inicial fêÂ¡cil. |

### Hype / lanêÂ§amento de marca
| Projeto | O que êÂ© |
|---|---|
| `aisoc-hype` | Filme de hype da marca AI Automation Society de 30s ê¢â¬â o scaffold que muitos outros projetos AIS referenciam. |
| `aisoc-app-release` | Promo de 30s do lanêÂ§amento do app mobile AIS. Leia `HANDOFF.md` ê¢â¬â o Nate documentou cada pegadinha. |

## ê¢Å¡Â ê¯Â¸Â Customizando para sua marca

**Esta êÂ© a seêÂ§êÂ£o mais importante.** O repositêÂ³rio vem com o branding da AI Automation Society (AIS) embutido como exemplo trabalhado. Antes de usar qualquer coisa disto para seu prêÂ³prio trabalho, troque isto:

### A lista de troca global

| Arquivo | O que êÂ© | O que fazer |
|---|---|---|
| `assets/brand-tokens.css` | Define `--ais-bg`, `--ais-accent`, `--ais-warn`, variêÂ¡veis de fonte | Substitua os valores hex + famêÂ­lias de fonte pelos seus. Considere renomear o prefixo das custom props para sua marca (`--acme-bg`, etc.) ê¢â¬â mas aêÂ­ vocêÂª vai precisar fazer grep em toda composiêÂ§êÂ£o pelos nomes antigos. |
| `assets/AIS Logo PNG.png` | Logo usado pelos projetos AIS | Jogue seu prêÂ³prio logo; ou mantenha o nome do arquivo para que as referêÂªncias existentes funcionem, ou renomeie e faêÂ§a grep-replace. |
| `assets/AIS Background.png` | Imagem de fundo ocasionalmente usada em cenas AIS | Mesmo padrêÂ£o do logo. |
| `assets/AIS Brand Guideline Small.jpg` | Imagem de referêÂªncia para a marca AIS | Delete; substitua por sua prêÂ³pria imagem de guideline se tiver uma. |
| `DESIGN.ais-example.md` | Spec completa da marca AIS | **NêÂ£o edite.** Use como seu template: copie para a pasta do seu novo projeto como `DESIGN.md` e reescreva cores, fontes, regras de motion e "O que NêÆO fazer" para sua marca. |

### Acoplamento AIS por projeto

| Projeto | Acoplamento AIS | Tratar como |
|---|---|---|
| `aisoc-hype`, `aisoc-app-release`, `aisoc-lesson-5-1`, `golden-ratio-demo` | **Pesado** ê¢â¬â valores hex hardcoded nas composiêÂ§êÂµes, handle `@aiautomationsociety`, receita de glow do logo AIS, identidade on-camera do Nate em algumas cenas | Apenas referêÂªncia. Reconstrua do zero para sua marca. |
| `clickup-demo`, `first-agent-promo`, `hyperframes-sizzle`, `linear-promo-30s`, `may-shorts-*`, `context-session`, `claude-edit-intro` | **MêÂ­nimo** | Bons templates iniciais ê¢â¬â troque os tokens de marca e vocêÂª estêÂ¡ quase lêÂ¡. |

### Varredura de busca-e-correêÂ§êÂ£o

Depois de trocar os assets globais, rode este grep para achar quaisquer referêÂªncias AIS ainda vivendo nas composiêÂ§êÂµes:

```bash
# Acha valores hex hardcoded e strings AIS em qualquer lugar de video-projects/
grep -rEn "(#37bdf8|#f09025|#07121c|#195066|aisoc|AIS Logo|@aiautomationsociety)" video-projects/
```

Substitua cada resultado pela custom prop CSS correspondente do seu novo `brand-tokens.css`, ou pelo seu prêÂ³prio hex/handle.

## Criando seu prêÂ³prio novo projeto de vêÂ­deo

1. Escolha um nome em kebab-case: `mkdir video-projects/meu-promo-marca`
2. FaêÂ§a o scaffold com a CLI ou copie um irmêÂ£o:
   ```bash
   cd video-projects/meu-promo-marca
   npx hyperframes init
   ```
   Ou, mais rêÂ¡pido: copie `hyperframes.json` + `meta.json` de um projeto irmêÂ£o que vocêÂª goste, edite `meta.json` com seu novo id/nome/dimensêÂµes, e comece o `index.html` do zero.
3. Instale os assets de marca compartilhados no seu projeto:
   ```bash
   cp ../../assets/brand-tokens.css assets/
   cp ../../assets/SeuLogo.png assets/
   ```
4. Escreva seu `DESIGN.md` (copie o formato de `DESIGN.ais-example.md` da raiz).
5. Construa. Preview. Lint. Render.

## O loop de autoria

```
editar ê¢â â lint ê¢â â preview (Studio, ao vivo) ê¢â â render draft ê¢â â verificar frames ê¢â â render final
```

| Passo | Comando | O que verificar |
|---|---|---|
| Lint | `npx hyperframes lint` | Zero erros antes do preview. Warnings sêÂ£o sobreviventes. |
| Preview | `npx hyperframes preview` | Varra a timeline, conserte qualquer coisa estranha ao vivo. Hot reload funciona. |
| Render draft | `npx hyperframes render --quality draft --output renders/draft.mp4` | ~1ê¢â¬â3 minutos. CRF 28 ê¢â¬â pixelado mas rêÂ¡pido. |
| Verificar frames | `ffmpeg -ss <t> -i renders/draft.mp4 -frames:v 1 out.png` | Puxe um frame por cena no momento-herêÂ³i. Procure por rostos cortados, texto desalinhado, frames em branco. |
| Render final | `npx hyperframes render --quality standard --output renders/final.mp4` | Visualmente lossless 1080p. êâ° este que se entrega. |

> **`MOTION_PHILOSOPHY.md` êÂ© sua academia estêÂ©tica.** Antes de construir qualquer coisa, leia a seêÂ§êÂ£o 0 (as 10 Leis) e a seêÂ§êÂ£o 4 (checklist prêÂ©-voo). Este doc êÂ© a diferenêÂ§a entre "renderizou" e "estêÂ¡ bom".

## Ordem de leitura recomendada

1. **Este README** (vocêÂª estêÂ¡ aqui)
2. **`CLAUDE.md`** ê¢â¬â guia completo do workspace, convenêÂ§êÂµes, skills, contrato de render. êÅ¡til mesmo se vocêÂª nêÂ£o usar Claude Code ê¢â¬â as 11 regras do Contrato de Render valem para qualquer um editando uma composiêÂ§êÂ£o.
3. **`MOTION_PHILOSOPHY.md`** ê¢â¬â regras estêÂ©ticas. Leia antes de brainstormar sua primeira cena.
4. **`DESIGN.ais-example.md`** ê¢â¬â exemplo trabalhado de uma spec de marca.
5. **Escolha um projeto genêÂ©rico** (`claude-edit-intro` êÂ© um bom comeêÂ§o). Abra `index.html`, `final.mp4` lado a lado, e a pasta `compositions/`. Leia, varra, modifique, re-renderize.
6. **Depois abra um projeto AIS** ê¢â¬â vocêÂª terêÂ¡ o vocabulêÂ¡rio para ver quêÂ£o longe eles empurram o framework.

## Ecossistema: quem êÂ© quem

Antes de mergulhar nas trilhas, vale entender a stack completa. SêÂ£o ferramentas em **camadas diferentes**, nêÂ£o concorrentes:

### Motores de base (rodam por baixo de tudo)

| Ferramenta | Camada | Para que serve |
|---|---|---|
| **FFmpeg** | Encoding | CLI clêÂ¡ssica pra cortar/misturar/encodar êÂ¡udio e vêÂ­deo. NêÂ£o sabe nada de HTML ê¢â¬â sêÂ³ pega frames + êÂ¡udio e monta o MP4 final. êâ° a engrenagem que todos os outros usam no fim. |
| **Chromium / Puppeteer** | Browser headless | O Chrome sem janela, controlado por cêÂ³digo. Renderiza o HTML frame a frame. Remotion e Hyperframes usam por baixo. |
| **Playwright** | AutomaêÂ§êÂ£o de browser | Primo do Puppeteer voltado pra **testes e scraping**. DêÂ¡ pra tirar screenshot e gravar vêÂ­deo, mas nêÂ£o êÂ© feito pra render determinêÂ­stico de motion-graphics (sem frame-rate fixo, sem sync de êÂ¡udio). |

### Frameworks de vêÂ­deo-como-cêÂ³digo

| Framework | Linguagem | Quando faz sentido |
|---|---|---|
| **Hyperframes** (este repo) | HTML + GSAP | ComposiêÂ§êÂµes declarativas com `data-start`/`data-duration` e um timeline GSAP por cena. TTS (Kokoro) + transcriêÂ§êÂ£o (Whisper) jêÂ¡ vêÂªm no CLI. Sem paywall ê¢â¬â da HeyGen. Studio com hot reload. |
| **Remotion** | React (TSX) | VêÂ­deo escrito em componentes com `useCurrentFrame()`. Ecossistema React maduro. Tem paywall comercial acima de certa escala. |
| Motion Canvas / Revideo | TypeScript imperativo | Alternativas para quem quer timelines imperativas (`yield* tween`). |

Ambos os frameworks fazem a mesma coisa por baixo: **abrem Chromium, capturam frame a frame, passam pro FFmpeg**. A diferenêÂ§a estêÂ¡ na **superfêÂ­cie de autoria** (HTML vs JSX) e no ecossistema de blocos prontos.

### Skills (slash commands do Claude Code)

NêÂ£o sêÂ£o motores de render ê¢â¬â sêÂ£o **prompts empacotados** que ensinam o Claude a usar as ferramentas acima com bom gosto:

- `/hyperframes`, `/hyperframes-cli`, `/hyperframes-registry` ê¢â¬â autoria e CLI deste framework
- `/gsap` ê¢â¬â easings, timelines, stagger, ScrollTrigger
- `/remotion` ê¢â¬â equivalente para o ecossistema React
- `/make-a-video`, `/short-form-video`, `/website-to-hyperframes` ê¢â¬â playbooks ponta-a-ponta (entrevista ê¢â â storyboard ê¢â â render)
- `/frontend-design`, `/canvas-design`, `/theme-factory`, `/brand-guidelines` ê¢â¬â estêÂ©tica de pêÂ¡ginas, posteres e artifacts estêÂ¡ticos

Skills nêÂ£o existem sem as ferramentas subjacentes. Uma skill `/hyperframes` bem usada economiza horas; sem o framework por baixo, êÂ© sêÂ³ texto.

### Resumo em uma frase

A stack deste workspace êÂ© **Hyperframes ê¢â â Chromium ê¢â â FFmpeg**, com as skills guiando as decisêÂµes estêÂ©ticas e de pipeline. Se vocêÂª viesse do React, trocaria sêÂ³ a camada do meio por **Remotion**.

## Usando Claude Code com este repositêÂ³rio

A pasta `.claude/skills/` traz um conjunto de slash commands que encodam padrêÂµes especêÂ­ficos do framework (registro `window.__timelines`, semêÂ¢ntica de atributos `data-*`, CSS compatêÂ­vel com shader). Se vocêÂª usa o [Claude Code](https://claude.com/claude-code), eles ativam automaticamente:

- `/hyperframes` ê¢â¬â autoria/ediêÂ§êÂ£o de composiêÂ§êÂµes, legendas, TTS, animaêÂ§êÂ£o audio-reativa
- `/hyperframes-cli` ê¢â¬â referêÂªncia da CLI (init, add, lint, preview, render, transcribe, tts)
- `/gsap` ê¢â¬â animaêÂ§êÂ£o GSAP: timelines, easing, stagger, plugins
- `/hyperframes-registry` ê¢â¬â instalar blocks/components do catêÂ¡logo
- `/website-to-hyperframes` ê¢â¬â transformar uma URL em composiêÂ§êÂ£o (captura-para-vêÂ­deo em 7 passos)
- `/make-a-video` ê¢â¬â fluxo iniciante ponta-a-ponta
- `/short-form-video` ê¢â¬â playbook 9:16 talking-head + motion graphics

NêÂ£o usa Claude Code? As skills sêÂ£o sêÂ³ markdown ê¢â¬â abra e leia como documentaêÂ§êÂ£o.

## SoluêÂ§êÂ£o de problemas

| Sintoma | Primeira coisa a tentar |
|---|---|
| `npx hyperframes` ê¢â¬â comando nêÂ£o encontrado | Rode `npm install` na raiz do repo primeiro |
| Render falha no meio | `npx hyperframes doctor` ê¢â¬â verifica Node, FFmpeg, Chrome |
| Preview do Studio travado em 0s | Hard-refresh no navegador (Ctrl+Shift+R). Se falhar, tente uma URL de sub-composiêÂ§êÂ£o especêÂ­fica: `http://localhost:3002/?comp=<sub-comp-id>` |
| Erros de lint sobre clips sobrepostos | Dois clips no mesmo `data-track-index` sobrepostos no tempo ê¢â¬â atribua track indices diferentes ou ajuste `data-start` / `data-duration` |
| Erros de lint sobre `missing_gsap_script` | Todo HTML de sub-composiêÂ§êÂ£o precisa do seu prêÂ³prio `<script src="https://cdn.jsdelivr.net/npm/gsap@3.14.2/dist/gsap.min.js"></script>` antes do seu IIFE ê¢â¬â GSAP nêÂ£o herda do pai |
| VêÂ­deo congelado num render, êÂ¡udio continua | Um elemento `<video>` foi animado diretamente (nêÂ£o anime `width`/`height`/`top`/`left` num `<video>`). Envolva num `<div>` e anime o wrapper. |

Mais: `npx hyperframes docs <têÂ³pico>` (têÂ³picos: `data-attributes`, `gsap`, `rendering`, `examples`, `troubleshooting`, `compositions`).

## CrêÂ©ditos e licenêÂ§a

- **CêÂ³digo e composiêÂ§êÂµes** ê¢â¬â MIT, veja `LICENSE`.
- **Assets de marca AIS** (logo, background, imagem de guideline, tokens AIS) ê¢â¬â permanecem propriedade da AI Automation Society. Inclusos como exemplo trabalhado; nêÂ£o licenciados para reuso. Substitua pelos seus prêÂ³prios antes de entregar.
- **Hyperframes** ê¢â¬â framework êÂ© HeyGen, docs em https://hyperframes.heygen.com.

ConstruêÂ­do por [Nate Herk](https://aiautomationsociety.ai). Divirta-se destrinchando.

---

<div align="center">
  <img src="capa/logo.svg" alt="Arckhé AI" height="32" />
  <p><strong>Arckhé AI</strong></p>
</div>