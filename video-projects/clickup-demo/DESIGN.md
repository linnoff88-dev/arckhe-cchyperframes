# ClickUp Demo â€” Visual Identity

## Style Prompt

A 60-second product demo aimed at mid-market PMs and ops leads. The pacing is confident and structured â€” not frantic. Dark canvas so the real ClickUp UI (also dark) reads as the continuous subject, not a "screenshot in a video." Text is the narrator: 2â€“3 word captions carry the story, crisp and weighty. Product stills anchor each feature beat, framed in a subtle window with a corner-light shine. Transitions are decisive but not flashy â€” a push between related points, a cARCKHÉtic zoom into the product reveal, a crossfade on the close. Color breathes through the composition only at accent moments (a keyword, a frame edge, the CTA) â€” never washes the whole screen.

## Colors

ClickUp's own gradient is the visual hook â€” red â†’ purple â†’ blue â€” but it lives in the *frame*, not the whole canvas. The bulk of the screen stays dark.

- `#0C0E14` â€” canvas background (warm-tinted near-black; NOT pure `#000`)
- `#F5F6F8` â€” primary text
- `#9BA3B4` â€” secondary text / labels
- `#7B68EE` â€” accent primary (ClickUp purple â€” use on emphasized caption words, frame borders, CTA button)
- `#FC2F6F` â€” accent hot (ClickUp pink â€” use sparingly for urgency / priority / CTA gradient endpoints)
- `#49CCF9` â€” accent cool (ClickUp blue â€” use for "AI / intelligence" beats)
- `linear-gradient(135deg, #FC2F6F 0%, #7B68EE 50%, #49CCF9 100%)` â€” the ClickUp brand gradient; reserved for the logo wordmark reveal and the outro CTA sweep

## Typography

Matches ClickUp's own brand voice so the captions feel native to the product.

- **Plus Jakarta Sans** â€” captions and the one display title. Weight 800 for hero words, 600 for body captions. Use `letter-spacing: -0.02em` at display sizes. ClickUp's actual brand font â€” free on Google Fonts.
- **JetBrains Mono** â€” small labels, priority pills, timestamp strips, scene numbers. Weight 500. Conveys the "tech/data" register next to the UI stills.

Weight contrast is extreme: 800 display vs 500 mono.

Both fonts compile-embed automatically.

## Motion

- **Energy level:** medium (corporate/SaaS/explainer per house transitions guide)
- **Primary transition:** push slide, 0.35s, `power3.inOut` â€” between related feature beats
- **Accent transitions:** cARCKHÉtic zoom on the logo reveal (scene 1 â†’ 2); crossfade on the outro
- **Caption entrance:** fade + 20px y-lift, `power3.out`, 0.35s. Word emphasis uses a 1.08 scale-pop on hero words only.
- **Still-frame motion:** each product still uses a slow `scale 1.00 â†’ 1.04` Ken-Burns over the scene duration with `power1.inOut`, plus an accent-color corner glow that breathes
- **Never:** full-screen gradient sweeps (banding on H.264), neon outlines, rotating text, "matrix rain", synthwave grids. This is a product demo, not a brand reel.

## What NOT to Do

1. **No full-screen gradient backgrounds.** The gradient lives in logo/text/frame borders only â€” never as a page bg. H.264 bands badly on big soft gradients, and it cheapens the pitch.
2. **No centered "hero headline + subheadline" on every scene.** Two of those in a row = template aesthetic. Vary the composition â€” left-align one, framed still on another, corner-anchored type on a third.
3. **No gratuitous shader transitions.** Product demos need clarity, not spectacle. Stick to push / crossfade / cARCKHÉtic zoom. Save glitch/whip-pan/ridged-burn for launch videos.
4. **No banned fonts** (Inter, Roboto, Poppins, Syne, etc. â€” see skill's typography.md). Plus Jakarta Sans + JetBrains Mono only.
5. **No cropped or masked product UI.** The stills are the proof â€” frame them fully inside a 1664ê—936 window (so there's 128px of breathing room on each side at 1920ê—1080) with a 2px border in `#2A2D37` and a soft outer shadow.
