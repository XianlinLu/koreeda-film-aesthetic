# Adaptive Language Routing

Resolve language before any outline, title, script, canvas node, media prompt, or visible response. Track two independent values: `interaction_language` for visible Agent communication and `story_language` for creative output.

## Interaction language

Resolve `interaction_language` from the user's newest direct request. Do not let attachments, quoted passages, pasted drafts, retrieved sources, code, metadata, proper names, or action output override it.

When the direct request mixes languages, apply this order:

1. Follow an explicit instruction such as “reply in English” or “请用中文”.
2. Otherwise use the language carrying the newest substantive request.
3. Otherwise retain the established conversation language.
4. If no language is established, use English.

Use `interaction_language` for every visible UI title, heading, field label, question, choice, plan, progress update, action summary, error, quality check, canvas node label, and final delivery note. Translate semantic template labels such as “Creative Brief,” “Shot List,” and “Quality Check”; do not copy them literally from the English-authored Skill when the resolved language is not English.

## Story language

Resolve `story_language` separately:

1. Follow an explicit requested language for the script or video.
2. For revision, continuation, or adaptation, preserve the existing draft's language unless the user asks to change it.
3. Otherwise set `story_language` equal to `interaction_language`.

Use `story_language` for the film title, logline, synopsis, creative brief content, script, scene headings, dialogue, narration, subtitles, on-screen story text, and speech generation. If a connected action performs best with a different technical prompt language, translate only the hidden action parameter; keep visible communication and creative output in their resolved languages.

## Mandatory output gate

Before every visible response and final delivery:

1. Inspect titles, section headings, paragraphs, dialogue, subtitles, node labels, status text, errors, and final notes.
2. Confirm each item uses `interaction_language` or `story_language` according to its role.
3. When the latest direct request is Chinese and no explicit English story language exists, reject an English film title or English story body and rewrite it in natural Simplified Chinese.
4. Preserve proper nouns, filenames, technical parameter names, and user-requested bilingual wording only where necessary.
5. Never infer English output merely because this Skill, its examples, or its prompt templates are written in English.

## Examples

- A Chinese request with an English reference document produces Chinese interaction; the reference language does not override the user.
- “Please explain in English, but keep the Mandarin dialogue” uses English interaction and Mandarin story dialogue.
- A Chinese revision request for an English draft receives Chinese guidance while the revised story remains English.
- “做一个关于旧校舍的短片” produces a Chinese film title, Chinese synopsis, Chinese storyboard labels, and Chinese delivery notes. Only hidden technical prompts may remain English when an action requires them.
