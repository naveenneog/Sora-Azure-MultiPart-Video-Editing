# Sora × Azure — Multi-Part Video Editing

**The Lamp & the Machine** — turning Karnataka's *Togalu Gombeyaata* (leather
shadow-puppet theatre) into an AI film studio with **Sora 2** and **Azure AI**,
and telling the story of **Kempegowda**, the founder of Bengaluru.

🔥 **Read it:** https://naveenneog.github.io/Sora-Azure-MultiPart-Video-Editing/

## What's inside

A build-log blog (single themed page, `index.html`) covering:

- **Act I – The Images** — Sora 2 shadow-puppet generation, a locked *Style Bible*,
  and killing cross-scene drift.
- **Act II – The Voice** — discovering Sora narrates in whatever language you name
  (it was Kannada!), then re-voicing the film in English **while keeping the original
  music/ambience** via Demucs source separation.
- **Act III – The Cast** — multi-voice narration (male / female / both + a unison
  finale) with Azure neural voices, and the ultra-natural **DragonHD** flagship cut.
- **The Four Voices** — the same film with four different narrations, side by side.
- **The Craft Notes** — every step-by-step change made to the two skills.

## The four cuts

| Cut | Narration | Music |
|-----|-----------|-------|
| Sora-native English | generated per clip by Sora | Sora original |
| Azure – single voice | one Azure neural narrator | Sora, retained (Demucs) |
| Multi-voice + styles | male + female + unison finale | Sora, retained |
| **DragonHD** (flagship) | Azure DragonHD voices | Sora, retained |

> Videos here are compressed 480p previews, self-hosted under `assets/video/`.
> To swap in YouTube: replace each `<video …>` with a responsive `<iframe>` embed.

## Pipeline

Sora 2 · gpt-4o-transcribe · Azure AI Speech (en-IN neural + DragonHD) ·
Demucs (htdemucs) · FFmpeg · Python 3.14 — all on Azure with Microsoft Entra (AAD) auth.

## Reusable skills produced

- **`togalu-gombe-video`** — heritage shadow-puppet film generator (Sora 2 + stitching).
- **`voice-dub`** — re-voice any video with Azure neural voices while keeping its music
  (one-speaker & multi-speaker workflows).
