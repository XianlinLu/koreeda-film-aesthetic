<p align="center">
  <a href="#english">English</a> · <a href="#简体中文">简体中文</a>
</p>

<a id="english"></a>

# Koreeda Film Aesthetic

A Lumina Canvas Agent skill that turns a premise, outline, or audiovisual reference into a restrained, human-centered short drama with adaptive language, continuity anchors, storyboard prompts, sequential full-video extension, original sound, and verified delivery.

## Import

Paste this repository URL into Lumina's Skill import screen. The entry file is `SKILL.md`.

All tracked documents use Lumina-supported lowercase text extensions. The license is named `license.md`, avoiding the extensionless `LICENSE` error shown by the importer. Reference images, videos, archives, and generated outputs are intentionally excluded from the repository.

## Lumina import requirements

The repository follows every requirement shown in the import warning:

- Supported document formats: `.md`, `.txt`, `.json`, `.yaml`, and `.yml`.
- File extensions must be lowercase.
- File and folder names may contain only uppercase and lowercase letters, numbers, underscores, and hyphens.
- Each file or folder name must be no longer than 64 characters.
- The extensionless `LICENSE` filename is not supported, so this repository uses `license.md`.
- The local Aime packaging file `.skillignore` is intentionally not tracked on the GitHub branch imported by Lumina.

The warning texts addressed by this repository are `LICENSE — Files only support .md, .txt, .json, .yaml, .yml formats` and `.skillignore — Files only support .md, .txt, .json, .yaml, .yml formats`.

## Lumina form copy

The following English text matches every field shown in the Skill form and stays within its limits.

### Skill name — 22/30 characters

```text
Koreeda Film Aesthetic
```

### One sentence introduction — 299/300 characters

```text
Turns premises into restrained, human-centered short films with adaptive language and video extension. [How to Use] Add a premise, duration, and references; approve the brief and storyboard. [Scenarios] Quiet family drama, memory and loss, poetic adaptation. [Outputs] Script, prompts, video, audio.
```

### Instructions for use — 992/1,000 characters

```markdown
## Language
Match visible text to the latest request; attachments and quotes do not override it. Unless specified, scripts and speech use that language; revisions retain draft language.

## Use
For dreamlike memory films with hard cuts, backlight, grain, and a still ending.

## Workflow
1. Provide premise, duration, ratio, language, references, and audio needs.
2. Create one asset node per character; each image shows one identity only.
3. Connect each asset to its generator, verify it, and obtain user approval.
4. If voice is requested, connect the approved asset to its audio node; generate and verify. Otherwise skip.
5. Approve storyboard and opening frame; generate the initial video.
6. Extend only the latest verified video. Start each call at 00:00; omit ratio.
7. Verify duration, ratio, identity, style, motion, and audio.

## Notes
Never combine characters or use unapproved assets downstream. Never concatenate clips or copy a film, shot, dialogue, music, or signature image.
```

Use the editor's `Preview` control before saving to verify headings, lists, code blocks, links, images, and tables. Use `Copy` to back up or transfer the final text.

The form limits shown by Lumina are: Skill name `30`, One sentence introduction `300`, and Instructions for use `1,000` characters. Skill name and one-sentence introduction are required fields.

## Adaptive language mechanism

- Visible UI text, questions, progress, errors, and delivery notes follow the language of the user's latest direct request.
- Attachments, quotations, drafts, references, metadata, names, and action output never override that language.
- An explicit story-language request controls scripts, dialogue, narration, subtitles, and speech.
- Revisions preserve the source draft's language unless the user requests a change.
- In mixed-language requests, an explicit language instruction wins; otherwise the newest substantive request determines the language, then the established conversation language, then English.
- Every generated film title, logline, synopsis, section heading, storyboard label, and body paragraph is checked before delivery. A Chinese request produces Chinese creative output unless English is explicitly requested.

## Continuous video workflow

