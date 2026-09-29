# Character Asset and Optional Audio Workflow

Apply this workflow whenever the story contains one or more characters.

## 1. Build the character registry

Create one registry entry for each distinct character identity. Record the character's localized display name, narrative role, visible appearance, wardrobe, carried object, and continuity notes. Assign stable IDs such as `character_01`, `character_02`, and `character_03`.

Do not merge family members, doubles, age variants, or background figures into one identity. When the same person appears at different ages and must look materially different, treat each age state as its own asset version and document the relationship.

## 2. Generate one character per asset node

Create exactly one character asset node for each registry entry. The generated asset may contain front, side, back, or expression views of that same identity, but no second character may appear anywhere in the image.

Forbidden outputs include:

- couples, families, teams, crowds, or comparison lineups in one character asset;
- two different identities on one character sheet;
- a main character with another person visible in the background, reflection, poster, screen, or photograph;
- a combined “all characters” asset node.

If a user provides a group reference, use it only to extract separate continuity descriptions. Generate each person independently in a dedicated node. Validate that each result contains exactly one identity before accepting it.

## 3. Connect and confirm assets

For every character:

1. Connect the character description or source reference to that character's dedicated asset-generation node.
2. Run the image action and confirm a real output was returned.
3. Verify that the output is attached to the correct character node and that the canvas edge exists.
4. Check identity, wardrobe, view consistency, and the one-character-only rule.
5. Present the character asset to the user with its localized name and version.
6. Stop for explicit approval before using it in any character-dependent audio or video generation.

The user may approve characters individually or as a clearly enumerated batch. Keep approved nodes unchanged. If one asset is rejected, regenerate only that character and invalidate only its dependent outputs.

## 4. Generate optional character audio

Character audio is opt-in for each character. Determine the requested scope explicitly:

- If the user requests audio for a character, wait until that character's asset is approved.
- If the user does not request audio for a character, do not create or run an audio-generation node for that character.
- If the request names only some characters, generate audio only for those approved characters.

Create one dedicated audio-generation node per requested character. Before generation, connect the approved character asset node to its matching audio node and verify that no other character asset feeds it. Use the approved image together with the user's character description and dialogue needs to choose non-sensitive voice properties such as apparent age range, pace, register, texture, clarity, and emotional energy. Do not infer ethnicity, health, private history, or a real person's identity from appearance, and do not imitate a named performer.

After generation, verify that the audio output is attached to the matching node, the voice remains consistent, and its duration and dialogue language are correct. Present it for user confirmation before using it in scene video.

## 5. Downstream connections

- Connect each approved character asset node separately to every scene-generation node in which that character appears. A multi-character scene may receive multiple separate character nodes; the source assets themselves remain one-character-only.
- Connect only approved character-audio nodes to dialogue or scene-video nodes.
- Record asset and audio version IDs on each dependent node.
- When a character asset changes, invalidate that character's audio and every dependent scene output. When only the voice changes, invalidate that character's dialogue and dependent scene audio, not unrelated assets.
- Do not claim that generation or connection succeeded until the canvas reports both a real output and the intended edge.

## Node naming

Use stable pairs such as:

```text
character_01_yuki
voice_01_yuki
character_02_mother
voice_02_mother
```

Localize visible node labels to `interaction_language` while preserving stable internal IDs when the canvas requires them.
