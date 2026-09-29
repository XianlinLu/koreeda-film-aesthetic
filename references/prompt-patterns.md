# Prompt Patterns

Fill every bracket with shot-specific information and repeat complete continuity anchors in every prompt. Do not include a living filmmaker's name, a film title, or a remake request in downstream prompts.

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
[Aspect ratio], live-action cinematic frame. [Complete character anchor] is in [complete location anchor], performing [one visible action]. [Distance, eyelines, and occlusion between characters]. [Shot scale], [camera height and angle], [locked composition or frame-within-frame]. [Time, weather, key-light direction], natural skin, muted neutrals, moderate depth of field, lived-in detail, subtle film grain. Express emotion through [hand action, pause, or object]. No text, watermark, or brand mark.
```

## Initial complete video

```text
Duration [supported initial duration]. Preserve the storyboard image's identity, wardrobe, location layout, light, and color. 00:00-[time point]: [opening action]. [time point]-[end]: [one continuous development], settling into [continuation-ready closing state]. Camera is [locked / slow pan / gentle follow / very slow push] with stable, motivated movement. Keep natural speed and plausible physics. Do not add people or objects, alter faces, clothing, weather, or spatial layout, jump the camera, deform bodies, or add text and watermarks.
```

## True extension

Submit the latest verified complete video as the input and omit the `ratio` field.

```text
Extend by [supported increment]. Preserve the input video's identity, wardrobe, scene geometry, lighting, color, motion direction, props, and audio logic. 00:00-[time point]: continue naturally from the existing final frame with [next action]. [time point]-[end]: [one relationship or story change], settling into [next continuation-ready state]. Keep camera behavior and physical timing plausible. Return the complete extended video, not an isolated tail clip. Do not reset the scene, change the frame shape, add people or objects, deform bodies, or add text and watermarks.
```

Every call-local timeline starts at `00:00`. Keep cumulative film positions outside generation prompts.

## Memory fragment

```text
Duration [1.5–3] seconds. A subjective memory triggered by [present action, object, or sound]. Preserve the defining traits of [character or location anchor] and show only [one action or sensory detail]. Link the composition to the present through [movement direction, color, or sound]. Allow slight motion blur or exposure shift. Do not copy an exact image from the reference film, add a second surreal element, or add text and watermarks.
```

## Sound

```text
Authentic [interior/exterior] ambience. Near field: [action detail]. Mid field: [continuous room or street tone]. Far field: [sound extending the space]. Dialogue is natural, stable, and includes brief pauses. No exaggerated reverb or trailer impacts. If music is used, choose sparse acoustic instruments, keep it below dialogue, enter at [point], and leave at [point].
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
