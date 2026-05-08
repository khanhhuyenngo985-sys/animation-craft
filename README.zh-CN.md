# Animation Craft

[English](README.md) | [中文](README.zh-CN.md)

Animation Craft 是面向动画视频制作的智能体技能：动画短片、分镜、animatic、AI 视频镜头、角色表演、镜头运动、连续性、剪辑节奏、声音节拍和图生视频提示词。

它不是前端/UI 动效技能。除非用户明确要求界面动画，否则不要把它用于网页、组件、CSS、React 或微交互。

| 方向 | 能帮你做什么 |
| --- | --- |
| 动画视频 | premise、节拍表、镜头表、分镜、animatic 时间 |
| AI 视频提示词 | Seedance、即梦、可灵、海螺、图生视频的分秒镜头块 |
| 角色表演 | 姿态、眼神、呼吸、预备动作、行动、反应、落定 |
| 场景运动 | 镜头逻辑、环境反应、轴线、光线/天气连续性 |
| 剪辑与声音 | 镜头节奏、剪辑点、静默、撞击声、声音时间点 |
| 审片与修复 | 故事可读性、调度、节奏、身份漂移、闪烁、变形、连续性 |

## 安装

使用 Skills CLI：

```bash
npx skills add khanhhuyenngo985-sys/animation-craft -g
```

手动安装：

```bash
mkdir -p ~/.agents/skills
git clone https://github.com/khanhhuyenngo985-sys/animation-craft ~/.agents/skills/animation-craft
```

## 使用

当你希望智能体制作、优化或评审动画视频时调用：

```text
Use $animation-craft to turn this idea into a 15-second AI-video shot with beginning, motion, ending state, camera, and sound cue.
```

```text
Use $animation-craft to plan a 30-second animated short with beat sheet, shot list, and animatic timing.
```

```text
Use $animation-craft to review this generated clip for story clarity, timing, continuity, and character drift.
```

## 这个技能会教什么

- 从“可见变化”开始，而不是从装饰性运动开始。
- 用第一帧、预备、行动、撞击、反应、落定构建镜头。
- 用姿态、道具、场景约束、光线、静默和声音提示让故事可读。
- 把情绪翻译成身体表演和时间节奏。
- 在多镜头中保护角色、场景、道具、光线和轴线连续性。
- 把 AI 视频提示词写成分秒发生的视觉事件，而不是静态图片描述。
- 审片顺序固定为：故事、调度、节奏、表演、连续性、制作瑕疵。

## 知识库

| 文件 | 什么时候读 |
| --- | --- |
| `references/animated-shorts.md` | 规划动画短片、分镜、镜头表、animatic、角色动作 |
| `references/visual-storytelling.md` | 用视觉节拍讲清楚故事，不依赖台词 |
| `references/animation-fundamentals.md` | 时间、间距、预备动作、弧线、跟随动作、重量 |
| `references/motion-principles.md` | 视频运动语言、调度、节奏、镜头/主体层级 |
| `references/motion-rules.md` | 可读镜头运动和连续性的实用规则 |
| `references/implementation-notes.md` | AI 视频制作、提示词时间轴、模型交付和验证 |
| `references/review-rubric.md` | 评审生成视频并输出修复意见 |

## 示例

| 文件 | 用途 |
| --- | --- |
| `examples/storyboard-template.md` | 分镜面板规划 |
| `examples/ai-video-shot-template.md` | 分秒 AI 视频镜头提示词 |
| `examples/continuity-ledger.md` | 多镜头连续性记录 |
| `examples/animation-review-template.md` | 生成片段审片与修复计划 |

## 仓库结构

```text
animation-craft/
|-- LICENSE
|-- SKILL.md
|-- README.md
|-- README.zh-CN.md
|-- agents/
|   `-- openai.yaml
|-- examples/
|   |-- README.md
|   |-- ai-video-shot-template.md
|   |-- animation-review-template.md
|   |-- continuity-ledger.md
|   `-- storyboard-template.md
`-- references/
    |-- animated-shorts.md
    |-- animation-fundamentals.md
    |-- implementation-notes.md
    |-- motion-principles.md
    |-- motion-rules.md
    |-- review-rubric.md
    `-- visual-storytelling.md
```

## License

MIT
