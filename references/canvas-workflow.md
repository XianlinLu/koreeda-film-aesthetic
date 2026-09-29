# Lumina Canvas Workflow

## Eight columns from left to right

1. Creative brief: request, assumptions, mode, duration, and aspect ratio.
2. Character/location anchors: reference images and continuity notes.
3. Script: scene actions, dialogue, sound, and relationship changes.
4. Storyboard: one entry per shot with start, action, end, and duration.
5. Keyframes: opening, turning point, and ending visual references.
6. Shot videos: numbered consistently and connected to their storyboard and reference images.
7. Sound: dialogue, ambient bed, action detail, and music layers.
8. Final sequence: accepted shots only, arranged in playback order.

## Node naming

Use `type_number_short-description`, such as `shot_04_empty-bowl` and `video_04_empty-bowl`. Keep a two-digit shot number and use only letters, numbers, underscores, and hyphens. Avoid spaces and special characters.

## Connections

- Connect character and location anchors to every relevant keyframe and video node.
- Connect each video node to at least one storyboard entry and one visual reference.
- Connect each sound node to a defined shot or section; avoid undated “whole-film mood” nodes.
- Connect only accepted versions to the final sequence. Place alternatives to the side and label them `alt`.

## Recovery paths

- Character drift: disconnect the failed video and return only to the character anchor and that shot's keyframe.
- Spatial jump: recheck door/window direction, key light, and furniture in the location anchor.
- Incomplete action: split multiple actions into two shots or extend the shot to 10 seconds.
- Excessive speed: lengthen present-day anchor shots instead of duplicating frames or using slow motion.
- Overstated emotion: remove music first, then explanatory dialogue, then unnecessary close-ups.
