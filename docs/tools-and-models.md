# Tools and Models

## Video generation

- **Muse Video** (Meta's media generation model), via the `media.generate_video` pipeline.
- Input: text prompt + reference images (ordered text/image entries). No audio input — clips come with synthesized sound matching the described mood.
- Output: ~10-second clips, 16:9. Longer scenes were split across multiple clips.
- Visual context can be carried across calls via `snapshot_id`, though this production relied mainly on re-attaching the frozen reference images.

## Dialogue / voiceover

- **TTS CLI** (`tts speak` for single lines, `tts synthesize-script` for multi-speaker scripts), MP3 output.
- Each character's line was synthesized individually with their fixed voice and concatenated with `ffmpeg` (0.5–0.6s pauses between lines). Unison lines were recorded per-voice and mixed with `ffmpeg amix`.
- Voice IDs (see `docs/voice-guide.md` for the casting rationale):
  - Fin → `avocado_v2:ronan`
  - Zei → `avocado_v2:chip`
  - Instructor → `avocado_v2:TruthTeller`
  - Organizer → `avocado_v2:NoSugar`

## Assembly

- **CapCut** — timeline assembly, dialogue layering, subtitles/graphics, music, final export (1920×1080, 24fps). See `docs/capcut-assembly.md`.

## Planning

- Initial prompt guide drafted with **Duck.ai** (included in `prompts/` as the base scene plan; adapted during production as described in `docs/workflow.md`).
- Orchestration, bookkeeping, and repo assembly by **Muse** (Meta).

## Not redistributed

Per the bounty terms: no third-party software, commercial tools, foundation models, or stock assets are included here — only this production's own prompts, scripts, reference images, audio, and documentation.
