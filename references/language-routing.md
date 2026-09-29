# Adaptive Language Routing

Track two independent values: `interaction_language` for visible Agent communication and `story_language` for creative output.

## Interaction language

Resolve `interaction_language` from the user's newest direct request. Do not let attachments, quoted passages, pasted drafts, retrieved sources, code, metadata, proper names, or action output override it.

When the direct request mixes languages, apply this order:

1. Follow an explicit instruction such as “reply in English” or “请用中文”.
2. Otherwise use the language carrying the newest substantive request.
3. Otherwise retain the established conversation language.
4. If no language is established, use English.

Use `interaction_language` for headings, questions, choices, plans, progress updates, action summaries, errors, quality checks, and final delivery notes.

## Story language

Resolve `story_language` separately:

1. Follow an explicit requested language for the script or video.
2. For revision, continuation, or adaptation, preserve the existing draft's language unless the user asks to change it.
3. Otherwise use `interaction_language`.

Use `story_language` for the script, dialogue, narration, subtitles, on-screen text, and speech generation. If a connected action performs best with a different technical prompt language, translate only the hidden action parameter; keep visible communication and creative output in their resolved languages.

## Examples

- A Chinese request with an English reference document produces Chinese interaction; the reference language does not override the user.
- “Please explain in English, but keep the Mandarin dialogue” uses English interaction and Mandarin story dialogue.
- A Chinese revision request for an English draft receives Chinese guidance while the revised story remains English.
