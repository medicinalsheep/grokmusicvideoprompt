# GrokMusicVideoPrompt

Turn a finished track into a consistent **Grok Imagine** music video.

You have an `.mp3` or `.wav` ready and want planned scenes, a locked visual style, and stitchable clips — this tool builds the structured master prompt that drives that workflow.

## Links

| | |
|---|---|
| **Live tool** | https://medicinalsheep.github.io/grokmusicvideoprompt/ |
| **X** | https://x.com/medicinalsheep |
| **Support** | https://github.com/sponsors/medicinalsheep |
| **Related** | [GrokDevPrompt](https://medicinalsheep.github.io/grokdevprompt/) |

## Who this is for

- You already finished the song (audio file ready)
- You want a music video made with Grok Imagine (image + video)
- You care about consistency: same characters, lighting, and scene handoffs you can edit to the track

## How to use

### Option A — Guided in Grok (easiest)

1. Open the [live site](https://medicinalsheep.github.io/grokmusicvideoprompt/)
2. Click **Copy link for Grok** (or paste the URL yourself)
3. Paste into a Grok chat — the opener asks Grok to run intake → outline → step-by-step generation

### Option B — Build the prompt yourself

1. Open the live tool (or open `index.html` locally)
2. Optionally click **Load example** for the Report Card sample (classroom satire from a finished Grok MV)
3. Fill or tweak song details, assets, clip length, workflow style, mood, and scenes
4. **Generate Master Prompt** → **Copy to Clipboard** → paste into Grok

## What you’ll need

- Finished track (`.mp3` / `.wav`) for the final edit — Grok makes visuals; you sync audio in your editor
- Song name, artist, and a rough mood / aesthetic
- Optional: reference images, character art, logos, lyric notes
- A video editor (CapCut, DaVinci Resolve, Premiere, etc.)

## Form sections

1. **Song details** — name, artist, credits  
2. **Starting assets & preferences** — optional pre-fill for intake (refs, must-includes, **6s / 10s / 15s** clip length, title card mode, **guided vs full prompt pack**)  
3. **Visual direction** — mood + style lock  
4. **Scene & timeline** — runtime, structure, scene breakdown (placeholders update with clip length)

## Intake (before the outline)

Grok asks (or confirms what you pre-filled):

1. Starting images / graphics?
2. Must-include notes or lyric moments?
3. Preferred clip length: **6s**, **10s**, or **15s**
4. Target runtime
5. Title card: auto black/white text, or your own art?

## Clip length

| Base | Scene blocks (base / +1 ext / +2 ext) | Best for |
|------|----------------------------------------|----------|
| 6s   | 6 / 12 / 18s                           | Snappy cuts, more scene changes |
| 10s  | 10 / 20 / 30s                          | Default — clean 30s scenes with two extensions |
| 15s  | 15 / 30 / 45s                          | Longer takes, fewer chains |

- Extensions stay in the **same** scene (no last-frame language in extension prompts)
- New scenes start when a clip chain ends
- Between scenes: **last frame** of chain A → start image for chain B

## Workflow style

| Mode | Behavior |
|------|----------|
| **Guided step-by-step** (recommended) | One image or video prompt at a time; wait for approval between steps |
| **Full prompt pack** | After outline approval, all copy-ready image + base + extension prompts in one package |

### Guided flow

1. **Intake** — assets, notes, clip length, title card  
2. **Outline only** — scene plan with base + extension counts (no images yet)  
3. **Title card** — still only  
4. **Scene 1 start image only** — do not pre-make later keyframes  
5. **Base video prompt** — one copy-ready base-length prompt from that image  
6. **Extension prompts** — one at a time (e.g. two extensions for a 30s scene on 10s base)  
7. **Boundary** — save last frame → next scene start image → repeat  

### Full pack flow

1. **Intake** → **Outline** (approve)  
2. Deliver **full prompt pack** for every scene  
3. Generate assets from the pack on request  

## Tips & edge cases

- **No audio in Grok** — export clips, then lay your track underneath in an editor
- **10s** is the practical default; use **15s** for longer continuous shots, **6s** for faster montage
- **Stitch carefully** — always capture last frame at scene boundaries
- **Load example** fills a **Report Card** demo (~1:37, 10s guided) and reveals a link to the [finished video on X](https://x.com/medicinalsheep/status/2081793904970731770?s=20) (made with an **earlier process** — style reference only, not a 1:1 guide to this tool’s current prompts)

## Local

Open `index.html` in a browser — no build step required. Static site; GitHub Pages serves the same file.

## Icons

Assets live in `icon/`:

| File | Use |
|------|-----|
| `favicon-16x16.png` | Browser tab (16×16) |
| `icon-32x32.png` | Browser tab (32×32) |
| `icon-192.png` / `icon-512.png` | PWA / high-res favicon |
| `gmvpicon.png` | Header logo, Apple touch icon, social preview |
| `gmvpicon.tif` | Source master (not used on the web) |

## License / support

Personal project by [medicinalsheep](https://x.com/medicinalsheep). If this helps your workflow: [GitHub Sponsors](https://github.com/sponsors/medicinalsheep).
