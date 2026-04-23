# Animation Craft

[English](README.md) | [中文](README.zh-CN.md)

Purposeful animation guidance for agents that build, refine, and review animated shorts, storyboards, animatics, UI motion, and interactive scenes.

Animation Craft helps an agent decide why something should move, what story or interaction beat the motion serves, which implementation technique fits the job, and how to verify the result without turning the work into a pile of decorative transitions.

| Focus | What It Helps With |
| --- | --- |
| Animated shorts | Story beats, shot lists, storyboard structure, animatics, character action |
| Motion design | Micro-interactions, transitions, loading states, scroll effects, page entrances |
| Implementation | CSS transitions, Web Animations API, Framer Motion, GSAP, Canvas, WebGL, Three.js |
| Quality review | Jank, timing, accessibility, layout shifts, reduced motion, visual hierarchy |

## Install

With the Skills CLI:

```bash
npx skills add khanhhuyenngo985-sys/animation-craft -g
```

Manual install:

```bash
mkdir -p ~/.agents/skills
git clone https://github.com/khanhhuyenngo985-sys/animation-craft ~/.agents/skills/animation-craft
```

## Use

Invoke the skill when asking an agent to create, refine, or review motion:

```text
Use $animation-craft to make this dashboard feel more responsive without adding decorative motion.
```

```text
Use $animation-craft to review the modal and loading animations for accessibility, timing, and layout issues.
```

```text
Use $animation-craft to outline a 30-second animated short with clear story beats, shot timing, and character action.
```

## What The Skill Teaches

The core skill file gives the agent a compact workflow:

- Start from the animation's job: feedback, continuity, guidance, or expression.
- Shape animated shorts with premise, beats, shot planning, staging, and animatic timing.
- Apply animation fundamentals such as timing, spacing, anticipation, follow-through, arcs, and object weight.
- Use practical motion rules for hierarchy, continuity, direction, restraint, and responsive feedback.
- Write a tiny motion brief before significant changes.
- Choose timing, easing, layering, and tooling based on the interaction.
- Respect `prefers-reduced-motion`.
- Verify first frame, peak motion, resting frame, mobile behavior, and rendered canvas/WebGL output.
- Review animation with severity, risk, recommendation, and verification steps.

## Knowledge Base

The `references/` folder adds optional depth without bloating the main skill:

| File | Load When |
| --- | --- |
| `references/animation-fundamentals.md` | Learning animation basics: timing, spacing, anticipation, arcs, follow-through |
| `references/animated-shorts.md` | Planning animated shorts, storyboards, shot lists, animatics, and character action |
| `references/motion-principles.md` | Planning motion language, hierarchy, staging, rhythm, and state storytelling |
| `references/motion-rules.md` | Applying practical UI motion rules for feedback, hierarchy, continuity, and restraint |
| `references/implementation-notes.md` | Choosing CSS, WAAPI, Framer Motion, GSAP, Canvas, WebGL, or Three.js |
| `references/review-rubric.md` | Auditing existing animation and writing actionable review findings |

## Examples

The `examples/` folder contains small generic snippets for common animation tasks:

| File | Use For |
| --- | --- |
| `examples/button-feedback.css` | Immediate hover, focus, and pressed feedback |
| `examples/modal-transition.css` | Backdrop and panel entrance/exit timing |
| `examples/list-reorder.css` | Trackable list changes with object constancy |
| `examples/reduced-motion.css` | Reduced-motion fallback patterns |
| `examples/storyboard-template.md` | Simple shot planning template for animated shorts |

## Repository Layout

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
    `-- review-rubric.md
```

## License

MIT
