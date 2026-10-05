# Reference Image Prompts

These were generated first and frozen as the consistency anchors for the whole production. The same files were attached to every clip generation. If a production sheet came back with multiple views, it was kept as-is and reused throughout.

## Fin — character reference

```
Create a clean cinematic character reference image for Fin, a young male student in a science-fiction story. Slim build, warm medium-brown skin, short slightly wavy dark hair, alert kind eyes. Outfit: simple rust-orange overshirt over a charcoal shirt, dark practical trousers, worn dark sneakers, plain cross-body fabric bag. No visible weapon, no futuristic armor, no logos. Show one full-body front view and one smaller three-quarter portrait of the same character in the same image; identical face and clothes in both views. Neutral pale-gray studio background, even light, relaxed standing pose, hands visible. This is a design reference, not a dramatic scene. No text.
```

Result: `assets/characters/fin.jpg` (in production referred to as the **brown** shirt, per the creator's naming).

## Zei — character reference

```
Create a clean cinematic character reference image for Zei, a young male student in a science-fiction story. Lean build, medium-brown skin, straight black hair cut short and slightly uneven, thoughtful dark eyes. Outfit: deep teal overshirt, muted gray-green shirt, charcoal trousers, practical dark shoes, simple digital watch on his left wrist. No armor, no weapon, no logos. Show one full-body front view and one smaller three-quarter portrait of the same character in the same image; identical face and clothes in both views. Neutral pale-gray studio background, even light, relaxed standing pose, hands visible. This is a design reference, not a dramatic scene. No text.
```

Result: `assets/characters/zei.jpg` (in production referred to as the **dark blue** shirt, per the creator's naming).

## Instructor — character reference

```
Create a clean cinematic character reference image for the male physics instructor in a community-run underground classroom. Adult man, around 40, average build, medium olive-brown skin, short dark hair with a little gray at the temples, calm focused expression. Clothes: simple dark green work jacket over a light neutral shirt, practical trousers, no tie, no uniform, no insignia. Show full-body front view and a smaller three-quarter portrait of the same person; same face and clothes. Neutral pale-gray studio background, even light, hands visible. No text.
```

Result: `assets/characters/instructor.jpg`.

## Dzego street — environment reference

```
Wide cinematic environment reference of Hun Min Street in Pafogai Du, Dzego: a lively low-rise electronics and light-industry street, small one- or two-storey storefronts, miniature workshops, trees shading the sidewalk, glowing colored shop lights, stairways leading underground, practical handmade near-future technology, busy but not crowded. Include a small sensor shop beside a shop selling reflective anti-transmission foil, but do not include readable signs or text. Daylight, inviting and lived-in, grounded science fiction, no skyscrapers, no flying cars, no cyberpunk overload.
```

Result: `assets/environments/dzego-street.jpg`.

## Dzego classroom — environment reference

```
Wide cinematic environment reference of a hidden community physics classroom in Dzego. Modest underground room, rows of simple chairs, thick hastily applied reflective anti-transmission foil on walls, cheerful hand-painted cartoon pig holding a calculator and hamster holding a green chemistry vial, trees and blue sky painted behind them, blank central poster area for text to be added later. Practical watch devices, an ordinary classroom made secure through improvised materials. No people, no legible text, no dramatic damage.
```

Result: `assets/environments/dzego-classroom.jpg`.

## Which references to attach per shot

- Most clips: Fin + Zei + the relevant environment.
- Classroom scenes: Fin + Zei + classroom.
- Instructor shots: instructor + classroom; include Fin or Zei only if clearly visible.
- If the generation mode allows fewer references, prioritize the character or location most important to that shot.
