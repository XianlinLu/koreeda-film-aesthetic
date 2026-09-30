# Camera and Aesthetic Language Library

## Source coverage

This library distills all 42 video-generation prompts visible in the read-only creation workflow for [Kenopsia on LibTV](https://www.liblib.tv/detail/9c44abc2c3474ffb9acf9b50b14204df). The source prompts span 3–10 second generations and repeatedly combine handheld DV behavior, fast focal changes, long-lens shake, parallax tracking, step-printed trails, strong backlight, analog texture, wind-driven internal motion, experimental montage, and liminal spatial anchors.

Do not copy a source prompt, character, action, signature object, or exact scene. Transfer the prompt architecture, camera logic, optical behavior, and aesthetic relationships to new material.

## Precedence and selection

Apply constraints in this order:

1. The user's current shot requirement.
2. The approved `Kenopsia` color and optical style lock.
3. One primary camera recipe from this document.
4. One optional focus or exposure gesture.
5. Shot-specific negative constraints.

Do not combine every attractive phrase. Each shot gets one dominant camera intention. A secondary gesture is allowed only when it supports the same subject and can finish within the duration.

## Transferable aesthetic layers

### Rough 1990s film and DV

- Handheld observational immediacy, imperfect framing, visible operator presence, no gimbal polish.
- Fine-to-heavy organic grain selected by shot intensity; edge softness, occasional defocus, autofocus breathing, and highlight bloom.
- Strong contrast with bright practical or sun sources and dense colored shadows.
- The result should feel recorded in the moment rather than art-directed into sterile perfection.

### Experimental memory cinema

- Stream-of-consciousness association instead of literal exposition.
- A tactile detail, face, hand, hair, paper, curtain, water, reflection, or moving light can become a memory trigger.
- Abrupt focal or scale change is permitted when emotion breaks through an otherwise stable spatial anchor.
- Step-printed temporal trails and incomplete focus may express memory, but never obscure every frame.

### Documentary presence

- Natural body physics, asynchronous group movement, unplanned micro-reactions, and wind interacting with hair and clothing.
- The camera may lag, overshoot, correct, or breathe focus slightly. It must still preserve a readable subject anchor.
- Ban perfectly synchronized crowd motion, rigid faces, frozen fabric, and frictionless camera paths.

### Liminal and dreamcore space

- Centered one-point perspective, empty corridors, deep rooms, windows, door glass, reflective floors, fog, rain, and slow internal environmental motion.
- Longer duration, quieter framing, and restrained camera travel contrast with the violent memory fragments.
- The uncanny feeling comes from an ordinary space behaving slightly wrong, not from adding monsters or spectacle.

### Youth-memory glow

- Strong backlight, soft flare, wind, dappled sun, high-key exterior wash, grain, loose smiles, and fleeting physical gestures.
- Keep it emotionally immediate rather than glossy, cute, or commercial.

### Ruin and surreal absence

- Weathered material, abandoned furniture, smoke, firelight, fog, water, or vegetation can make time visible.
- Use one contradiction at a time and preserve realistic material physics.
- Avoid stacking unrelated surreal symbols.

## Camera recipe library

### C1 — Visceral handheld DV burst

Use for sudden laughter, running, panic, release, or memory eruption.

- Extreme handheld shake with spontaneous, imperfect dynamic framing.
- Begin in a wide or medium spatial view, then react to the subject rather than anticipating perfectly.
- Preserve operator inertia, small overshoot, and correction.
- Pair with a wide-to-close progression only if the subject remains trackable.
- Ban stabilized glide, static formal framing, low-energy action, and synchronized movement.

### C2 — Snap zoom into a tactile or emotional anchor

Use for an eye opening, hand pressing, face turning, or a small object becoming emotionally charged.

- Start with enough context to establish location.
- Execute a fast optical-looking snap zoom into a face, eye, hand, or object.
- Allow strong handheld vibration and a short autofocus correction after the zoom.
- End with the selected anchor readable; avoid digital stretch, face deformation, or indefinite focus hunting.

### C3 — Static handheld with telephoto jitter

Use for watching, waiting, a face by a window, or a charged object.

- Camera position stays fixed; the frame carries natural long-lens micro-shake.
- No pan, track, or follow unless explicitly requested.
- The subject or environment supplies internal motion: wind, hair, cloth, paper, flame, water, or shifting light.
- Ban tripod sterility and large accidental reframing.

### C4 — Tracking parallax with counter-pan

Use for bicycles, trains, walking across traffic, or lateral movement through a city.

- Truck the camera opposite or alongside the subject while panning back to keep the subject centered.
- Produce strong foreground/background parallax and directional streaking.
- Keep the subject's face or torso readable while architecture, lights, vehicles, and pedestrians sweep past.
- Explicitly state vehicle and subject directions; reject a static background or a drifting subject center.

### C5 — Lateral follow with long-shutter or step-printed trails

Use for running memory fragments and emotional acceleration.

- Handheld side follow with a simulated long-shutter appearance.
- Choose either continuous directional smear or discrete step-printed trails; never request both in the same shot.
- Retain one readable anchor such as a flower bouquet, hand, profile edge, or clothing silhouette.
- For step printing, request separated temporal impressions rather than smooth Gaussian blur.
- Ban stabilized footage, unrelated ghosting, doubled faces, and trail direction that contradicts motion.

### C6 — Vertical descent with compensating tilt

Use for hands playing, writing, sorting, or another precise manual action.

- Move the handheld camera slowly downward while tilting upward enough to keep the hand/object centered.
- Let a high angle gradually approach a more horizontal view.
- Prioritize correct hand physics, contact, and continuous action over decorative camera motion.
- Exclude face, head, or torso when the composition is intentionally hand-only.

### C7 — Slow pull-back or push-in with handheld presence

Use for revealing absence, deepening isolation, or approaching a person absorbed in an action.

- Travel slowly and evenly, but retain mild operator shake unless the shot is declared a continuous spatial anchor.
- Keep the central subject stable in the composition while the surrounding space expands or compresses.
- Ban mechanical gimbal smoothness for memory fragments.

### C8 — Rack focus across depth

Use when a foreground detail changes the meaning of a background person or space.

- Establish background action first.
- Shift focus once, deliberately, from background to foreground or the reverse.
- Keep both planes spatially coherent and stop hunting after the selected subject becomes sharp.
- Ban simultaneous zoom, orbit, and rack focus unless the duration clearly supports them.

### C9 — Slow orbit around a still subject

Use sparingly for a contained turning point.

- Handheld arc to the right or left around a centered subject.
- Preserve light direction, spatial geometry, and silhouette.
- Let fabric, curtains, hair, or dust provide counter-motion.
- Avoid a full commercial product orbit or impossible background reconstruction.

### C10 — Continuous architectural retreat

Use for the final liminal passage or a transition from room to corridor.

- One uninterrupted, slow, constant pull-back through a doorway or glass boundary.
- Dynamic center framing, eye-level view, readable reflections, and uninterrupted environment continuity.
- This is the principal exception to rough handheld movement: keep it controlled and continuous.
- Ban cuts, jumps, resets, dry/wet continuity changes, or geometry morphing.

## Lens and composition grammar

- **35 mm:** immersive wide or overhead group energy; deep architecture; environmental movement.
- **50 mm:** eye-level wide or medium observation; centered composition; deep one-point perspective.
- **85 mm:** side-profile medium or close portrait; rule-of-thirds separation; compressed emotional distance.
- **105 mm macro:** eye, hand, fingertip, pen, cloth, or other tactile insert; shallow focus and controlled subject motion.
- **200 mm telephoto:** pronounced spatial compression, long-lens jitter, distant tracking, and flattened layers.

Choose focal language according to composition; do not enumerate multiple lenses in one prompt. Use centered symmetry and deep perspective for empty spaces, imperfect off-center framing for rough DV memories, and strict crop boundaries when excluding faces or heads.

## Focus, exposure, and atmospheric motion

- Use autofocus breathing as a brief documentary imperfection, not permanent pulsing.
- Use shallow focus for sensory inserts and compressed memory; use deeper focus for spatial anchors and continuous architectural travel.
- Strong backlight may reduce a person to a readable silhouette. Do not request detailed facial illumination and silhouette-only exposure simultaneously.
- Keep flare and shadow patterns temporally stable enough to avoid flicker while allowing motivated movement from leaves, curtains, vehicles, or water.
- Wind is a continuity system: hair, fabric, paper, smoke, flame, vegetation, and curtains must respond in compatible directions and intensities.
- Internal environmental motion prevents static frames from feeling dead; it must not compete with the primary action.

## Motion-blur and temporal grammar

- A source prompt's `motion blur-free` clause usually protects the selected subject, not the entire image. Scope it as `subject remains readable; background may smear directionally`.
- Use full-frame rough blur only in a declared memory-burst shot.
- Use simulated 1/4-second-shutter language only for deliberately extreme temporal abstraction. It creates long exposure trails and should not be the default 24-fps motion treatment.
- Use step-printed trails for separated temporal impressions; use continuous smear for vehicle or lateral background motion.
- Preserve normal 24-fps playback unless the shot explicitly requests step printing. Do not accidentally combine normal playback, slow motion, frame dropping, and long-shutter trails.
- Motion vectors, focus, wind, and camera direction must agree.

Do not place a living filmmaker's name in downstream prompts. Translate any named reference into functional language such as `step-printed temporal cadence, discrete directional trails, handheld snap zoom, and high-contrast backlight bloom`.

## Shot-specific negative constraints

Always include only relevant negatives.

### Temporal integrity

`no flicker, no unintended frame dropping, no sudden light shift, no morphing, no warping, no clipping/intersection artifacts`

### Handheld intent

For C1, C2, C3, C5, C6, C7, and C9: `no gimbal glide, no perfectly smooth movement, no static operator feel`.

For C10: invert that rule and require continuous controlled travel with `no cuts, jumps, shake spikes, or discontinuous speed`.

### Subject fidelity

Protect only what is visible: face, eyes, hands, fingers, limbs, clothing, instrument, bicycle, or another defined object. Do not add irrelevant anatomy negatives.

### Environmental physics

Prevent frozen hair, cloth, curtains, flame, smoke, water, vegetation, or paper only when those elements are present. Keep wind direction and light direction stable.

### Blur intent

- Anchor shot: `no whole-frame blur; architecture and held face remain readable`.
- Tracking shot: `subject readable; background must not freeze; smear follows movement vector`.
- Step-print shot: `discrete temporal trails required; no smooth continuous blur`.
- Long architectural shot: `no temporal trails, interpolation warping, or geometry smear`.

### Audio separation

When sound is generated later as a separate layer, end the video prompt with `no background music`. Do not prohibit environmental sound when the generation action needs diegetic ambience.

## Prompt assembly order

Write final video prompts in this order:

1. `Style lock:` approved color, exposure, grain, halation, and frame-rate appearance.
2. `Camera recipe:` one recipe ID and a plain-language description.
3. `Lens and composition:` one focal tendency, scale, angle, and subject placement.
4. `Primary action:` one continuous action with a clear opening and ending state.
5. `Camera/subject relationship:` tracking target, readable anchor, motion direction, and parallax.
6. `Focus and temporal behavior:` sharp plane, optional rack focus, blur type, shutter appearance, or step printing.
7. `Light and atmosphere:` motivated backlight, flare, wind, fog, rain, paper, curtains, or reflections.
8. `Negative constraints:` temporal integrity plus only the shot-specific failure modes.

## Selection guide

- Quiet present or empty room → C3, C7, or C10.
- Sudden emotional memory → C1 plus optional C2.
- Running or lateral escape → C4 or C5.
- Hand/object action → C6, optionally C8.
- Face at window or watched subject → C3.
- Meaning shifts from person to object → C8.
- Climactic spatial withdrawal → C10.

If two candidate recipes are equally plausible, choose the simpler one and preserve the stronger recipe for a later contrast beat.

## Originality boundary

Do not reproduce the source workflow's burning piano, butterfly landing, corridor run, flooded music room, bouquet run, bicycle couple, or other recognizable combinations. Do not copy its people, wardrobe, shot order, or verbatim prompt wording. Reuse the camera mechanism and aesthetic relationships with new story content.
