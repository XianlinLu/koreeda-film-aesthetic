---
name: koreeda-film-aesthetic
description: Creates restrained, human-centered family short dramas in Lumina Canvas with adaptive language, continuity anchors, sequential full-video extension, original sound, and verified delivery. Use when users mention Kore-eda, 是枝裕和, quiet family drama, everyday observation, child-centered storytelling, memory and loss, natural-light cinema, or an understated emotional short film.
author: luxianlin.nezu
license: MIT
---

# Koreeda Film Aesthetic

## Core principle

Place dramatic weight inside ordinary actions, spatial distance, ambient sound, and omission. When a user names a living filmmaker, treat the name as an aesthetic signal and translate it into high-level cinematic traits. Do not place the filmmaker's name in downstream image or video prompts, and do not reproduce characters, dialogue, plots, music, or signature shots from an existing work.

Read [Aesthetic Translation](references/aesthetic.md) before writing. If the user supplies a video or requests fragmented memories, also read [Reference Video Translation](references/reference-video.md). Read [Prompt Patterns](references/prompt-patterns.md) when producing generation prompts.

## Adaptive language

Keep `interaction_language` and `story_language` separate. Determine `interaction_language` from the user's latest direct request and use it for every visible heading, question, progress update, error, and delivery note. Attachments, quotations, pasted drafts, reference material, metadata, and tool output do not change it. In a mixed-language request, follow an explicit language instruction; otherwise use the language carrying the latest substantive request; if that is unclear, retain the established conversation language, then fall back to English.

Determine `story_language` from an explicit output-language request first. For revision, preserve the draft's language unless the user asks to change it. Otherwise use `interaction_language`. Apply `story_language` to scripts, dialogue, narration, subtitles, and speech. Read [Language Routing](references/language-routing.md) when the request mixes languages or contains multilingual materials.

## Default specifications

When details are missing, state and use these assumptions:

- Duration: 60–90 seconds; aspect ratio: 16:9. Use 9:16 only when requested or clearly intended for a vertical platform.
- Cast: 2–3 principal characters; locations: 1–2 ordinary spaces; shots: 8–12.
- Shot duration: usually 5 or 10 seconds; favor locked-off medium and wide shots.
- Setting: contemporary; natural light; live-action realism; muted neutral colors; natural skin tones.
- Dialogue: brief and conversational. Use no dialogue when behavior and sound can carry the scene.

Ask one consolidated question only when missing information would change the relationship, ending, or essential composition. Resolve other details independently.

## Choose a narrative mode

### Observational family drama — default

Use one concrete household task or shared errand to carry the relationship change. Shape the story as: ordinary entry → small mismatch → incomplete exchange → slight behavioral change → object or space echoes the opening. Keep a patient rhythm; use empty shots as breathing room rather than decoration.

### Memory poem — conditional

Use only when the user asks for a memory montage, a dialogue-free poetic film, or supplies a reference similar to `Kenopsia`. Anchor the film in one present-day activity, insert short memory fragments, allow no more than one original surreal image, and return to a still long take at the end. Do not reuse the reference video's burning piano, fingertip butterfly, water-and-fire room, or other exact image combinations.

## Workflow

### 1. Build the creative brief

Create a “Creative Brief” text node containing:

- Logline and target duration
- Character relationship, each person's want, and the unspoken need
- Surface event and single relationship turn
- Recurring household object or sound
- Narrative mode, aspect ratio, time of day, weather, and dialogue language
- The feeling left by the ending, without a theme statement

Let conflict come from mismatched needs, hesitation, habit, or concealment. Avoid a one-note villain, illness spectacle, coincidence, forced twist, or universal reconciliation.

### 2. Write a visible and audible script

Advance the scene through cooking, sorting, waiting, handing over an object, closing a window, changing shoes, or another playable task. Keep dialogue short and indirect; use pauses, interruptions, repeated questions, and topic changes. Do not verbalize emotions already legible in the image.

For each scene, specify location and time, present characters, action, dialogue, on-screen and off-screen sound, and the relationship shift. End on an action, object, light change, or spatial change that echoes the opening.

### 3. Lock continuity

