# Prompt Patterns

Fill every bracket with shot-specific information and repeat complete continuity anchors in every prompt. Apply the style kernel in [Kenopsia Reference Style Lock](reference-video.md) to every storyboard and moving-image prompt. Keep `reference_00_kenopsia`, `style_lock_00`, and the approved look-test frames connected wherever the action supports visual references. Do not include a living filmmaker's name, a film title, or a remake request in downstream prompts.

## Character reference

```text
[Aspect ratio], live-action character reference. [Apparent age, facial traits, hair, build], [clothing layers, colors, materials, shoes, carried object]. Natural stance and restrained expression; recognizable front and three-quarter views; soft natural light, neutral background, natural skin, moderate depth of field, detailed without oversharpening. No text, watermark, brand mark, or exaggerated makeup.
```

## Location reference

```text
[Aspect ratio], live-action cinematic location. [Place, floor relationships, doors and windows, furniture, lived-in traces], [time, weather, key-light direction], with [two or three muted dominant colors]. No people; moderate depth of field; exterior detail and material texture retained. No text, watermark, or brand mark.
```

## Mandatory look test

Generate four original frames—dark interior, blown-window interior, backlit exterior, and tactile close-up—plus one shortest-supported lateral-motion clip.

```text
Use the attached Kenopsia reference as the binding visual target, not as story content. Preserve its localized white-gold or fire-orange highlight clipping, warm skin within cyan-green and olive-teal shadows, intense motivated backlight, soft bloom, amber-red halation, organic 35 mm grain, slight edge softness, and restrained red/cyan chromatic fringing. For the motion test, track [new subject and action] laterally at a 24-fps, long-shutter memory-film appearance: keep [readable face/hand/object anchor] legible while the background and fast limbs smear along [direction]. No copied people, objects, places, titles, logos, or exact staging. No beige grade, neutral documentary color, clean HDR, uniform post blur, or frame interpolation.
```

Record the test as approved only after the user confirms color, exposure, texture, and blur behavior together.

## Storyboard image

```text
[Aspect ratio], dreamlike live-action memory-film frame using the approved Kenopsia look test as the binding visual target. [Complete character anchor] is in [complete location anchor], performing [one visible action]. [Distance, eyelines, and occlusion]. [Centered / deep corridor / doorway frame / tactile insert], [camera height and angle], [locked composition / gentle tracking]. Localized white-gold or fire-orange clipping from [motivated light], warm skin inside cyan-green and olive-teal shadows, visible beams, soft bloom, amber-red halation, organic 35 mm grain, slight edge softness, restrained red/cyan fringing, [shallow or deep] focus, lived-in texture. Express emotion through [hand action, pause, object, or environmental motion]. No beige or neutral grade, clean HDR, generic commercial orange-teal, text, watermark, logo, or copied signature imagery.
```

## Initial complete video

```text
Duration [supported initial duration], 24-fps appearance. Preserve the approved reference look, storyboard identity, wardrobe, location layout, split-tone palette, localized highlight clipping, backlight, bloom, halation, grain, chromatic fringing, and focus behavior. Blur mode: [anchor / tracking-memory / transition-smear]. Readable anchor: [face/hand/object/architecture]. Blur direction: [direction aligned to action]. 00:00-[time point]: [opening action]. [time point]-[end]: [one continuous development], settling into [continuation-ready closing state]. Keep blur optical and exposure-integrated. Do not add people or objects, alter faces, clothing, weather, spatial layout, frame shape, shadow hue, or light direction, deform bodies, clean away film texture, apply uniform post blur, interpolate frames, or add text and watermarks.
```

## True extension

Submit the latest verified complete video as the input and omit the `ratio` field.

```text
Extend by [supported increment]. Preserve the input video's identity, wardrobe, scene geometry, approved cyan-green/olive-teal shadows, white-gold/fire-orange highlights, localized clipping, motivated backlight, bloom, halation, organic grain, chromatic fringing, focus behavior, motion direction, props, and sound logic. Blur mode: [anchor / tracking-memory / transition-smear]. Readable anchor: [anchor]. Blur direction: [direction]. 00:00-[time point]: continue naturally from the existing final frame with [next action]. [time point]-[end]: [one memory or relationship change], settling into [next continuation-ready state]. Return the complete extended video, not an isolated tail clip. Do not reset the scene, neutralize or warm the grade, change frame shape or light direction, clean away the analog texture, apply uniform blur, interpolate frames, add people or objects, deform bodies, or add text and watermarks.
```

Every call-local timeline starts at `00:00`. Keep cumulative film positions outside generation prompts.

## Memory fragment

```text
Duration [1.5–3] seconds. A subjective memory triggered by [present action, object, or sound]. Preserve the defining traits of [character or location anchor] and show only [one action or sensory detail]. Blur mode: tracking-memory, 24-fps long-shutter appearance. Track [subject] along [direction], keep [readable feature] partially legible, and let [background/limb/material] smear along the true movement vector. Link the fragment to the present through [movement direction, color, or sound]. Do not blur the entire frame, create duplicate limbs or faces, copy an exact image from the reference, add a second surreal element, or add text and watermarks.
```

## Sound

```text
Original slow lo-fi instrumental pulse with restrained drums and nostalgic analog synth pad. Near field: [tactile action detail]. Mid field: [continuous room tone, wind, paper, cloth, water, or footsteps]. Far field: [sound extending the empty space]. Include [ambience-only interval]. Align selected hard cuts with beats or musical turns. No dialogue unless requested; no recognizable melody, lyrics, exaggerated trailer impact, or copied reference audio.
```

## Shot entry example

```text
Shot 04 | 10 s | relationship test | kitchen, medium shot, locked camera
Action: The mother slides an extra bowl of rice toward an empty seat, pauses, then draws it back.
Sound: Rice cooker's warming hum; a door closes in the corridor; no music.
Opening: Two people sit opposite each other; the empty seat is frame right.
Closing: The mother lowers her eyes to eat; the child looks at the empty bowl.
Continuity: Wardrobe, table direction, right-side window light, and the three differently colored bowls match the references.
```

The example demonstrates information density only. Do not reuse its plot or composition.
