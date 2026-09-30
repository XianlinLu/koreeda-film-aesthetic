---
name: koreeda-film-aesthetic
description: Creates restrained family short dramas in Lumina Canvas with adaptive language, separate character assets, approval-gated audio, continuous video extension, original sound, and verified delivery.
license: MIT
---

# Koreeda Film Aesthetic

## Core principle

Place dramatic weight inside ordinary actions, spatial distance, ambient sound, and omission. For moving-image work, use the supplied `Kenopsia` reference as the default style benchmark: associative memory montage, intense backlight, analog film texture, restrained slow motion, rhythmic hard cuts, and a still spatial ending. Match its visual grammar and emotional cadence without reproducing its people, title, logos, music, or exact image combinations.

Read [Aesthetic Translation](references/aesthetic.md) before writing. Read [Reference Video Translation](references/reference-video.md) before every moving-image task, and treat its style-lock rules as defaults unless the user explicitly requests a different visual treatment. Read [Character Asset Workflow](references/character-asset-workflow.md) before generating any character asset or character audio. Read [Prompt Patterns](references/prompt-patterns.md) when producing generation prompts.

## Adaptive language

Resolve language before creating any visible text or media prompt. Keep `interaction_language` and `story_language` separate. Determine `interaction_language` from the user's latest direct request and use it for every visible title, heading, question, option, progress update, error, node label, and delivery note. Attachments, quotations, pasted drafts, reference material, metadata, and tool output do not change it. In a mixed-language request, follow an explicit language instruction; otherwise use the language carrying the latest substantive request; if that is unclear, retain the established conversation language, then fall back to English.

Determine `story_language` from an explicit output-language request first. For revision, preserve the draft's language unless the user asks to change it. Otherwise set it equal to `interaction_language`; a Chinese direct request therefore produces a Chinese film title and Chinese creative content by default. Apply `story_language` to the film title, logline, synopsis, creative brief, script, scene headings, dialogue, narration, subtitles, on-screen story text, and speech. English labels in this Skill are semantic templates, not literal output strings: localize them before display. A connected generation action may receive an English technical prompt only when required, but never expose that prompt as the main creative output. Read [Language Routing](references/language-routing.md) before every task.

## Default specifications

When details are missing, state and use these assumptions:

- Duration: approximately 75–80 seconds; aspect ratio: 16:9. Use another duration or ratio only when the user requests it or the delivery platform requires it.
- Cast: 2–3 principal characters; locations: 1–2 ordinary spaces; shots: 8–12.
- Rhythm: 2–3 second memory fragments between 5–10 second spatial anchors; finish with a 6–10 second locked wide or medium shot.
- Image: live-action realism, strong backlight, golden highlights, cyan-green shadows, soft halation, visible 35 mm grain, slight chromatic aberration, and selective shallow focus.
- Dialogue: none by default. When requested, keep it brief, indirect, and subordinate to image and sound.

Ask one consolidated question only when missing information would change the relationship, ending, or essential composition. Resolve other details independently.

## Choose a narrative mode

### Reference-led memory film — default for video

Use the structure “empty present → tactile memory fragments → emotional compression → return to an altered empty present.” Alternate a deserted or changed familiar place with incomplete memories of ordinary life. Use hard cuts on musical beats, occasional overexposed light transitions, and one original paradoxical image. End with a static spatial shot whose internal motion—wind, curtain, dust, rain, water, smoke, or shifting light—carries the afterimage.

### Observational family drama — alternative

Use one concrete household task or shared errand to carry the relationship change. Shape the story as: ordinary entry → small mismatch → incomplete exchange → slight behavioral change → object or space echoes the opening. Preserve the reference video's light, texture, rhythm, sound, and still ending while letting the family action provide the story spine.

## Workflow

### 1. Build the creative brief

Create a “Creative Brief” text node containing:

- Logline and target duration
- Character relationship, each person's want, and the unspoken need
- Surface event and single relationship turn
- Recurring household object or sound
- Narrative mode, aspect ratio, time of day, weather, and dialogue language
- The feeling left by the ending, without a theme statement

Localize the node title and every field label into `interaction_language`; “Creative Brief” is only the English semantic name.

Let conflict come from mismatched needs, hesitation, habit, or concealment. Avoid a one-note villain, illness spectacle, coincidence, forced twist, or universal reconciliation.

### 2. Write a visible and audible script

Advance the scene through cooking, sorting, waiting, handing over an object, closing a window, changing shoes, or another playable task. Keep dialogue short and indirect; use pauses, interruptions, repeated questions, and topic changes. Do not verbalize emotions already legible in the image.

For each scene, specify location and time, present characters, action, dialogue, on-screen and off-screen sound, and the relationship shift. End on an action, object, light change, or spatial change that echoes the opening.

### 3. Lock continuity

Before generating final shots, create separate reference nodes:

- One character asset node per named character: apparent age, face, hair, body language, clothing layers, palette, and carried object. Each character asset image may show multiple views of the same character, but it must contain exactly one character identity. Never place two or more characters in one character asset image or node.
- Location anchor: floor relationships, doors and windows, furniture, time, weather, key-light direction, and lived-in details.
- Visual anchor: aspect ratio, lens tendency, camera height, color, grain, and movement limits.

