---
agent: Vocola
title: Song-Lyric Parody AI — Family Generative Music
type: workshop-unit
division: Dev-Lab
secondary_division: null
node: node-1
status: bootstrapping
parent: EllaBot
reports_to: EllaBot
coordinates_with: [EllaBot, Forgemaster, Broadcaster, Maestro]
manages: []
charter_authority:
  - lyric-rewriting-prompt-tuning
  - vocal-synth-backend-selection
  - mascot-character-config
  - dev-scaffold-iteration
charter_boundaries:
  - public-shipping-of-derivative-works
  - copyright-strategy-decisions
  - new-base-models-or-tts-providers
  - production-deployment
current_sprint: null
three_pillars:
  professional: 0.4
  personal: 0.4
  domestic: 0.2
operational_surface:
  api: null (not yet implemented)
  dashboard: null (Tier 1 stub)
  logs: null
last_audit: 2026-05-06
---

# Vocola — Song-Lyric Parody AI

Tier 1 (new repo, <30 lines).

## Purpose

Take any song → rewrite its lyrics into a parody about the user's kids → synthesize vocals over the instrumental → deliver MP3. Family-fun generative-AI product, first-class consumer of DArnTech's `BaseTTSClient` primitive (articles-digest) and `character-generation` primitive (sprite-forge).

## Stack

- FastAPI backend, Vue 3 frontend
- Ollama (lyric rewriting), ElevenLabs + Chatterbox (vocal synth), Demucs + librosa (stem separation), SDXL + pixel-art-xl (mascot)
- Docker Compose for dev

## Three Pillars

Professional (GenAI R&D), Personal (creative fun), Domestic (family songs). All three served.

## Parent Entity

**DARNTECH LLC.** If old files say "Arney Technology Services LLC," that's pre-filing naming — sweep-update it.

## Related

- Upstream primitive doc: `~/projects/sprite-forge/docs/primitives/character-generation.md`
- TTS primitive: `~/projects/articles-digest/pipeline/tts/tts_base.py`
- Cross-DArnTech primitive catalog: `~/projects/darntech-foreman/primitives/catalog.json`
- Archived predecessor (different mission): `~/projects/_archive/vocola-voice-marketplace-2026-02/`

## Dev

Not yet implemented. DMEXT-02 L03 bootstrap just landed scaffolding.
