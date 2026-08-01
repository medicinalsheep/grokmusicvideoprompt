# GrokMusicVideoPrompt

Turn a finished track into a consistent **Grok Imagine** music video.

You have an `.mp3` or `.wav` ready and want planned scenes, a locked visual style, and clips you can extend, loop, or combine in Grok — full cut or a lighter token budget. This tool builds the structured master prompt that drives that workflow.

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
- You care about consistency (last-frame screenshots between chains) more than reinventing each start image from text

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

- Finished track (`.mp3` / `.wav`) — the song the music video is built for
- Song name, artist, and a rough mood / aesthetic
- Optional: multi-image refs (character/location), voice ref, lyric notes
- Grok Imagine for stills, clips, extensions, and combining the video sequence

**Note:** This static page does not read your audio file. **In Grok chat**, attach the track so Grok can estimate **BPM** and rough structure, then plan scene times from that.

## Form sections

1. **Song details** — name, artist, credits  
2. **Starting assets & preferences** — multi-refs, optional voice ref, must-includes, **6s / 10s / 15s** clip length, title card, aspect ratio, **scope/compute**, resolution, **guided vs full pack**  
3. **Visual direction** — mood + style lock  
4. **Scene & timeline** — runtime, structure, scene breakdown (placeholders update with clip length)

## Intake (before the outline)

Grok asks (or confirms what you pre-filled):

1. Attach track for **BPM + structure** analysis (or confirm already attached)
2. Multi-image refs to attach in Imagine?
3. Optional voice ref (or none)?
4. Must-include notes / lyric moments?
5. Preferred clip length: **6s**, **10s** (default), or **15s**
6. Target runtime (prefer measured length from file)
7. Title card: auto black/white text, or your own art?
8. Aspect ratio (**before first image**): **16:9**, **9:16**, **1:1**, or **3:2**
9. Scope / compute: light / medium / full
10. Resolution preference if available

Then: **BPM pass** → music-aware outline → generate

## Clip length

| Base | Scene blocks (base / +1 ext / +2 ext) | Best for |
|------|----------------------------------------|----------|
| 6s   | 6 / 12 / 18s                           | Montage, loops, token thrift |
| 10s  | 10 / 20 / 30s                          | Default — clean 30s scenes with two extensions |
| 15s  | 15 / 30 / 45s                          | Longer takes, fewer generations |

Align with the **duration slider** on your Grok surface if options differ.

- Extensions stay in the **same** scene (no last-frame language in extension prompts)
- New scenes start when a clip chain ends
- **Consistency layers:** multi-image refs (identity) + **last-frame screenshot** between chains (shot flow) — do **not** text-prompt a new start still if you want continuity

## Workflow style

| Mode | Behavior |
|------|----------|
| **Guided step-by-step** (recommended) | One image or video prompt at a time; wait for approval between steps |
| **Full prompt pack** | After outline approval, all copy-ready image + base + extension prompts in one package |

### Guided flow

1. **Intake** — track attach, refs, notes, clip length, title card  
2. **BPM pass** — Grok estimates BPM / sections from the track  
3. **Outline only** — music-aware scene plan with base + extension counts (no images yet)  
4. **Title card** — still only  
5. **Scene 1 start image only** — do not pre-make later keyframes  
6. **Base video prompt** — one copy-ready base-length prompt from that image  
7. **Extension prompts** — one at a time (e.g. two extensions for a 30s scene on 10s base)  
8. **Boundary** — screenshot last frame → next clip start image (if continuity) → repeat  
9. **Before assembly** — confirm order of operations, then combine / loop as you prefer  

### Full pack flow

1. **Intake** → **Outline** (approve)  
2. Deliver **full prompt pack** for every scene  
3. Generate assets from the pack on request  
4. Confirm assembly order, then mix in Grok  

## Tips & edge cases

- **Scope / compute** — light / medium / full; video is expensive on shared weekly pools
- **Use Grok tab or Grok app** when mixing — not Grok inside the **X** tab
- **Multi-refs + last-frame** — re-attach character/location refs; screenshot last frame between chains
- **Voice ref** — optional for speech; song file remains the music bed
- **BPM in Grok** — attach the track in chat; Grok analyzes BPM/structure and plans scene times (this page only builds the prompt)
- **10s** default; **15s** fewer gens; **6s** montage/loops
- **Load example** — Report Card (~1:32, 10s guided)
- **Copy link for Grok** — app/web, intake, BPM-on-track-attach, multi-ref + last-frame
- Soft **timeline check** on scene ranges vs target runtime

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
