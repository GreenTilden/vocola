# Vocola

<p align="center">
  <img src="assets/canonical/vocola_mascot_canonical.png" alt="Vocola mascot — a cheerful chibi songsmith with tousled orange hair, green overalls, holding a retro microphone, rainbow brand frame" width="280" />
</p>

**Song-lyric parody AI.**

> Take any song. Rewrite the lyrics about your kids.

Vocola is a family-fun generative-AI product that takes a song (or any vocal track) and rewrites its lyrics into a personalized parody — songs about your kids, the cat, whatever is making the household laugh today. Uses ElevenLabs / Chatterbox TTS for vocal synthesis over the instrumental stem.

## Status

**Bootstrap — DMEXT-02 L03 · 2026-04-17.** Scaffold + mascot landed. Landing page live at `public/index.html`. Song pipeline implementation deferred to a dedicated cycle-03 sprint.

Canonical mascot: seed 1001 (operator pick candidate; HITL override at any time — alternatives in `assets/mascot-candidates/`).

## Tech Stack

| Layer | Technology | Notes |
|---|---|---|
| Lyric rewriting | Ollama local LLM (Node 1) | Lyric preservation + parody-swap patterns |
| Vocal synthesis | ElevenLabs API + Chatterbox | Cross-backend via `BaseTTSClient` primitive (articles-digest origin) |
| Audio processing | Demucs (stem separation) + librosa | Remove original vocals, lay new vocals over instrumental |
| Backend | FastAPI (port TBD) | REST endpoints for job submission + status |
| Frontend | Vue 3 + Vite (port TBD) | Upload song, enter family names, get MP3 |
| Mascot + brand | sprite-forge character-generation primitive v1.1 | `assets/canonical/vocola_mascot_canonical.png` + `public/index.html` landing page |

## Three Pillars

- **Professional** — GenAI product, cross-project TTS + prompt-engineering primitive consumer, R&D-qualifying
- **Personal** — creative work (making songs is fun); validates voice-cloning + lyric-rewriting patterns
- **Domestic** — makes family songs actually happen; the kids love personalized music

## Parent Entity

Product of **DARNTECH LLC**.

## Related Repos

- `~/projects/_archive/vocola-voice-marketplace-2026-02/` — previous paused MVP for a "consent-first voice reference marketplace." Archived 2026-04-17 to free this name for the song-lyric parody mission. Different project, different mission.
- `~/projects/beakly` (formerly LornaCo) + its internal product `Cantor` — the ethically-licensed AI voice marketplace. Separate project from Vocola; shares TTS infrastructure but different product goal. Renamed 2026-04-17 to free the Vocola name.
- `~/projects/articles-digest` — `BaseTTSClient` primitive Vocola consumes (Chatterbox + Kokoro backends already implemented)
- `~/projects/sprite-forge` — character-generation primitive v1.1 Vocola's mascot uses (canonical pick from L03 pilot: seed 1001 chibi songsmith)
- `~/projects/darntech-foreman/primitives/catalog.json` — cross-DArnTech primitive registry (Vocola is both a consumer of TTS + prompt-engineering primitives and a candidate future producer of a parody-lyric-rewriting primitive of its own)
