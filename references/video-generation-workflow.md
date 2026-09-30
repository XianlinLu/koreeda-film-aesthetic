# Continuous Video Generation Workflow

Use this workflow for the final moving-image artifact. Storyboard shots remain planning units; they are not independent clips to concatenate.

## 0. Bind and approve the look

Before capability checks, add the supplied `Kenopsia` video as `reference_00_kenopsia` and connect it to the available project-style or visual-reference route. Create `style_lock_00`, four look-test images, and one shortest-supported lateral-motion test as specified in [Kenopsia Reference Style Lock](reference-video.md).

Do not proceed until the user approves the tests and the canvas records `style_lock_status: approved`. If the action cannot accept the uploaded video or approved frame references, stop before final generation. Do not substitute a text-only approximation or an end-stage filter while claiming complete fidelity.

## 1. Check capabilities and lock the plan

Before generation, confirm that connected actions can:

- create a reference-aware storyboard image;
- consume the uploaded style video or approved look-test frames;
- turn that image into an initial video;
- extend the latest complete video and return a longer complete video;
- report trustworthy duration and frame metadata.

If true full-video extension or duration metadata is unavailable, stop at the earliest safe state and report the limitation. Do not present isolated continuation clips as a continuous final film.

Lock the requested target duration, supported initial duration, supported extension increments, action tolerance, and maximum cumulative duration. If the exact target is unreachable, offer only supported outcomes and wait for the user to choose; do not round silently.

Choose the initial aspect ratio from the user's explicit choice, named destination, composition, or the connected actions' shared default, in that order. Use the same orientation for the storyboard and initial video.

## 2. Build a continuity map

Plan one continuous film and record:

- character identity, wardrobe, and carried objects;
- location geometry, weather, light direction, and color;
- one C1–C10 camera recipe, lens tendency, composition, and at most one focus/exposure gesture for each beat;
- opening action and continuation-ready end state for each generation call;
- prop positions, screen direction, camera behavior, and emotional progression;
- dialogue, ambience, action sound, and music curve.
- reference-style invariants: intense backlight, gold-to-cyan palette, organic grain, halation, focus pattern, rhythmic hard cuts, and the final locked spatial image.
- a declared blur mode, readable subject anchor, and directional motion vector for every moving beat.

Global film time belongs only in planning metadata. Prompts use call-local time.

## 3. Generate the initial video

Create one storyboard image as the opening frame. Verify identity, composition, location, and light before animating it.

Generate one short initial complete video. Its prompt describes only that call and begins at `00:00`. End in a stable state that can continue naturally.

After the action returns, verify:

- a playable artifact exists;
- actual duration matches the requested initial duration within tolerance;
- actual width and height establish the locked ratio;
- identity, wardrobe, scene layout, light, motion, and audio remain coherent;
- the `Kenopsia` style invariants are visibly present rather than added as a final filter;
- shadows remain cyan-green or olive-teal, highlights remain white-gold or fire-orange, and localized clipping, bloom, halation, and grain agree with the approved look test;
- motion blur matches the declared mode and movement vector without whole-frame Gaussian softness, doubled anatomy, or optical-flow warping;
- the selected camera recipe remains legible and is not diluted by incompatible zoom, orbit, rack-focus, shake, or tracking instructions;
- the final frame is suitable for continuation.

Use the actual returned ratio only for validation and delivery metadata.

## 4. Extend sequentially

For each extension:

1. Submit the latest verified complete video, never an earlier version or independent clip.
2. Omit the `ratio` field entirely. Do not send the locked ratio, `auto`, `null`, or an empty value.
3. Describe only the next story beat and use a local timeline beginning at `00:00`.
4. Preserve identity, wardrobe, scene geometry, backlight direction, cyan-green/olive-teal shadows, white-gold/fire-orange highlights, localized clipping, grain, halation, chromatic fringing, focus behavior, declared blur mode, motion direction, props, camera logic, and audio continuity.
5. Wait for the returned full video before starting the next extension.
6. Verify that the artifact is complete, its duration increased by the expected amount, its ratio matches the input, continuity remains acceptable, and its start/middle/end frames still match the approved look test.
7. Promote it to the new checkpoint only after verification.

Reject tail-only clips, unintended scene resets, identity drift, incorrect duration increases, or outputs that change the frame shape. Do not concatenate independent clips or reach duration through loops, freezes, speed changes, padding, or silent rounding.

## 5. Recover only the failed step

Always preserve the latest successful complete video and every verified upstream asset.

### Ratio constraint

If an extension reports `InvalidParameter.TaskTypeConstraint` for `ratio`, remove the field and retry only that extension once with the same input video, duration, local timeline, story beat, and other valid parameters. If the connector reinserts `ratio`, stop and report the real action name, request or log identifier, and rejected field.

### Copyright-policy rejection

For output-side video or audio copyright restrictions, do not repeat identical inputs, obscure names, transform rejected media to evade detection, or switch providers solely to bypass the result.

Preserve the checkpoint and audit named works, creators, performers, characters, brands, exact-scene requests, recognizable recordings, logos, watermarks, signature props, and iconic staging. If the input itself is recognizable third-party material or its origin is unclear, stop automatic retry and request an original, unbranded replacement.

Otherwise allow at most two targeted recovery attempts:

1. Rewrite only the failed prompt using functional story, motion, lighting, material, lens, performance, and sound language; remove names, exact-recreation wording, signature elements, lyrics, samples, and likeness requests.
2. If the same policy class persists, replace the failed visual or audio expression. For video, change at least three dimensions such as environment, camera, blocking, props, palette, weather, or composition. For music, change at least four dimensions such as tempo, meter, contour, harmony, instrumentation, sound palette, structure, or cadence.

Retry only the failed initial, extension, music, speech, effect, or embedding step. After two rejected recovery attempts, stop that branch, return the last verified complete video when available, and report the actual stage, error code, request or log identifier, and attempted compliant rewrites.

## 6. Finish sound and delivery

Create a fully original instrumental cue matched to the verified final duration when a compatible action is connected. Dialogue clarity comes first, followed by ambience, action detail, and music. Embed audio only through a route that preserves the single continuous video; otherwise deliver it separately with synchronization guidance.

Final acceptance requires one traceable lineage from the initial video through every verified extension, a verified target duration and ratio, coherent character and environment continuity, sustained reference-style invariants, zero-based timelines for all video calls, and no independent-clip concatenation. Compare at least four samples beside the source and approved look tests: opening, middle spatial anchor, strongest motion-blur fragment, and final held shot. Reject delivery if palette, exposure, optical texture, or selective blur has drifted.

This workflow is adapted from the continuous-generation principles documented in [Short Drama Creation](https://github.com/XianlinLu/short-drama-creation), while preserving this Skill's restrained family-drama aesthetic and originality safeguards.
