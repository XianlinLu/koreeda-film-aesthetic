<p align="center">
  <a href="#english">English</a> · <a href="#简体中文">简体中文</a>
</p>

<a id="english"></a>

# Humanist Family Short Drama Skill

A Lumina Canvas Agent skill that turns a premise, outline, or audiovisual reference into a restrained, human-centered short drama with a script, continuity anchors, storyboard, generation prompts, sound plan, and canvas layout.

## Import

Paste this repository URL into Lumina's Skill import screen. The entry file is `SKILL.md`.

All regular files use Lumina-supported lowercase text extensions. The license is named `license.md`, avoiding the extensionless `LICENSE` error shown by the importer. Reference images, videos, archives, and generated outputs are intentionally excluded from the repository.

## Lumina form copy

The following English text matches every field shown in the Skill form and stays within its limits.

### Skill name — 27/30 characters

```text
Humanist Family Short Drama
```

### One sentence introduction — 190/300 characters

```text
Create restrained, human-centered short dramas in Lumina Canvas from a premise or visual reference, with scripts, continuity anchors, shot prompts, sound design, and a clear canvas workflow.
```

### Instructions for use — 999/1,000 characters

```markdown
## When to use
Use this skill for quiet family drama, everyday-life stories, child-centered scenes, memory and loss, natural-light cinema, or a poetic short based on a visual reference.

## Workflow
1. Provide a premise, relationship, duration, aspect ratio, dialogue language, and references.
2. Choose Observation Mode for patient daily drama or Memory-Poem Mode for fragmented recollection.
3. Approve the creative brief, character anchor, location anchor, and 2–3 keyframes before generating every shot.
4. Generate one action per shot, then build dialogue, ambience, detail sounds, and restrained music.
5. Arrange the canvas from brief to anchors, script, storyboard, keyframes, videos, sound, and final sequence.
6. Run the quality checklist before export.

## Notes
Do not name a living director in generation prompts or copy a specific film, shot, character, dialogue, music, or signature image. Keep runtime media outside the Skill repository. Use only supported lowercase text extensions.
```

Use the editor's `Preview` control before saving to verify headings, lists, code blocks, links, images, and tables. Use `Copy` to back up or transfer the final text.

## Two creative modes

- **Observation Mode:** ordinary events, restrained dialogue, locked medium shots, everyday ambient sound, and an open ending.
- **Memory-Poem Mode:** present-day anchors connected to fragmented memories, with surreal imagery used sparingly rather than as spectacle.

Neither mode places a living filmmaker's name in downstream generation prompts or copies a specific film or reference video's characters, dialogue, plot, music, or signature images.

## Repository structure

```text
SKILL.md
README.md
license.md
references/
  aesthetic.md
  canvas-workflow.md
  prompt-patterns.md
  quality-check.md
  reference-video.md
```

The hidden `.skillignore` file is used only for Skill packaging and contains no runtime media.

## Example requests

> A daughter who has not returned home for years helps her father repot the old plants on his balcony on the night before a typhoon. Make it a 75-second 16:9 short drama with Mandarin dialogue.

> Using my uploaded memory film as a reference, make an 80-second dialogue-free short about the last day before an old barbershop is demolished. Keep the fragmented memories and still long takes without copying its exact images.

Review the creative brief, character anchor, and location anchor before asking the Agent to generate every shot.

---

<a id="简体中文"></a>

# 人文家庭电影感短剧 Skill

这是一个面向 Lumina 画布 Agent 的短剧创作 Skill。它把一句话故事、已有梗概或视听参考发展为脚本、连续性锚点、分镜、生成提示词、声音方案与画布编排。

## 导入

在 Lumina 的 Skill 导入界面粘贴本仓库地址，入口文件为 `SKILL.md`。

仓库中的普通文件均使用 Lumina 支持的小写文本扩展名。许可证命名为 `license.md`，不会触发无扩展名 `LICENSE` 的导入报错。参考图片、视频、压缩包和生成结果不会放入仓库。

## Lumina 表单英文文案

上方“Lumina form copy”提供了截图中三个字段对应的英文内容：

- Skill name：不超过 30 字符。
- One sentence introduction：不超过 300 字符。
- Instructions for use：不超过 1,000 字符，并包含适用场景、使用步骤和注意事项。

发布前使用编辑器的 `Preview` 检查标题、列表、代码块、链接、图片和表格；使用 `Copy` 备份或迁移最终文案。

## 两种创作模式

- **观察式家庭短剧：**日常事件、克制对白、固定中景、生活环境声和开放余韵。
- **记忆诗篇：**用现实锚点串联碎片化回忆，谨慎使用超现实意象，避免作品变成炫技 MV。

两种模式都不会在下游生成提示词中使用在世导演姓名，也不会复制具体电影或参考视频的角色、对白、情节、音乐和标志性镜头。

## 示例请求

> 一个多年没有回家的女儿，在台风前夜陪父亲给阳台上的旧花盆换土。做成 75 秒横屏短剧，普通话对白。

> 参考我上传的记忆短片，把“拆掉老理发店前的最后一天”做成 80 秒无对白短片；保留碎片化回忆和静止长镜头，但不要复制参考片中的具体意象。

第一次运行建议先检查创作简报、人物锚点和场景锚点，再让 Agent 批量生成镜头。
