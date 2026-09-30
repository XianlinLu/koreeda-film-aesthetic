# Lumina Canvas Workflow

## Nine columns from left to right

1. Creative brief: request, assumptions, mode, duration, and aspect ratio.
2. Style lock: uploaded `reference_00_kenopsia`, `style_lock_00`, four look-test images, one motion test, and approval status.
3. Character/location anchors: one single-character asset node per identity, confirmation status, location references, and continuity notes.
4. Script: scene actions, dialogue, sound, and relationship changes.
5. Storyboard: one entry per shot with start, action, end, duration, C1–C10 camera recipe, lens/composition, focus gesture, blur mode, readable anchor, and blur direction.
6. Keyframes: opening, turning point, and ending visual references.
7. Continuous video chain: initial complete video followed by sequential extensions of the latest verified complete video.
8. Sound: dialogue, ambient bed, action detail, and music layers.
9. Final delivery: the last verified complete video, synchronized original audio, and validation notes.

## Node naming

Use `type_number_short-description`, such as `beat_04_empty-bowl`, `video_00_initial`, and `video_02_extension`. Keep a two-digit number and use only letters, numbers, underscores, and hyphens. Avoid spaces and special characters.

## Connections

- Connect each character description to one dedicated character-asset generation node. Verify the output and edge, then stop for user approval.
- Connect `reference_00_kenopsia` to the style-binding route and every visual action that accepts a separate style reference. Connect approved look-test frames to storyboard and initial-video actions. Do not report complete fidelity when no such reference route exists.
- For each requested voice, connect only the corresponding approved character asset to its dedicated audio-generation node. Skip the audio node when that character does not need audio.
- Connect approved single-character assets separately to every relevant keyframe and scene-generation node. Multi-character scenes may receive multiple separate asset inputs, but character asset nodes never contain multiple identities.
- Connect the initial video to its storyboard image. Connect each extension only to the immediately preceding complete-video node and its next narrative beat.
- Connect each sound node to a defined shot or section; avoid undated “whole-film mood” nodes.
- Connect only the latest verified complete video to final delivery. Place failed or alternate branches to the side and label them `failed` or `alt`.

## Recovery paths

- Character drift: preserve the latest verified complete video and retry only the failed initial or extension step with stronger identity anchors.
- Character asset contains multiple people: reject it, keep other approved assets, and regenerate only that character's dedicated node with an explicit one-character-only constraint.
- Missing or wrong audio edge: do not run audio generation; reconnect the approved character asset to its matching audio node and verify the edge first.
- Spatial jump: recheck door/window direction, key light, and furniture in the location anchor.
- Incomplete action: split multiple actions into two shots or extend the shot to 10 seconds.
- Excessive speed: lengthen present-day anchor shots instead of duplicating frames or using slow motion.
- Overstated emotion: remove music first, then explanatory dialogue, then unnecessary close-ups.
- Ratio error during extension: remove the `ratio` field and retry only that extension; do not crop or restart the chain.
- Palette or blur drift: preserve the latest verified complete video, reattach the approved look tests and reference video where supported, restate the declared blur mode and direction, and retry only the failed visual unit. Never hide drift with a global finishing filter.
