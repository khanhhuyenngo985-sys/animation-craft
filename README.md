# Animation Craft

[English](README.md) | [中文](README.zh-CN.md)

Animation Craft is an agent skill for animation video production: animated shorts, storyboards, animatics, AI-video shots, character performance, camera movement, continuity, editing rhythm, and sound-aware shot planning.

It is not a frontend/UI motion skill. Interface animation is out of scope unless explicitly requested.

| Focus | What It Helps With |
| --- | --- |
| Animated video | Premise, beat sheet, shot list, storyboard, animatic timing |
| AI-video prompting | Timed shot blocks for Seedance, 即梦, 可灵, 海螺, and image-to-video workflows |
| Character performance | Pose, gaze, breath, anticipation, action, reaction, settle |
| Scene motion | Camera logic, environment reaction, screen direction, light and weather continuity |
| Editing + sound | Shot rhythm, cut points, silence, impact cues, audio timing |
| Review + repair | Story clarity, staging, timing, identity drift, flicker, morphing, continuity |

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

Invoke the skill when asking an agent to create, refine, or review animation video work:

```text
Use $animation-craft to turn this idea into a 15-second AI-video shot with beginning, motion, ending state, camera, and sound cue.
```

```text
Use $animation-craft to plan a 30-second animated short with beat sheet, shot list, and animatic timing.
```

```text
Use $animation-craft to review this generated clip for story clarity, timing, continuity, and character drift.
```

## What The Skill Teaches

- Start from the visible change, not decorative motion.
- Build a shot from first frame, anticipation, action, impact, reaction, and settle.
- Use pose, props, scene constraints, light, silence, and sound cues to make story readable.
- Convert emotion into physical performance and timing.
- Preserve character, scene, prop, light, and screen-direction continuity across shots.
- Write AI-video prompts as timed visual events, not still-image descriptions.
- Review animation videos in order: story, staging, timing, performance, continuity, polish.

## Knowledge Base

| File | Load When |
| --- | --- |
| `references/animated-shorts.md` | Planning shorts, storyboards, shot lists, animatics, and character action |
| `references/visual-storytelling.md` | Making visual-first story beats readable without relying on dialogue |
| `references/animation-fundamentals.md` | Timing, spacing, anticipation, arcs, follow-through, weight |
| `references/motion-principles.md` | Video motion language, staging, rhythm, camera/object hierarchy |
| `references/motion-rules.md` | Practical rules for readable shot motion and continuity |
| `references/implementation-notes.md` | AI-video production notes, prompt timing, model handoff, verification |
| `references/review-rubric.md` | Auditing generated animation videos and writing repair notes |

## Examples

| File | Use For |
| --- | --- |
| `examples/storyboard-template.md` | Storyboard panel planning |
| `examples/ai-video-shot-template.md` | Timed AI-video shot prompt |
| `examples/continuity-ledger.md` | Multi-shot continuity tracking |
| `examples/animation-review-template.md` | Generated clip review and repair plan |

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
