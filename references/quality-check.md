# Final Quality Check

Score each item from 0 to 2: 0 = absent, 1 = weak, 2 = clear. Revise before delivery when the average is below 1.5 or any blocker scores 0.

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

## Character assets and audio — blocker

- Every character has a dedicated asset node, and every asset image contains exactly one character identity.
- No second person appears in the background, reflection, poster, screen, photograph, or alternate slot of a character asset.
- Each generated character asset is connected to its source or generation node and explicitly confirmed by the user before dependent media begins.
- Character audio exists only when requested and only after that character asset is approved.
- Every audio node receives exactly its matching approved character asset, and both the canvas edge and returned audio output are verified.
- Rejected or revised assets invalidate only their own dependent audio and scene outputs.

## Image and motion

- Each shot has one primary action that fits its duration.
- Camera movement has a narrative reason; otherwise the camera is locked.
- Every close-up adds information rather than decoration.
- Medium shots, wide shots, and breathing shots preserve a lived-in space.
- No face drift, malformed bodies, invented objects, text, or watermarks remain.

## Reference-style fidelity — blocker

- The uploaded source, `style_lock_00`, four look-test images, motion test, and explicit user approval are present and connected before final generation.
- Opening, middle, strongest-motion, and ending samples preserve cyan-green/olive-teal shadows and white-gold/fire-orange highlights; they do not drift to beige, neutral, magenta-shadowed, uniformly warm, or generic commercial orange-teal.
- Motivated backlight, visible beams or flare, localized highlight clipping, soft bloom, and amber-red halation remain visible without turning the image into flat haze.
- Organic film grain, slight edge softness, and restrained red/cyan chromatic fringing survive across the full video; skin is not denoised or beauty-retouched.
- Every shot declares `anchor`, `tracking-memory`, or `transition-smear`. Blur is optical, directional, and aligned to movement; a readable subject or spatial anchor remains.
- Held portraits and the ending remain legible. No whole-frame Gaussian blur, duplicated anatomy, frame interpolation, optical-flow warping, or unrelated ghost trail remains.
- Brief tactile fragments alternate with longer spatial anchors; hard cuts follow musical beats or turns.
- Camera movement is limited to gentle handheld tracking, a very slow reveal, or a locked frame with internal motion.
- The ending holds on a static wide or medium composition before fading to black, without copying the reference's exact objects or scene.

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

Fix story causality first, reference binding and look-test approval second, character/location anchors third, and single-shot action fourth. Treat color, exposure, texture, and motion-blur drift as blockers rather than optional finishing. Retry one affected visual unit no more than twice. If it still fails, shorten the action, reduce visible people, choose `anchor` mode, or stop and report that the connected model cannot maintain the approved look. Never hide drift with a final filter.