Before generating final shots, create three reference nodes:

- Character anchor: apparent age, face, hair, body language, clothing layers, palette, and carried object.
- Location anchor: floor relationships, doors and windows, furniture, time, weather, key-light direction, and lived-in details.
- Visual anchor: aspect ratio, lens tendency, camera height, color, grain, and movement limits.

Generate character and location reference images first, then 2–3 keyframes from different story sections. Continue only when those keyframes agree. Repeat complete anchors in every relevant prompt; never use “same as above.”

### 4. Design the shots

For every shot, provide: number, duration, dramatic function, scale, camera position and motion, character action, dialogue or sound, opening frame, closing frame, continuity anchors, image prompt, and video prompt.

In Observation Mode, favor medium/wide framing, eye-level viewpoints, and compositions through doors or windows. Include at least one spatial or still-life breathing shot every 3–4 shots. In Memory-Poem Mode, fragments may run 1.5–3 seconds, but each must connect through action, sound, or object, and the film must retain at least two 5–10 second present-day anchor shots.

### 5. Generate images and continuous video

Give each shot one achievable primary action. Default to a locked camera. Use a slow pan, gentle follow, or very slow push only when movement reveals information. Avoid unmotivated orbits, drone dives, rapid zooms, constant rack focus, and shallow focus in every shot.

Generate one credible version first and no more than two composition options for a key emotional shot. If character or location continuity fails twice, stop batch generation, simplify the reference anchors, and regenerate only the affected shots.

Read [Continuous Video Generation](references/video-generation-workflow.md) before any video call. Lock the target duration and extension plan, create one initial storyboard image, and generate one short initial complete video. Then extend only the latest verified complete video, one step at a time, until the target duration is reached. Every video-call prompt uses a local timeline beginning at `00:00`; cumulative film time remains planning metadata. Do not concatenate independent clips, accept a tail-only clip as an extension, or simulate duration with loops, freezes, speed changes, or padding.

Set the aspect ratio only for the storyboard and initial video. After the initial video succeeds, lock its actual metadata ratio and omit the `ratio` field from every extension request so the input video controls the frame. After each call, verify the returned artifact, actual duration, ratio, identity, wardrobe, location, light, action direction, and audio continuity before continuing.

### 6. Design sound

Prioritize dialogue clarity, then ambient bed, action detail, and music. Establish space with refrigerator hum, dishes, rain on an awning, distant traffic, corridor footsteps, insects, or comparable sounds before adding music. Keep music sparse and unable to substitute for performance.

When music is requested or a compatible action is connected, generate a fully original instrumental cue matched to the verified final video duration. Preserve the completed video if audio generation or embedding fails; retry only the failed audio unit through the bounded recovery in [Continuous Video Generation](references/video-generation-workflow.md).

For a dialogue-free film, assign one recognizable ambient sound to each section and use one sound bridge or deliberate withdrawal of sound for the emotional turn.

### 7. Organize the Lumina canvas

Follow [Canvas Workflow](references/canvas-workflow.md) from left to right: brief → character/location anchors → script → storyboard → keyframes → continuous video chain → sound → final delivery. The initial video must trace back to its storyboard image; every extension must trace back to the immediately preceding verified complete video.

Run [Quality Check](references/quality-check.md) before delivery. Fix story logic in the script and storyboard before regenerating downstream assets; fix continuity errors only in the affected shots.

## Deliverables

Return, in order:

1. Assumptions and logline
2. Character relationship and emotional subtext
3. Location and visual anchors
4. Shootable short-drama script
5. Shot list with complete image and video prompts
6. Continuous video extension plan and verified lineage
7. Sound and editing plan
8. Canvas node and connection plan
9. Brief quality-check result

## Import safety

Before publishing or handing off the Skill repository, retain only `.md`, `.txt`, `.json`, `.yaml`, and `.yml` files, with lowercase extensions. Regular file and folder names must use only letters, numbers, underscores, and hyphens, with each name no longer than 64 characters. Name the license `license.md`, never extensionless `LICENSE`. Keep reference images, videos, archives, and generated outputs on the Lumina canvas rather than in the Skill repository.
