# Animation Craft

[English](README.md) | [中文](README.zh-CN.md)

面向智能体的 UI 动效技能，用来创建、优化和评审有目的的动画。

Animation Craft 帮助智能体先判断“为什么要动”，再决定动效强度、实现技术和验证方式。目标不是堆转场，而是让界面更清楚、更顺滑、更有反馈。

| 方向 | 能帮你做什么 |
| --- | --- |
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

## 这个技能会教什么

核心技能文件提供一套紧凑工作流：

- 先判断动画的任务：反馈、连续性、引导或表达。
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
| `references/motion-principles.md` | 规划动效语言、层级、staging、节奏和状态叙事 |
| `references/motion-rules.md` | 使用产品动效里的实用规律：反馈、层级、连续性和克制 |
| `references/implementation-notes.md` | 选择 CSS、WAAPI、Framer Motion、GSAP、Canvas、WebGL 或 Three.js |
| `references/review-rubric.md` | 评审已有动画，并写出可执行的问题、风险和建议 |

## 仓库结构

```text
animation-craft/
|-- SKILL.md
|-- README.md
|-- README.zh-CN.md
|-- agents/
|   `-- openai.yaml
`-- references/
    |-- animation-fundamentals.md
    |-- implementation-notes.md
    |-- motion-principles.md
    |-- motion-rules.md
    `-- review-rubric.md
```

## License

这个仓库暂时还没有添加 license。如果要进一步分发，建议先补充 license。
