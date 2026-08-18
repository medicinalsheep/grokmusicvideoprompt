# GrokMusicVideoPrompt

Structured prompt builder for **Grok Imagine** music videos on the current stack:

- **Image 2.0** (Quality Mode) — multi-ref stills, precision edits, Smart Resize, world lock (character / locations / props), sharp title text  
- **Video 1.5** — ~6–15s by plan, multi-ref (often up to ~7), voice ref, native 1080p when available, image-to-video + text-to-video, Extend / Extend from frame  

You bring a finished `.mp3` / `.wav`. This page does **not** read audio — attach the track **in Grok** for a BPM/structure estimate. Scope can be a full cut or a few looped clips.

## Links

| | |
|---|---|
| **Live tool** | https://medicinalsheep.github.io/grokmusicvideoprompt/ |
| **X** | https://x.com/medicinalsheep |
| **Support** | https://github.com/sponsors/medicinalsheep |
| **Related** | [GrokDevPrompt](https://medicinalsheep.github.io/grokdevprompt/) |

## Flow

1. **Intake** — track, multi-refs, voice, **negative / avoid list**, prefs  
2. **BPM pass** — estimate structure from attached track  
3. **Outline** — music-aware plan  
4. **Image 2.0 world lock** — character / location / prop stills (+ Smart Resize to video ratio if needed)  
5. **Title card** — Image 2.0 for crisp text when auto  
6. **Scene still → image-to-video**  
7. **Same-scene Extend** (Extend UI / Extend-from-frame)  
8. **Chain boundary** — save last frame and/or Extend-from-frame for next start  
9. **Assemble** — Grok app/grok.com and/or an external editor for longer cuts  

**Text-to-video** = B-roll. Character scenes stay **image-first**.

## Aspect ratios

**Image 2.0 Smart Resize:** `1:2` · `9:16` · `2:3` · `3:4` · `1:1` · `4:3` · `3:2` · `16:9` · `2:1`  

Also offered: **`21:9`** ultrawide (fall back to `2:1` / `16:9` if unsupported).  

Video may expose a subset — lock one ratio for the project and Smart Resize stills into it when needed.

## Clip length (planning defaults)

| Base | Blocks | Notes |
|------|--------|--------|
| 6s | 6 / 12 / 18s | Montage; also common plan max on lower tiers |
| 10s | 10 / 20 / 30s | Default |
| 15s | 15 / 30 / 45s | Longer takes when your plan allows |

## Continuity

- **Within a scene:** Extend Video (motion-only prompts; no “use last frame” language inside extends)  
- **Between chains:** save/screenshot last frame as next start **and/or** Extend-from-frame  
- Do **not** invent next starts from text alone for locked characters  

## Negative prompts

Optional short avoid list (extra limbs, watermarks, style drift, etc.). The master prompt applies it on stills, title cards, and clips. Keep lists tight — Imagine responds better to short exclusions.

## Form highlights

- World lock / multi-refs  
- Voice ref + audio bed preference (song only / song + SFX / Imagine complementary)  
- Negative / avoid list  
- Full aspect set above  
- 720 vs native 1080p trade-off  
- Scope light/medium/full · guided vs full prompt pack  

## How to use

1. Open the [live tool](https://medicinalsheep.github.io/grokmusicvideoprompt/)  
2. Fill the form (or **Load example**) → **Generate Master Prompt** → paste into Grok  
3. Attach your track · work in **Grok app / grok.com** (not Grok-in-X)  
4. Or **Copy link for Grok** as a short opener (still paste the master prompt for full rules)  

Report Card example video on X = **older model era** (style reference only).

## Local

Open `index.html` — no build step.

## Support

[medicinalsheep](https://x.com/medicinalsheep) · [GitHub Sponsors](https://github.com/sponsors/medicinalsheep)
