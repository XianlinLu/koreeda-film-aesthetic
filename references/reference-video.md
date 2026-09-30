# Kenopsia Reference Style Lock

## Exact source identity

The visual target is the user-supplied `Kenopsia` reference with this observed profile:

- Duration: `79.583333` seconds
- Frame: `1280 × 720`, `16:9`
- Frame rate: `24 fps`
- Video: H.264, progressive, BT.709, `yuv420p`
- Audio: AAC stereo
- SHA-256: `63c156780daa6cfe7fc10530f6bf9fbb72ad1befe5f1e269f08d1180d3805d72`

Use it as the mandatory moving-image look reference. Preserve its transferable color, exposure, texture, motion-blur behavior, camera energy, cut rhythm, and emotional cadence while creating new characters, places, actions, objects, music, and surreal images.

The video is not stored in this repository because Lumina rejects `.mp4` during Skill import. Keep the uploaded video as a runtime canvas asset.

## Runtime reference-binding gate

Do not begin final storyboard or video generation from text alone.

1. Add the supplied video to the canvas as `reference_00_kenopsia`.
2. Connect it to the available project-style, reference-video, or visual-reference input used by the storyboard and initial-video actions.
3. Create a `style_lock_00` text node containing the color, exposure, texture, and blur invariants below.
4. Generate a look test containing four new images: a dark interior, a blown-window interior, a backlit exterior, and a tactile close-up. Generate one shortest-supported lateral-motion test.
5. Compare the tests beside the uploaded video and obtain one explicit user approval. Record `style_lock_status: approved` before producing final shots.
6. Feed the approved look-test frames and uploaded video into later visual actions whenever the connector supports them. For extensions, the latest verified complete video remains the primary continuity input; also retain the source reference when the action accepts a separate style input.

If the connected action cannot consume either the uploaded video or approved frame references, stop before final generation and report that exact limitation. A prose prompt or end-stage filter alone cannot substantiate a claim of complete style matching.

## Color and exposure DNA — blocker

- **Split tone:** luminous amber, gold, and fire-orange highlights against cool cyan, blue-green, olive-teal, and occasional gray-blue shadows.
- **Hue targets:** warm highlight accents cluster around orange-gold; colored shadows cluster around cyan-green/teal. Use these as a relationship, not a flat two-color overlay.
- **Contrast:** deep, colored shadows with readable material detail; bright sources and sunlit skin may clip locally. Do not crush all blacks or lift them into gray haze.
- **Overexposure:** window, sun, flame, and flare regions may bloom one to two stops beyond white. Keep clipping localized in ordinary shots; allow broader white wash only at memory transitions or directly backlit exteriors.
- **Skin:** keep skin warm-neutral inside cool surroundings. It may become pale or partially blown where direct sun or flare crosses it, but it must not turn uniformly orange, waxy, or beauty-retouched.
- **Saturation:** rich but not neon. Preserve blue/cyan separation in water, sky, corridors, and shadow planes; preserve amber/orange separation in flame, sun, wood, and skin highlights.
- **Forbidden drift:** beige pastel, neutral Rec.709 documentary color, clean HDR, generic blockbuster orange-teal, magenta shadows, low-contrast gray, or uniformly warm vintage grading.

## Optical texture DNA — blocker

- Visible organic 35 mm grain with finer grain in bright regions and stronger grain in midtones and shadows.
- Soft amber-red halation around clipped windows, sun, flame, and specular edges.
- Gentle bloom and flare that come from a motivated light source; occasional blue/cyan streak flare is acceptable.
- Slight edge softness and restrained red/cyan chromatic fringing near high-contrast borders.
- Selective shallow focus in memory fragments; deeper focus in architectural anchors and the final still image.
- Never replace this with a uniform grain overlay, fake dust pack, heavy vignette, clarity sharpening, denoised skin, or clean digital-advertising polish.

## Dynamic-blur grammar — blocker

The reference does not blur every shot. Blur is selective and motivated.

