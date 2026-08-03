# GrokMusicVideoPrompt

Structured prompt builder for **Grok Imagine** music videos: intake, BPM-aware outline, clip chains, extensions, and last-frame continuity.

You bring a finished `.mp3` / `.wav`. This static page does **not** read your audio — attach the track **in Grok** so it can estimate BPM/structure and plan scene times. Scope can be a full cut or a few looped clips.

## Links

| | |
|---|---|
| **Live tool** | https://medicinalsheep.github.io/grokmusicvideoprompt/ |
| **X** | https://x.com/medicinalsheep |
| **Support** | https://github.com/sponsors/medicinalsheep |
| **Related** | [GrokDevPrompt](https://medicinalsheep.github.io/grokdevprompt/) |

## Who this is for

- Finished song ready
- Want a Grok Imagine music video with planned scenes and locked style
- Prefer **last-frame screenshots** between clip chains for continuity (not a new text-only start image each time)

## How to use

### Option A — Opener in Grok

1. Open the [live site](https://medicinalsheep.github.io/grokmusicvideoprompt/)
2. **Copy link for Grok** (or paste the URL + your own ask)
3. Paste into a Grok chat and **attach your track**
4. Strongly recommended: also fill the form → **Generate Master Prompt** → paste that too (full rules beat a bare URL)

### Option B — Full master prompt

1. Open the live tool (or `index.html` locally)
2. Optional: **Load example** (Report Card style sample)
3. Fill song, assets, clip length, aspect, scope, mood, scenes
4. **Generate Master Prompt** → copy → paste into Grok → attach track

## What you’ll need

- Finished track (`.mp3` / `.wav`) attached in Grok for BPM/structure estimate
- Song name, artist, rough mood
- Optional: multi-image refs, voice ref, lyric notes
- Grok app or grok.com (Imagine for stills/video/combine)

## Form sections

1. **Song details** — name, artist, credits  
2. **Assets & preferences** — multi-refs, voice ref, must-includes, clip length **6/10/15s**, title card, aspect (**16:9 · 9:16 · 1:1 · 3:2 · 4:3 · 21:9**), scope, resolution, guided vs full pack  
3. **Visual direction** — mood + style lock  
4. **Timeline** — runtime, structure, scene breakdown  

## Flow

1. **Intake** — track, refs, prefs  
2. **BPM pass** — Grok *estimates* BPM / sections from the attached track (user can correct)  
3. **Outline** — music-aware plan; no images yet  
4. **Title card** → **Scene 1 start image** → **base clip** → **extensions** (same scene)  
5. **Boundary** — screenshot last frame → next clip start (if continuity)  
6. **Assemble** — confirm order; prefer Grok app / grok.com, not Grok-in-X  

## Clip length (planning defaults)

| Base | Blocks (base / +1 / +2 ext) | Notes |
|------|------------------------------|--------|
| 6s | 6 / 12 / 18s | Montage, loops |
| 10s | 10 / 20 / 30s | Default |
| 15s | 15 / 30 / 45s | Longer takes, fewer gens |

Match the duration control on **your** Grok surface if it differs. Extensions stay in the **same** scene. Between chains: **last-frame screenshot** for continuity; multi-refs help identity.

## Tips

- Scope light/medium/full — video uses more usage than chat  
- Multi-refs + last-frame (not text-only next starts)  
- Voice ref optional; song file is the music bed  
- Aspect ratios include 4:3 and 21:9; if unsupported on your surface, pick the closest  
- Soft **timeline check** on the form is advisory only  

## Local

Open `index.html` — no build step. GitHub Pages serves the same files.

## Icons

| File | Use |
|------|-----|
| `icon/favicon-16x16.png` | Tab 16×16 |
| `icon/icon-32x32.png` | Tab 32×32 |
| `icon/icon-192.png` / `icon-512.png` | High-res / PWA |
| `icon/gmvpicon.png` | Header, Apple touch, social preview |

## Support

[medicinalsheep](https://x.com/medicinalsheep) · [GitHub Sponsors](https://github.com/sponsors/medicinalsheep)
