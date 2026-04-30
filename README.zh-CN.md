# Animation Craft

[English](README.md) | [中文](README.zh-CN.md)

面向智能体的动画技能，用来创建、优化和评审动画短片、分镜、animatic、UI 动效和互动场景。

Animation Craft 帮助智能体先判断“为什么要动”，这个动作服务哪个故事或交互节拍，再决定动效强度、实现技术和验证方式。目标不是堆转场，而是让动画更清楚、更顺滑、更有表达。

| 方向 | 能帮你做什么 |
| --- | --- |
| 动画短片 | 故事节拍、镜头表、分镜结构、animatic、角色动作 |
| 视觉叙事 | 无对白表演、可读场景约束、道具驱动的因果 |
| 动效设计 | 微交互、状态过渡、加载状态、滚动效果、页面入场 |
| 技术实现 | CSS transitions、Web Animations API、Framer Motion、GSAP、Canvas、WebGL、Three.js |
| 质量评审 | 卡顿、节奏、可访问性、布局偏移、减少动态效果、视觉层级 |

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

当你希望智能体创建、优化或评审动效时，可以这样调用：

```text
Use $animation-craft to make this dashboard feel more responsive without adding decorative motion.
```

```text
Use $animation-craft to review the modal and loading animations for accessibility, timing, and layout issues.
```

```text
Use $animation-craft to outline a 30-second animated short with clear story beats, shot timing, and character action.
```

## 这个技能会教什么

核心技能文件提供一套紧凑工作流：

- 先判断动画的任务：反馈、连续性、引导或表达。
- 用 premise、节拍、镜头规划、staging 和 animatic 时间来组织动画短片。
- 用姿态、道具、场景、停顿和声音提示来承载视觉优先的故事节拍。
- 使用时间、间距、预备动作、跟随动作、弧线和重量感等动画基础。
- 使用层级、连续性、方向、克制和即时反馈等产品动效规律。
- 重要动效开始前，写一个很短的 motion brief。
- 根据交互选择节奏、缓动、层次和技术方案。
- 尊重 `prefers-reduced-motion`。
- 验证第一帧、运动峰值帧、静止帧、移动端表现，以及 Canvas/WebGL 是否正常渲染。
- 用严重度、风险、建议和验证步骤来评审动画。

## 知识库

`references/` 文件夹提供按需加载的扩展知识，不会把主技能文件撑得太重：

| 文件 | 什么时候读 |
| --- | --- |
| `references/animation-fundamentals.md` | 学习动画基础：时间、间距、预备动作、弧线、跟随动作 |
| `references/animated-shorts.md` | 规划动画短片、分镜、镜头表、animatic 和角色动作 |
| `references/visual-storytelling.md` | 让视觉优先的故事节拍更可读，不依赖台词或私有风格配方 |
| `references/motion-principles.md` | 规划动效语言、层级、staging、节奏和状态叙事 |
| `references/motion-rules.md` | 使用产品动效里的实用规律：反馈、层级、连续性和克制 |
| `references/implementation-notes.md` | 选择 CSS、WAAPI、Framer Motion、GSAP、Canvas、WebGL 或 Three.js |
| `references/review-rubric.md` | 评审已有动画，并写出可执行的问题、风险和建议 |

## 示例

`examples/` 文件夹包含一些常见动效任务的通用小片段：

| 文件 | 用途 |
| --- | --- |
| `examples/button-feedback.css` | hover、focus 和 pressed 的即时反馈 |
| `examples/modal-transition.css` | backdrop 和 panel 的入场/退出节奏 |
| `examples/list-reorder.css` | 保持对象连续性的列表变化 |
| `examples/reduced-motion.css` | reduced-motion 降级模式 |
| `examples/storyboard-template.md` | 动画短片的简单镜头规划模板 |

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
|   |-- button-feedback.css
|   |-- list-reorder.css
|   |-- modal-transition.css
|   |-- reduced-motion.css
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