- **Anchor mode:** locked or very slow camera, approximately a 180-degree-shutter appearance at 24 fps. Architecture and still faces remain readable; only moving paper, hair, curtain, water, or hands may blur.
- **Tracking-memory mode:** lateral follow or pan with an approximately 270–360-degree-shutter appearance. Keep one subject feature readable while the background and fast limbs smear along the true movement vector.
- **Transition-smear mode:** a brief overexposed or fast-motion smear, used only to enter or leave a memory cluster. Limit it to a short transition, not a whole scene.
- Motion blur must look exposure-integrated and directional, never like Gaussian blur applied to the entire frame.
- Preserve motion direction across the cut. A rightward run creates rightward or trailing lateral smear; vertical paper fall creates vertical trails.
- Favor normal/anchor motion for roughly two thirds of the film, tracking-memory blur for most remaining fragments, and transition smears only as rare punctuation.
- Reject frame interpolation, optical-flow warping, double faces, duplicate limbs, ghost trails unrelated to movement, smeared eyes in a held portrait, or artificial depth blur mistaken for motion blur.

The shutter-angle values above describe the appearance to request; they are not claimed as embedded camera metadata from the source file.

## Timecoded evidence map

Use these regions when comparing look tests and final output:

- `00:00–00:08`: fire-orange highlights against cyan-gray debris and sky; dense smoke; deep colored shadows.
- `00:15–00:22`: blue-green corridor and gym interiors, blown windows, visible beams, silhouettes, floating paper, and fast running.
- `00:28–00:40`: longer spatial anchors with dark teal/olive architecture and warm sun intrusion.
- `00:40–00:45`: high-key backlit exterior, cyan-white wash, pale skin, golden rim light, and blooming highlights.
- `00:44–00:54`: compressed tactile montage; directional hand and running blur, hard cuts, dappled facial light, and selective sharp anchors.
- `00:58–01:04`: cool interior shadows, strongly clipped window, cobalt flare streak, and restrained subject motion.
- `01:04–01:15`: long dark-teal interior anchor with amber fire reflection and slow internal environmental movement.

## Transferable structure

- `00:00–00:14`: establish absence through an unfamiliar condition, strong central image, or empty architecture.
- `00:15–00:40`: alternate 2–3 second memories with 5–10 second spatial anchors.
- `00:40–00:54`: compress emotion with a short cluster of 0.3–1.2 second tactile or motion fragments.
- `00:54–01:15`: decelerate into interior stillness, then hold a 6–10 second wide or medium spatial ending.
- After `01:15`: fade to black; use minimal end text only when requested.

## Translation into family drama

Keep the shape “empty present → memory fragments → altered present.” A simple act of return, clearing, waiting, searching, or leaving can provide the story spine. Each fragment must reveal a changed relationship to the place rather than decorate the montage.

- Choose one recurring object or sound rather than stacking symbols.
- Create one new paradoxical image tied directly to absence or memory.
- Include at least one ambience-only section.
- End with a locked wide or medium shot whose subtle environmental movement carries time.

## Prompt style kernel

Adapt and repeat this kernel in every final storyboard and video prompt, then append one compatible movement recipe from [Camera and Aesthetic Language](camera-aesthetic-library.md):

```text
Use the attached Kenopsia reference as the binding visual target. Dreamlike live-action memory film, 16:9, 24-fps appearance. Preserve its high-contrast split grade: localized white-gold or fire-orange highlight clipping, warm skin inside blue-green and olive-teal shadows, intense motivated backlight, visible beams, soft bloom, amber-red halation, organic 35 mm grain, slight edge softness, and restrained red/cyan chromatic fringing. Use [anchor / tracking-memory / transition-smear] blur mode: [shot-specific directional blur behavior and readable subject anchor]. Keep blur optical, exposure-integrated, and aligned to actual movement. Preserve tactile lived-in detail and melancholy without melodrama. No beige pastel grade, neutral documentary color, generic commercial orange-teal, clean HDR, uniform post blur, frame interpolation, logos, captions, watermarks, or copied signature imagery.
```

## Hard rejection rules

Reject and regenerate the affected visual unit if any of these occur:

- the palette becomes neutral, beige, magenta-shadowed, or uniformly warm;
- backlight has no bloom or halation, or the image looks digitally clean;
- the whole frame is uniformly blurred, or fast motion has no directional smear;
- a held face or final spatial anchor is unreadably smeared;
- extensions drift away from the approved cyan-green shadow and amber-gold highlight relationship;
- a final filter is used to disguise mismatched source lighting or inconsistent generated footage.

## Do not copy

Do not reuse the combinations of a burning piano, a butterfly on a fingertip, fire inside a flooded room, or the exact corridor-running sequence. Do not reuse the title, faces, wardrobe, shot order, credits, logos, or music. Match the color, optical behavior, rhythm, and sensory grammar—not protected expression.
