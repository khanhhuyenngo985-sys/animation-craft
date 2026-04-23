# Animation Craft

Purposeful UI motion for agents that build, refine, and review animation.

Animation Craft helps an agent decide why something should move, how much motion the interface can afford, which implementation technique fits the job, and how to verify the result without turning the product into a pile of decorative transitions.

| Focus | What It Helps With |
| --- | --- |
| Motion design | Micro-interactions, transitions, loading states, scroll effects, page entrances |
| Implementation | CSS transitions, Web Animations API, Framer Motion, GSAP, Canvas, WebGL, Three.js |
| Quality review | Jank, timing, accessibility, layout shifts, reduced motion, visual hierarchy |
| Public safety | Useful public guidance without private style recipes or proprietary assets |

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

## What The Skill Teaches

The core skill file gives the agent a compact workflow:

- Start from the animation's job: feedback, continuity, guidance, or expression.
- Write a tiny motion brief before significant changes.
- Choose timing, easing, layering, and tooling based on the interaction.
- Respect `prefers-reduced-motion`.
- Verify first frame, peak motion, resting frame, mobile behavior, and rendered canvas/WebGL output.
- Review animation with severity, risk, recommendation, and verification steps.

## Knowledge Base

The `references/` folder adds optional depth without bloating the main skill:

| File | Load When |
| --- | --- |
| `references/motion-principles.md` | Planning motion language, hierarchy, staging, rhythm, and state storytelling |
| `references/implementation-notes.md` | Choosing CSS, WAAPI, Framer Motion, GSAP, Canvas, WebGL, or Three.js |
| `references/review-rubric.md` | Auditing existing animation and writing actionable review findings |

## Repository Layout

```text
animation-craft/
|-- SKILL.md
|-- README.md
|-- agents/
|   `-- openai.yaml
`-- references/
    |-- implementation-notes.md
    |-- motion-principles.md
    `-- review-rubric.md
```

## Public Boundary

This is a public skill. It intentionally contains general heuristics, safe defaults, and review rubrics, not private animation recipes, signature sequences, proprietary prompts, client examples, or reusable internal assets.

## License

No license has been added yet. Add one before redistributing beyond normal GitHub viewing or internal use.
