# Vocola

**Song-lyric parody AI.**

> Take any song and replace the lyrics with ones about your kids.

Vocola is a family-fun generative-AI product that takes a song (or any vocal track) and rewrites its lyrics into a personalized parody — songs about [REDACTED-PRIVATE], [REDACTED-PRIVATE], the cat, whatever's making the household laugh today. Uses ElevenLabs / Chatterbox TTS for vocal synthesis.

## Status

**Bootstrap — DMEXT-02 L03 · 2026-04-17.** First scaffold + first mascot-candidate generation pending.

## Tech Stack

| Layer | Technology | Notes |
|---|---|---|
| Lyric rewriting | Ollama local LLM (Node 1) | Lyric preservation + parody-swap patterns |
| Vocal synthesis | ElevenLabs API + Chatterbox | Cross-backend via `BaseTTSClient` primitive (articles-digest origin) |
| Audio processing | Demucs (stem separation) + librosa | Remove original vocals, lay new vocals over instrumental |
| Backend | FastAPI (port TBD) | REST endpoints for job submission + status |
| Frontend | Vue 3 + Vite (port TBD) | Upload song, enter family names, get MP3 |
| Asset generation | sprite-forge character-generation primitive v1.0 | Vocola mascot sprites (DMEXT-02 L03 pilot) |

## Three Pillars

- **Professional** — GenAI product, cross-project TTS + prompt-engineering primitive consumer, R&D-qualifying
- **Personal** — creative work (making songs is fun); validates voice-cloning + lyric-rewriting patterns
- **Domestic** — makes family songs actually happen; [REDACTED-PRIVATE] + [REDACTED-PRIVATE] love personalized music

## Parent Entity

Product of **DARNTECH LLC** (not Arney Technology Services — that's old pre-LLC-filing naming; if you find it in old files, sweep-update it).

## Related Repos

- `~/projects/_archive/vocola-voice-marketplace-2026-02/` — previous paused MVP for a "consent-first voice reference marketplace." Archived 2026-04-17 to free this name for the song-lyric parody mission. The voice-marketplace concept is dormant but not killed; if it revives, give it a different name.
- `~/projects/articles-digest` — `BaseTTSClient` primitive Vocola consumes (Chatterbox + Kokoro backends already implemented)
- `~/projects/sprite-forge` — character-generation primitive v1.0 Vocola's mascot uses
- `~/projects/darntech-foreman/primitives/catalog.json` — cross-DArnTech primitive registry (Vocola is both a consumer of TTS + prompt-engineering primitives and a candidate future producer of a parody-lyric-rewriting primitive of its own)
