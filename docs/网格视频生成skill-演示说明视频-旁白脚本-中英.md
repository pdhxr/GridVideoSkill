# 网格视频生成 Skill · 演示说明视频旁白脚本（中英）

本文档是当前 **网页交互录屏 / 网格视频生成 Skill** 演示与说明视频的**旁白与字幕文字脚本**（作用类似 README：给人阅读，也给 AI Agent 对照成片与口播）。

- **成片**：`out/skill-explainer.mp4`（竖屏 1080×1920，硬烧中英字幕）
- **字幕源**：`public/captions/captions-zh-en.srt` / `captions-zh-en.ass`
- **旁白口播源**：`public/voice/scripts.json`
- **Skill 仓库**：https://github.com/pdhxr/GridVideoSkill

说明：下列中文为成片实际口播（与 `scripts.json` 一致）；English 为对应准确翻译。标注 *(visual only)* 的示例页当前成片无旁白，故无字幕。

---

## 1. 开场 Opening

**中文**

怎样做一个网页交互录屏视频的 Skill。从一次次踩坑，沉淀成可复用流程。

这是一个给人欣赏、给 AI Agent 学习并应用实操的视频。

**English**

How to build a Skill for web interaction screen recordings. From repeated pitfalls, refined into a reusable workflow.

This is a video for people to enjoy — and for AI Agents to learn and apply in practice.

*(口播文件为拼接后的 `opening.mp3` = 开场主句 + 短静音 + audience 句；对应 `scripts.json` 的 `openingFull`。)*

---

## 2. 第一 · 先确认再录 Confirm first

**中文**

第一，先确认再录。用户用自然语言描述需求后，AI 转成时间轴脚本，再画出带网页底图的操作示意图；开录前发起始帧，确认录屏范围。没 OK，不开录。

**English**

First: confirm before you record. After the user describes the need in natural language, the AI turns it into a timeline script, then draws an operation schematic on a webpage layout base; before recording, open a first-frame check to confirm the capture region. No OK — no recording.

### 示例 · 先确认再录 *(visual only)*

无旁白。画面为珠帘操作示意图（时间轴 · 关键点位 · 确认范围）Ken Burns 聚焦。

*(脚本稿 `confirmFirstDemo` 仍保留：这是珠帘操作示意图。时间轴、关键点位和确认范围，开录前先画清楚。 / This is the crystal-curtain operations schematic. Draw the timeline, key points, and confirm region clearly before recording.)*

---

## 3. 第二 · 目标定位 Targeting

**中文**

第二，目标定位。优先用 DOM 选择器现算坐标，像素坐标只作兜底。页面缩放或滚动之后，禁止继续用死坐标。

**English**

Second: target positioning. Prefer live coordinates from DOM selectors; pixel coords are fallback only. After zoom or scroll, never keep using hard-coded coordinates.

---

## 4. 第三 · 交互落到网页 Interaction

**中文**

第三，交互要落到网页。自定义光标叠层必须点击穿透。开录前用探针确认页面真的会变，正式开录前先激活目标窗口。

**English**

Third: interactions must land on the page. Custom cursor overlays must pass clicks through. Before recording, probe to confirm the page actually changes, and activate the target window before the real take.

### 示例 · 交互落到网页 *(visual only)*

无旁白。画面为按钮操作示意图。

*(稿 `interactionDemo`：按钮操作示意图：点哪里、怎么移开、动效怎么验，都写在图上。 / Button operations schematic: where to click, how to move away, and how to verify motion — all on the figure.)*

---

## 5. 第四 · 音效进成片 Audio

**中文**

第四，音效要进成片。用系统监视录下浏览器声。遇到 Web Audio 页面，先解锁用户手势。不要无故去掉音轨。

**English**

Fourth: sound effects must make the final cut. Capture browser audio via system monitoring. On Web Audio pages, unlock with a user gesture first. Do not drop the audio track without reason.

### 示例 · 音效进成片 *(visual only)*

无旁白。画面为按钮点击音效演示片段。

---

## 6. 第五 · 成片观感四条 Four rules

**中文**

第五，成片观感有四条硬规矩。点后移开鼠标；关键文案变化时放大看清；验证动效真正结束再二次操作；声音和画面要对齐。

**English**

Fifth: four hard rules for how the final cut feels. Move the cursor away after a click; zoom in when key copy changes so it stays readable; wait until the motion effect truly finishes before the next action; and keep sound aligned with picture.

### 示例 · 成片观感 *(visual only)*

无旁白。四宫格对照：点后移开 / 放大文案 / 等动效结束 / 拖拽过程。

*(稿 `fourRulesDemo`：点后移开鼠标、关键处放大、动效走完再点、声画对齐——四条都要过。 / Move away after click, zoom on key copy, wait for motion to finish, sync A/V — all four must pass.)*

---

## 7. 第六 · 专项目录 Dedicated directory

**中文**

第六，专项目录。每开一个页面录制任务，单独建一个目录。过程资料和成品，都只写进这个目录，不要混。

**English**

Sixth: a dedicated directory. For every page-recording task, create its own folder. Put process files and deliverables only there — do not mix.

### 示例 · 专项目录 *(visual only)*

无旁白。画面为 Finder 专项目录示意。

*(稿 `dedicatedDirDemo`：每个录制任务单独一个文件夹。珠帘和按钮演示，过程与成品都落在各自目录里。 / One folder per recording task. Curtain and button demos keep process files and deliverables in their own directories.)*

---

## 8. 第七 · 定稿后整理 Cleanup

**中文**

第七，定稿后整理。只留成品、脚本、示意图、光标素材和确认帧。试片和多余截图删掉，目录保持干净。

**English**

Seventh: clean up after the final cut. Keep only the deliverable, script, schematic, cursor assets, and confirm frames. Delete test takes and extra screenshots — keep the folder clean.

### 示例 · 定稿后整理 *(visual only)*

无旁白。画面为定稿与保留清单示意。

*(稿 `cleanupDemo`：定稿验收合格后，只留成片、脚本、示意图和清单，目录保持干净。 / After final acceptance, keep only the cut, script, schematic, and checklist — keep the folder clean.)*

---

## 9. 第八 · Skill 效果 Skill results

**中文**

第八，Skill 效果。经过制作前面两个视频修改后的 Skill 用起来怎么样？用它制作了 draw guess 的网页交互视频。

**English**

Eighth: Skill results. How does the Skill feel after refining it while making the first two videos? We used it to make a draw-guess web interaction video.

---

## 10. 总结 Closing

**中文**

总结一下：这个 Skill 既包含技术和细节的设计，也包含工程上的管理。做菜要好吃，做完菜也要把厨房台面收拾干净，不留垃圾残局。这是可复用流程 Skill，下次新页面功能想录制视频，使用这个 Skill 就行。

**English**

To sum up: this Skill covers both technical detail design and engineering management. Cooking should taste good — and after cooking, clear the counter; leave no mess. This is a reusable workflow Skill — next time you want to record a new page feature, just use this Skill.

---

## 附录 · `scripts.json` 字段对照

| Key | 成片是否口播 |
| --- | --- |
| `opening` / `audience` → `openingFull`（`opening.mp3`） | 是 |
| `confirmFirst` | 是 |
| `targeting` | 是 |
| `interaction` | 是 |
| `audio` | 是 |
| `fourRules` | 是 |
| `dedicatedDir` | 是 |
| `cleanup` | 是 |
| `skillEffect` | 是 |
| `closing` | 是 |
| `*Demo` 桥接旁白 | 否（mp3 在 `public/voice/_unused/`，示例页未挂 `voiceFile`） |
