# GrokMusicVideoPrompt

Structured prompt builder for **Grok Imagine music videos** on the current stack:

- **Image 2.0** — multi-ref stills, precision edits, character/location/prop world lock, sharper title text  
- **Video 1.5** — up to ~15s clips, multi-ref (often up to ~7), voice ref, native 1080p when available, text-to-video + image-to-video, improved **Extend / Extend from frame**

You bring a finished `.mp3` / `.wav`. This static page does **not** read audio — attach the track **in Grok** so it can estimate BPM/structure. Scope can be a full cut or a few looped clips.

## Links

| | |
|---|---|
| **Live tool** | https://medicinalsheep.github.io/grokmusicvideoprompt/ |
| **X** | https://x.com/medicinalsheep |
| **Support** | https://github.com/sponsors/medicinalsheep |
| **Related** | [GrokDevPrompt](https://medicinalsheep.github.io/grokdevprompt/) |

## Who this is for

- Finished song ready  
- Want planned scenes and locked style in Grok Imagine  
- Prefer **image-first + multi-ref + last-frame / Extend-from-frame** continuity over ad-hoc text-to-video  

## How to use

### Option A — Opener in Grok

1. Open the [live site](https://medicinalsheep.github.io/grokmusicvideoprompt/)  
2. **Copy link for Grok**  
3. Paste into Grok (app or grok.com) and **attach your track**  
4. Strongly recommended: form → **Generate Master Prompt** → paste that too  

### Option B — Full master prompt

1. Fill song, **world-lock refs (up to ~7)**, clip length, aspect, scope, audio preference, mood, scenes  
2. Optional: **Load example** (Report Card style; linked X video is older-model reference)  
3. **Generate Master Prompt** → copy into Grok → attach track  

## Flow

1. **Intake** — track, multi-refs, voice, prefs  
2. **BPM pass** — estimate structure from attached track  
3. **Outline** — music-aware plan (no video yet)  
4. **Image 2.0 world lock** — character / location / prop stills  
5. **Title card** — Image 2.0 for crisp text when auto  
6. **Scene still → image-to-video** (Video 1.5)  
7. **Same-scene Extend** (Extend UI / Extend-from-frame)  
8. **Chain boundary** — last-frame screenshot and/or Extend-from-frame for next start  
9. **Assemble** in Grok app/grok.com (not Grok-in-X); honor audio-bed preference  

**Text-to-video** is available but preferred only for B-roll; character scenes stay image-first.

## Clip length (planning defaults)

| Base | Blocks | Notes |
|------|--------|--------|
| 6s | 6 / 12 / 18s | Montage, loops |
| 10s | 10 / 20 / 30s | Default |
| 15s | 15 / 30 / 45s | Longer takes, fewer gens |

Match your surface’s duration control if it differs.

## Form highlights

- Multi-refs / world lock (up to ~7)  
- Voice ref (optional)  
- Aspect: **16:9 · 9:16 · 1:1 · 3:2 · 4:3 · 21:9**  
- Resolution: 720 vs **native 1080p** (quality vs cost)  
- **Audio when assembling** — song only / song + SFX / allow Imagine complementary audio  
- Scope light/medium/full; guided vs full prompt pack  

## Continuity

- **Within a scene:** Video 1.5 Extend (motion-only prompts; no “use last frame” language inside extends)  
- **Between chains:** last-frame **screenshot** as next start image remains the reliable method; use **Extend from frame** when the UI fits  
- Do **not** invent next starts from text alone if you want characters/scene to match  

## Tips

- World-lock with Image 2.0 **before** burning 1080p video budget  
- Free tiers and long form still limited  
- Report Card example on X = earlier model era (style only)  

## Local

Open `index.html` — no build step.

## Icons

| File | Use |
|------|-----|
| `icon/favicon-16x16.png` / `icon-32x32.png` | Favicons |
| `icon/icon-192.png` / `icon-512.png` | High-res / PWA |
| `icon/gmvpicon.png` | Header, Apple touch, social |

## Support

[medicinalsheep](https://x.com/medicinalsheep) · [GitHub Sponsors](https://github.com/sponsors/medicinalsheep)
