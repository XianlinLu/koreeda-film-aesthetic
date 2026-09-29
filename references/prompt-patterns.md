# Prompt Patterns

Fill every bracket with shot-specific information and repeat complete continuity anchors in every prompt. Apply the style kernel in [Kenopsia Reference Style Lock](reference-video.md) to every storyboard and moving-image prompt. Do not include a living filmmaker's name, a film title, or a remake request in downstream prompts.

## Character reference

```text
[Aspect ratio], live-action character reference. [Apparent age, facial traits, hair, build], [clothing layers, colors, materials, shoes, carried object]. Natural stance and restrained expression; recognizable front and three-quarter views; soft natural light, neutral background, natural skin, moderate depth of field, detailed without oversharpening. No text, watermark, brand mark, or exaggerated makeup.
```

## Location reference

```text
[Aspect ratio], live-action cinematic location. [Place, floor relationships, doors and windows, furniture, lived-in traces], [time, weather, key-light direction], with [two or three muted dominant colors]. No people; moderate depth of field; exterior detail and material texture retained. No text, watermark, or brand mark.
```

## Storyboard image

```text
[Aspect ratio], dreamlike live-action memory-film frame. [Complete character anchor] is in [complete location anchor], performing [one visible action]. [Distance, eyelines, and occlusion]. [Centered / deep corridor / doorway frame / tactile insert], [camera height and angle], [locked composition / gentle handheld tracking]. Intense [backlight source] with visible beams and controlled flare, warm golden highlights against cool cyan-green shadows, soft halation, organic 35 mm grain, slight chromatic aberration, [shallow or deep] focus, lived-in texture. Express emotion through [hand action, pause, object, or environmental motion]. No clean commercial gloss, text, watermark, logo, or copied signature imagery.
```

## Initial complete video

```text
Duration [supported initial duration]. Preserve the storyboard image's identity, wardrobe, location layout, intense backlight, golden-to-cyan palette, halation, grain, and focus behavior. 00:00-[time point]: [opening action]. [time point]-[end]: [one continuous development], settling into [continuation-ready closing state]. Use restrained slow-motion feeling and [locked camera with internal motion / gentle handheld tracking / very slow push]. Keep plausible physics. Do not add people or objects, alter faces, clothing, weather, spatial layout, or frame shape, deform bodies, clean away the film texture, or add text and watermarks.
```

## True extension

Submit the latest verified complete video as the input and omit the `ratio` field.

```text
Extend by [supported increment]. Preserve the input video's identity, wardrobe, scene geometry, intense backlight, golden-to-cyan palette, halation, organic grain, focus behavior, motion direction, props, and sound logic. 00:00-[time point]: continue naturally from the existing final frame with [next action]. [time point]-[end]: [one memory or relationship change], settling into [next continuation-ready state]. Maintain its restrained slow-motion feeling and camera behavior. Return the complete extended video, not an isolated tail clip. Do not reset the scene, change the frame shape, clean away the analog texture, add people or objects, deform bodies, or add text and watermarks.
```

Every call-local timeline starts at `00:00`. Keep cumulative film positions outside generation prompts.

## Memory fragment

```text
Duration [1.5–3] seconds. A subjective memory triggered by [present action, object, or sound]. Preserve the defining traits of [character or location anchor] and show only [one action or sensory detail]. Link the composition to the present through [movement direction, color, or sound]. Allow slight motion blur or exposure shift. Do not copy an exact image from the reference film, add a second surreal element, or add text and watermarks.
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