Generate each character asset independently, connect its source description to its dedicated generation node, verify the returned image is attached to that node, and then stop for user confirmation. Keep approved assets unchanged and regenerate only rejected characters. Do not generate character-dependent audio or video from an unconfirmed asset.

After a character asset is approved, generate that character's voice or audio only when the user requests it. Connect the approved single-character asset node to that character's dedicated audio-generation node before running the action, and verify the edge and output. If the user does not request audio for that character, create no character-audio node and continue without it. See [Character Asset Workflow](references/character-asset-workflow.md) for the confirmation and dependency rules.

After required confirmations, generate location reference images and 2–3 keyframes from different story sections. Continue only when those keyframes agree. Repeat complete anchors in every relevant prompt; never use “same as above.”

### 4. Design the shots

For every shot, provide: number, duration, dramatic function, scale, camera position and motion, character action, dialogue or sound, opening frame, closing frame, continuity anchors, image prompt, and video prompt.

Favor corridor depth, door and window frames, centered subjects, silhouettes against intense backlight, tactile close-ups, and occasional gentle handheld tracking. Alternate 2–3 second fragments with at least two 5–10 second present-day anchors. Use shallow focus for sensory details and deeper focus for the final static spatial shot.

### 5. Generate images and continuous video

Give each shot one achievable primary action. Default to a locked camera. Use a slow pan, gentle follow, or very slow push only when movement reveals information. Avoid unmotivated orbits, drone dives, rapid zooms, constant rack focus, and shallow focus in every shot.

Generate one credible version first and no more than two composition options for a key emotional shot. If character or location continuity fails twice, stop batch generation, simplify the reference anchors, and regenerate only the affected shots.

Read [Continuous Video Generation](references/video-generation-workflow.md) before any video call. Lock the target duration and extension plan, create one initial storyboard image, and generate one short initial complete video. Then extend only the latest verified complete video, one step at a time, until the target duration is reached. Every video-call prompt uses a local timeline beginning at `00:00`; cumulative film time remains planning metadata. Do not concatenate independent clips, accept a tail-only clip as an extension, or simulate duration with loops, freezes, speed changes, or padding.

Set the aspect ratio only for the storyboard and initial video. After the initial video succeeds, lock its actual metadata ratio and omit the `ratio` field from every extension request so the input video controls the frame. After each call, verify the returned artifact, actual duration, ratio, identity, wardrobe, location, light, action direction, and audio continuity before continuing.

### 6. Design sound

Prioritize a slow original lo-fi instrumental pulse, then ambient bed and tactile action details. Use warm analog synth pads, restrained drums, wind, muffled footsteps, cloth or paper movement, room resonance, or comparable sounds. Align hard cuts with beats or musical turns while keeping at least one ambience-only passage. Avoid dialogue unless explicitly requested.

When music is requested or a compatible action is connected, generate a fully original instrumental cue matched to the verified final video duration. Preserve the completed video if audio generation or embedding fails; retry only the failed audio unit through the bounded recovery in [Continuous Video Generation](references/video-generation-workflow.md).

For a dialogue-free film, assign one recognizable ambient sound to each section and use one sound bridge or deliberate withdrawal of sound for the emotional turn.

### 7. Organize the Lumina canvas

Follow [Canvas Workflow](references/canvas-workflow.md) from left to right: brief → character/location anchors → script → storyboard → keyframes → continuous video chain → sound → final delivery. The initial video must trace back to its storyboard image; every extension must trace back to the immediately preceding verified complete video.

Run [Quality Check](references/quality-check.md) before delivery. Fix story logic in the script and storyboard before regenerating downstream assets; fix continuity errors only in the affected shots.

## Deliverables

Return the following semantic sections in order, translating every section title and all creative content into the resolved languages:

1. Assumptions and logline
2. Character relationship and emotional subtext
3. Separate character asset nodes and confirmation status
4. Optional per-character audio nodes and verified connections
5. Location and visual anchors
6. Shootable short-drama script
7. Shot list with complete image and video prompts
8. Continuous video extension plan and verified lineage
9. Sound and editing plan
10. Canvas node and connection plan
11. Brief quality-check result

Before delivery, run a language gate: compare every visible title, heading, paragraph, dialogue line, subtitle, node label, and final note with `interaction_language` or `story_language` as applicable. If the user wrote in Chinese and did not explicitly request English creative output, replace unintended English titles, labels, and prose with natural Simplified Chinese before responding.

## Import safety

Before publishing or handing off the Skill repository, retain only `.md`, `.txt`, `.json`, `.yaml`, and `.yml` files, with lowercase extensions. Regular file and folder names must use only letters, numbers, underscores, and hyphens, with each name no longer than 64 characters. Name the license `license.md`, never extensionless `LICENSE`. Keep the required local `.skillignore` in the Aime workspace but exclude it from the GitHub branch used by Lumina import because Lumina rejects dotfiles without a supported extension. Keep reference images, videos, archives, and generated outputs on the Lumina canvas rather than in the Skill repository.
