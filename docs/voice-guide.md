# Voice Guide

Every character keeps **one fixed voice** across all scenes. Voices were never baked into the video clips (AI speech drifts between generations) — dialogue was recorded separately and layered in CapCut.

## Cast

### FIN — `avocado_v2:ronan`
Young male voice, warm mid-range, open and friendly, quick but not rushed, natural conversational delivery. Fin is warm and curious, lightly teasing with Zei, steady and reassuring under pressure ("I've got you. Stay still.").

### ZEI — `avocado_v2:chip`
Young male voice, slightly lower and more measured than Fin, thoughtful, dry humor, calm under pressure, restrained emotion rather than a heroic tone. Zei is pleased but understated, practical ("The lesson location changed. We need to sync the new proof."), quietly shaken after the blast.

### INSTRUCTOR — `avocado_v2:TruthTeller`
Adult male voice, calm mid-low register, patient teacherly rhythm, clear enunciation. Reassuring during the emergency without shouting ("Is anyone hurt? Tell me now.").

### ORGANIZER — `avocado_v2:NoSugar`
Adult voice, practical and composed, concise delivery. Gives the room change as routine information, not a dramatic warning ("Change of room. Upstairs, opposite side.").

## Recording method

1. One line per synthesis call, one speaker per call — voices are never in the same recording except intentionally.
2. Lines joined with `ffmpeg`, 0.5–0.6s silence between speakers.
3. Unison line ("Dzego will rise again", scene 12): Fin and Zei each recorded separately, then mixed with `ffmpeg amix` so both voices are heard together.

## If you recast

Replace the voice ID in the mapping above and re-run every line for that character — never mix old and new recordings of the same character.