The production chain follows the verified continuous-generation method from [Short Drama Creation](https://github.com/XianlinLu/short-drama-creation):

```text
target duration and ratio lock
→ continuity map and opening storyboard
→ short initial complete video
→ sequential extensions of the latest complete video
→ duration, ratio, and continuity verification after every call
→ original instrumental audio matched to the final duration
→ final verified complete video
```

Every video prompt starts its call-local timeline at `00:00`. The initial video establishes the actual ratio; every extension request omits `ratio` and inherits the input video's frame. Independent clips are never concatenated. A failed step keeps the latest verified complete video and retries only the failed unit within the documented recovery limits.

## Character asset and audio gate

Every character receives a separate asset node, and every character asset image contains exactly one identity—never a couple, family, group, background person, reflection, poster figure, or combined cast sheet. Each asset is generated and connected on the canvas, then shown to the user for explicit approval. Character-dependent generation pauses until approval.

Character audio is optional per character. When requested, it is generated only after the matching character asset is approved, using one dedicated audio node connected to that single approved asset. When audio is not requested for a character, no audio node is created. Every canvas edge and generated output must be verified before the workflow reports success.

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
  character-asset-workflow.md
  language-routing.md
  prompt-patterns.md
  quality-check.md
  reference-video.md
  video-generation-workflow.md
```

A local `.skillignore` is retained for Aime packaging but intentionally excluded from the GitHub branch imported by Lumina, because Lumina rejects that dotfile as an unsupported document.

## Reference-video style lock

Generated videos use the supplied `Kenopsia` file as a mandatory runtime style reference, not a loose mood-board. Before final generation, the Agent binds the uploaded video, creates four look-test frames plus one motion test, and waits for one explicit style approval. The locked look preserves localized white-gold/fire-orange clipping, cyan-green and olive-teal shadows, motivated backlight, bloom, amber-red halation, organic 35 mm grain, restrained chromatic fringing, and selective directional long-shutter blur at a 24-fps appearance. Opening, middle, strongest-motion, and ending samples are compared before delivery. If the connected action cannot consume the video or approved frame references, the Skill stops instead of claiming complete fidelity from prose or a final filter.

The Skill still creates new people, places, actions, music, and paradoxical imagery rather than copying the reference's exact shots, title, logos, music, or signature object combinations.

## Example requests

> A daughter who has not returned home for years helps her father repot the old plants on his balcony on the night before a typhoon. Make it a 75-second 16:9 short drama with Mandarin dialogue.

> Using my uploaded memory film as a reference, make an 80-second dialogue-free short about the last day before an old barbershop is demolished. Keep the fragmented memories and still long takes without copying its exact images.

Review the creative brief, character anchor, and location anchor before asking the Agent to generate every shot.

---

<a id="简体中文"></a>

# Koreeda Film Aesthetic（中文说明）

这是一个面向 Lumina 画布 Agent 的短剧创作 Skill。它把一句话故事、已有梗概或视听参考发展为克制、关注人物关系的短片，并提供自适应语言、连续性锚点、分镜提示词、连续视频延长、原创声音与交付校验。

## 导入

在 Lumina 的 Skill 导入界面粘贴本仓库地址，入口文件为 `SKILL.md`。

仓库中的普通文件均使用 Lumina 支持的小写文本扩展名。许可证命名为 `license.md`，不会触发无扩展名 `LICENSE` 的导入报错。本地 Aime 打包所需的 `.skillignore` 不再发布到供 Lumina 导入的 GitHub 分支，从而避免本次截图中的不支持格式与点号文件名报错。参考图片、视频、压缩包和生成结果不会放入仓库。

## Lumina 表单英文文案

上方“Lumina form copy”提供了截图中三个字段对应的英文内容：

- Skill name：不超过 30 字符。
- One sentence introduction：不超过 300 字符。
- Instructions for use：不超过 1,000 字符，并包含适用场景、使用步骤和注意事项。

发布前使用编辑器的 `Preview` 检查标题、列表、代码块、链接、图片和表格；使用 `Copy` 备份或迁移最终文案。

## 自适应语言机制

- 所有可见交互跟随用户最新直接请求的语言。
- 附件、引文、草稿、参考资料、元数据、专有名词和工具输出不会覆盖交互语言。
- 用户明确指定故事语言时，以该语言生成脚本、对白、旁白、字幕与语音。
- 修改或续写现有草稿时，默认保留原稿语言，除非用户要求更换。
- 混合语言请求优先服从明确的语言指令；否则跟随最新实质请求所用语言，再沿用对话语言，仍无法判断时使用英文。
- 交付前会检查片名、梗概、章节标题、分镜标签与正文；中文请求在没有明确英文指令时必须输出自然的简体中文内容。

## 连续视频生成流程

视频流程参考 [Short Drama Creation](https://github.com/XianlinLu/short-drama-creation)：先锁定目标时长与初始画幅，建立连续性地图和首帧分镜，再生成一段短的初始完整视频。之后每次只把上一次验证通过的完整视频作为输入逐步延长。

每次视频调用的提示词时间轴都从 `00:00` 开始。初始视频确定实际画幅，延长调用必须省略 `ratio`。每次返回后校验实际时长、画幅、人物、服装、场景、光线、运动方向和音频连续性。不拼接独立片段，不使用循环、定格、变速或填充伪造目标时长。失败时保留最近一次成功的完整视频，只重试失败步骤。

## 人物资产与音频确认门禁

每个人物必须使用独立的人物资产节点，每张人物资产图只能包含一个人物身份。严禁把两名及以上人物放进同一资产图或同一人物资产节点，也不能在背景、倒影、海报、屏幕或照片中出现第二个人物。每个人物资产都要在画布中连接到自己的生成节点，确认输出与连线成功后展示给用户，并等待明确确认。

只有用户需要某个人物的音频时，才在该人物资产确认通过后创建专属音频生成节点，并把这一个已确认的人物资产连接到对应音频节点；用户不需要该人物音频时不创建、不生成。人物音频还需再次核验节点对应关系、连线、实际输出、语言与时长。未确认的人物资产不得进入人物音频或后续视频生成。

## 参考视频风格锁定

`Kenopsia` 视频是运行时必须绑定的视觉参考，不是宽泛情绪板。最终生成前，Agent 必须把视频接入风格参考节点，先生成四张风格测试图与一段最短可用的横向运动测试，经过一次明确确认后才继续。锁定项包括局部白金/火橙高光溢出、青绿与橄榄蓝绿色阴影、强逆光、bloom、琥珀红色 halation、有机 35 mm 颗粒、轻微色差，以及 24 fps 观感下有方向的选择性长快门拖影。

交付前必须并排检查开场、中段空间镜头、最强运动模糊片段和结尾定镜。若连接的生成动作无法读取参考视频或已确认参考帧，Skill 会停止并说明限制，不会仅凭文字提示或后期滤镜声称“完全一致”。人物、地点、动作、音乐和矛盾意象仍保持原创，不复制参考片的具体镜头、片名、Logo、音乐或标志性物件组合。

## 两种创作模式

- **观察式家庭短剧：**日常事件、克制对白、固定中景、生活环境声和开放余韵。
- **记忆诗篇：**用现实锚点串联碎片化回忆，谨慎使用超现实意象，避免作品变成炫技 MV。

两种模式都不会在下游生成提示词中使用在世导演姓名，也不会复制具体电影或参考视频的角色、对白、情节、音乐和标志性镜头。

## 示例请求

> 一个多年没有回家的女儿，在台风前夜陪父亲给阳台上的旧花盆换土。做成 75 秒横屏短剧，普通话对白。

> 参考我上传的记忆短片，把“拆掉老理发店前的最后一天”做成 80 秒无对白短片；保留碎片化回忆和静止长镜头，但不要复制参考片中的具体意象。

第一次运行建议先检查创作简报、人物锚点和场景锚点，再让 Agent 批量生成镜头。
