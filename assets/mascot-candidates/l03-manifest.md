---
artifact: Vocola mascot L03 candidate manifest
authored: 2026-04-17
authored_by: Louie DMEXT-02 L03 [actor:autonomous_agent_with_hitl]
sprint: DMEXT-02
loop: L03
primitive_consumed: sprite-forge/docs/primitives/character-generation.md v1.0
workflow: workflows/vocola-mascot-l03.json (1.0.0, slot-swap from barry-comfyui-canonical v2.1.0)
---

# Vocola Mascot — L03 Candidate Gallery

First character-generation primitive port outside sprite-forge. Three candidates generated at known-good seeds per primitive v1.0 guidance (1001 / 1002 / 1004; avoided seed 1003 which triggers sprite-sheet mode globally).

## Candidates

| Seed | File | Size | Wall-clock | Notes |
|---|---|---|---|---|
| 1001 | `vocola_mascot_l03_seed001001.png` | 737 KB | 8.0s | Prompt-obedient seed per primitive v1.0 (stronger chibi adherence expected) |
| 1002 | `vocola_mascot_l03_seed001002.png` | 415 KB | 6.0s | Style-obedient seed per primitive v1.0 (LoRA + archetype defaults dominate) |
| 1004 | `vocola_mascot_l03_seed001004.png` | 656 KB | 6.0s | Backup known-good seed |

Size range 415-737 KB is below SFGEN-02's 937-1029 KB Barry range — unclear whether this signals simpler/cleaner output or lower detail. HITL review at L05 arc boundary.

## Identity slots (per workflow v1.0)

- **subject**: young cheerful songsmith with retro microphone, playful family-music parody performer
- **hair**: curly tousled bright hair
- **accessory_eyes**: big excited eyes (no glasses, per DuckTales-adjacent family aesthetic)
- **accessory_ears_or_prop**: holding retro microphone with swirl cord and small music-note stickers
- **wardrobe**: colorful graphic t-shirt with treble-clef print, rainbow suspenders, bright patterned pants
- **expression**: open mouth mid-song big grin
- **aesthetic**: cartoon family-karaoke musical performer vibe

## Template slots (unchanged from primitive)

`pixel art mascot character, clean silhouette on white background, full body standing pose, small chibi body with large round head, ..., sega genesis era sprite style`

## HITL decision points for L05 arc boundary

- **D1**: Canonical Vocola mascot selection (pick one of 3, or request reshoot)
- **D2**: Microphone-as-prop vs mic-stand-with-body — primitive v1.0 is humanoid-bounded; mic is an accessory, not the subject. If operator wants Vocola to BE a microphone character (non-humanoid), that's a distinct primitive / SFGEN-0X follow-up.
- **D3**: Kid-audience acceptability — does a young kid respond to this character visually? Family HITL data is a validated ranking signal per charter v0.1.6 (HITL = ground truth).
- **D4**: Port lessons for the Extensions-page cross-family topology claim — cross-repo adaptation evidence for primitives/catalog.json family #4.

## Expected failure modes (per primitive v1.0 guardrails)

- ~50-60% clean-bg rate — chop with rembg post-hoc if needed
- Wardrobe color drift (LoRA overrides specific colors) — may drift toward LoRA defaults
- Proportion drift on young/songwriter archetype — archetype may override chibi cue at some seeds
- Identity-cluster = everything — microphone + colorful wardrobe should hold character identity even if other markers drift

## Provenance

- **Primitive**: sprite-forge character-generation v1.0 (Huey SFGEN-02 L13)
- **Workflow lineage**: barry-comfyui-canonical v2.1.0 → vocola-mascot-l03 v1.0.0 (identity slot swap only; all template slots + generation params inherited unchanged)
- **Generation host**: ComfyUI on the GPU host (LAN, port 8188, RTX 5070 Ti)
- **ComfyUI version**: 0.14.1 · PyTorch 2.10.0+cu128
- **Cross-family Extensions evidence**: first primitive port outside sprite-forge — feeds catalog.json `cross_repo_adaptations[]` for family_id=`prompt-engineering` at DMEXT-02 L06
