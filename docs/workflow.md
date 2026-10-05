# Production Workflow

How the twelve Chapter 2 scenes were produced, step by step. Written so another creator can follow or adapt the process.

## 1. Plan the sequence

The chapter was broken into twelve short scenes, each describable as a single camera setup with a clear action. Each scene got:

- a shot description (framing, camera move, action),
- a list of which reference images to attach,
- dialogue with speaker labels (newly written for this adaptation),
- an audio description (ambience and effects baked into the clip),
- the common visual-continuity prompt appended verbatim (see `prompts/common-visual-prompt.md`).

The full plan lives in `prompts/scene-prompts.md`.

## 2. Reference images first

Before any video clip, character and environment reference images were produced and frozen:

- **Fin** — teenage boy, brown shirt, messenger bag (`assets/characters/fin.jpg`)
- **Zei** — teenage boy, dark blue shirt, digital watch (`assets/characters/zei.jpg`)
- **Instructor** — adult man, dark green jacket (`assets/characters/instructor.jpg`)
- **Dzego street** and **Dzego classroom** environments (`assets/environments/`)

Every clip generation attached the relevant references. Reusing the same reference images across all shots is the main mechanism for face/clothing consistency. The prompts used to create them are in `prompts/reference-image-prompts.md`.

## 3. Generate one clip per scene

Each scene was generated individually as a ~10-second clip with its references attached. Two things were appended to every scene prompt beyond the shot description:

1. **A context block** identifying each attached image (which one is the environment, who each character is) so the generator doesn't confuse them.
2. **A speaking-motion direction** for dialogue scenes: subtle, natural lip movement with small restrained mouth shapes — never exaggerated — so the separately recorded dialogue sits naturally underneath.

## 4. Record dialogue separately

AI-generated speech changes between clips, so dialogue was never baked into the video generation. Instead:

- Each character was assigned **one fixed voice**, used for every line across all scenes (see `docs/voice-guide.md`).
- Each line was synthesized **individually** (one speaker per recording) and joined with short pauses — this prevents voices blending into each other.
- For the final scene's unison line ("Dzego will rise again"), Fin and Zei each recorded it separately and the two recordings were mixed together.

The dialogue audio files live in `scenes/sceneNN/` next to their clips, and the full script is in `dialogue/full-script.md`.

## 5. Regeneration policy

When a clip came out wrong, it was regenerated rather than accepted. Regenerations during this production:

| Scene | Problem | Fix |
|-------|---------|-----|
| 4 | Lip movement looked off | Regenerated with subtler speaking-motion direction |
| 7 | Instructor only seen from behind | Reframed so his face is visible asking the question |
| 8 | The two characters' features got muddled | Added explicit "two clearly different people, do not blend features" direction |
| 10 | Classroom looked empty | Regenerated with classmates present at their desks |
| 11 | Students were touching their watches; voices felt blended | Regenerated with no watch-touching; each voice recorded separately |

If a character drifts in your own generations, regenerate that clip with the clearest character reference attached and simplify the camera move.

## 6. Assemble in CapCut

Clips and dialogue audio were layered in CapCut. Assembly notes: `docs/capcut-assembly.md`.

## 7. Known limitations

- **No true lip sync.** The video generator cannot take audio input, so lips can't be animated against the dialogue track. Mitigation: restrained mouth movement in the clips + nudging dialogue timing in CapCut.
- **Face drift between clips is possible.** Anchoring on reference images keeps it close; regeneration fixes the misses.
- **The generator can't be fully directed.** Outputs were QC'd by eye; the person assembling in CapCut is the final quality gate.
- **No readable text in generations.** Signs, watch faces, and posters were kept blank/abstract; wording was added later in CapCut.
