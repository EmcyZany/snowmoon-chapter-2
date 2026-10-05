# Snowmoon — Chapter 2 Audiovisual Adaptation

An AI-assisted film adaptation of **Chapter 2** of *Snowmoon*, the science-fiction novel by Vitalik Buterin (published under GPL v3).

Created as an entry for the **"Bring Snowmoon to Life"** bounty: pick a scene from Snowmoon and turn it into a finished audiovisual piece, with the production pipeline open-sourced so other creators can learn from it and build on it.

## The story

Fin and Zei walk down Hun Min Street in Pafogai Du, Dzego. A changed lesson location reroutes them to a foil-lined hidden classroom, where the instructor teaches thermodynamics with two jars of gas — a lesson about heat, uncertainty, and information. A last-minute room change turns out to be what saves the class when a blast hits a nearby room. It ends quietly: *"Dzego will rise again."*

Twelve scenes, each generated as a short clip (~10 seconds) and assembled in CapCut:

| # | Scene | Clip |
|---|-------|------|
| 1 | Hun Min Street — establishing shot | `scenes/scene01/` |
| 2 | Fin and Zei talk as they walk | `scenes/scene02/` |
| 3 | The security drone passes | `scenes/scene03/` |
| 4 | The changed lesson location | `scenes/scene04/` |
| 5 | The last-minute room change (stairwell) | `scenes/scene05/` |
| 6 | Inside the improvised secure classroom | `scenes/scene06/` |
| 7 | The two jars: entropy made visual | `scenes/scene07/` |
| 8 | The lesson's idea lands | `scenes/scene08/` |
| 9 | A shared moment before the blast | `scenes/scene09/` |
| 10 | The nearby blast and classroom damage | `scenes/scene10/` |
| 11 | Fin helps Zei; the danger becomes real | `scenes/scene11/` |
| 12 | The final line | `scenes/scene12/` |

## What's in this repo

- `prompts/` — every prompt used: the common visual-continuity block, the character/environment reference-image prompts, and all 12 scene prompts, plus notes on the per-scene adaptations applied during generation.
- `dialogue/` — the full dialogue script with speaker labels, and the voice assigned to each character.
- `assets/` — character reference sheets, environment references, and scene reference frames.
- `scenes/` — per-scene folders (prompt used, dialogue audio). Final video clips are assembled in CapCut — see `docs/capcut-assembly.md`.
- `docs/` — how it was made: `workflow.md` (full process), `tools-and-models.md`, `voice-guide.md`, `capcut-assembly.md`.

## Finished video

🎬 *The finished cut will be linked here once it is assembled and published.*

## How it was made (short version)

1. Character and environment reference images were created first and reused as anchors for every shot — the single biggest factor in keeping faces and clothes consistent.
2. One clip per scene, generated with the reference images attached and the common visual-continuity prompt appended.
3. Dialogue was recorded separately with a fixed voice per character and layered over the clips in CapCut (AI-generated speech drifts between clips, so voices were never baked into the video generation).
4. Full detail: [`docs/workflow.md`](docs/workflow.md).

## Reuse

Another creator can take the prompts in `prompts/`, swap in their own character references, and generate their own version of these scenes — or continue the story into Chapter 3. See [`docs/workflow.md`](docs/workflow.md) for the regeneration policy used when a clip came out wrong.

## License

GPL-3.0 — see [LICENSE](LICENSE). *Snowmoon* itself is published under GPL v3; this adaptation's production materials are released in the same spirit.

## Disclaimer

Character designs and dialogue are original interpretations written for this adaptation, not claims about details specified in the novel. The characters' exact appearances and clothing are this production's consistent design choices.
