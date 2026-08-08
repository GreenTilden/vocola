# Vocola — Project Memory

## Session Status
- **Status**: BOOTSTRAP · scaffold landed via DMEXT-02 L03 (Louie session)
- **Current Focus**: first mascot candidate generation via sprite-forge character-generation primitive v1.0
- **Blockers**: none (actual implementation deferred to post-DMEXT-02; this sprint only lands scaffolding + mascot asset pilot)
- **Next Steps**: mascot HITL at DMEXT-02 L05 arc boundary → implementation sprint (cycle-03 SFSONG-01 candidate?) decides architecture
- **Last Updated**: 2026-04-17 (DMEXT-02 L03)

## Project Identity
- **Name**: Vocola — Song-Lyric Parody AI
- **Repo**: ~/projects/vocola (GitHub: https://github.com/GreenTilden/vocola, pushed 2026-04-17 DMEXT-02 polish phase, public)
- **Stack**: FastAPI + Vue 3/Vite; Ollama for lyric rewriting; ElevenLabs + Chatterbox for vocal synth; Demucs + librosa for stem separation; SDXL + pixel-art-xl LoRA for mascot
- **Ports**: TBD (implementation sprint assigns)
- **Deploy Target**: Docker Compose dev initially; prod decision deferred
- **Parent Entity**: DARNTECH LLC (NOT "Arney Technology Services LLC" — that's archived pre-filing naming)
- **Casey-Jr Deployment**: `xxxxxxxx` — professional pillar, lab-automation domain template (both
  API-immutable, so they are identity). Status/phase/need-counts are volatile:
  `curl -s "$CASEY_BASE"/api/deployments/xxxxxxxx` (+ `/needs`) — the "phase 1 pre_sales"
  transcribed here read `parked` live (corrected cycle-65 L10). session_start activity `1421710d`
  logged 2026-04-17 L03.

## Architecture & Patterns
- **Consumes `BaseTTSClient` primitive** (articles-digest `pipeline/tts/tts_base.py`): supports Chatterbox + ElevenLabs swap via same abstract contract (health_check + synthesize_article + synthesize_short)
- **Consumes `character-generation` primitive** (sprite-forge `docs/primitives/character-generation.md` v1.0): mascot via 11-slot prompt template + SDXL + pixel-art-xl LoRA
- **Will eventually PRODUCE a `lyric-rewriting` primitive** if the parody-swap patterns prove reusable (backlog, cycle-03+)

## Dependencies
- → depends-on: articles-digest (BaseTTSClient primitive)
- → depends-on: sprite-forge (character-generation primitive)
- → depends-on: ComfyUI on the GPU host (LAN, port 8188) for mascot generation
- → depends-on: Ollama on the GPU host for lyric rewriting

## Archived Predecessor
- `~/projects/_archive/vocola-voice-marketplace-2026-02/` — paused MVP from 2026-02 for a consent-first voice reference marketplace. Different mission, different codebase. Did NOT share the current song-lyric-parody scope. Not loaded here — if the voice-marketplace concept ever revives, give it a new name.

## Three Pillars (explicit)
- **Professional**: R&D (TTS primitive consumer, prompt-engineering primitive consumer, novel lyric-rewriting prompt work), shippable GenAI product surface
- **Personal**: creative satisfaction (making songs is fun), family connection ([REDACTED-PRIVATE] + [REDACTED-PRIVATE] audience)
- **Domestic**: makes family songs actually happen with kid names embedded
