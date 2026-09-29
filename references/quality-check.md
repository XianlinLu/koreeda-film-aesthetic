# Final Quality Check

Score each item from 0 to 2: 0 = absent, 1 = weak, 2 = clear. Revise before delivery when the total is below 20/26 or any blocker scores 0.

## Story

- The surface event and relationship change fit in one sentence.
- Every principal character has a concrete want rather than a functional role.
- Action, space, and sound carry most of the emotion.
- Unnecessary explanation, villains, coincidences, and forced twists are removed.
- The ending echoes the opening while leaving interpretive space.

## Continuity — blocker

- Face, apparent age, hair, clothing, and carried objects remain consistent.
- Layout, window light, weather, time, and key-object positions remain consistent.
- Screen direction, eyelines, entrances, exits, and action matches are plausible.
- Every prompt repeats complete anchors instead of relying on “same as above.”

## Image and motion

- Each shot has one primary action that fits its duration.
- Camera movement has a narrative reason; otherwise the camera is locked.
- Every close-up adds information rather than decoration.
- Medium shots, wide shots, and breathing shots preserve a lived-in space.
- No face drift, malformed bodies, invented objects, text, or watermarks remain.

## Sound and rhythm

- Sound alone establishes place and time.
- Dialogue is conversational and contains pauses or unfinished thoughts.
- Music does not tell the audience to feel before the scene earns it.
- The beginning and end of each shot have breathing room.
- Removing any shot would cause a specific loss of information or emotion.

## Canvas delivery — blocker

- Script, storyboard, references, keyframes, videos, and sound are clearly grouped.
- The initial video traces back to its storyboard image and visual references.
- Every extension consumes the immediately preceding verified complete video and returns a longer complete video.
- Every video prompt starts its local timeline at `00:00`; extension requests contain no `ratio` field.
- The final artifact is not assembled from independent clips, loops, freezes, speed changes, or padding.
- The latest verified video duration matches the locked target within the action's declared tolerance.

## Repair order

Fix story causality first, character/location anchors second, single-shot action third, and color, music, and transitions last. Retry one shot no more than twice. If it still fails, shorten the action, reduce the number of visible people, or use a locked camera instead of adding more prompt clauses.
