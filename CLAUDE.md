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
