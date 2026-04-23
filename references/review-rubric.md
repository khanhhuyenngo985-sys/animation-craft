# Review Rubric

Use this reference when reviewing existing UI animation or motion implementation.

## Review Output

Lead with findings. For each issue, include:

- Severity: P0, P1, P2, or P3.
- Finding: what is wrong.
- Risk: why it matters.
- Recommendation: the smallest useful fix.
- Verification: how to confirm the fix.

If there are no findings, say so and list unverified areas.

## Severity

| Severity | Meaning |
| --- | --- |
| P0 | Breaks interaction, causes severe accessibility risk, or makes content unusable. |
| P1 | Noticeable usability, performance, layout, or accessibility regression. |
| P2 | Quality issue that makes motion feel rough, confusing, or inconsistent. |
| P3 | Polish suggestion with low user impact. |

## What To Inspect

Purpose:

- Does the animation explain a state change?
- Does it provide useful feedback?
- Does it direct attention to the right place?
- Is it decorative without improving the experience?

Timing:

- Does feedback happen immediately?
- Do entrances feel intentional but not slow?
- Are exits faster than entrances when appropriate?
- Do repeated animations become tiring?

Hierarchy:

- Does the main subject move first?
- Are secondary elements quieter?
- Does motion compete with reading?
- Is the final resting frame clear?

Continuity:

- Can the user track objects across state changes?
- Are filtering, sorting, navigation, or modal transitions spatially understandable?
- Do elements teleport, flicker, or pop unexpectedly?

Accessibility:

- Is `prefers-reduced-motion` handled?
- Does meaning survive when motion is reduced?
- Are flashing, shaking, zooming, or large parallax effects avoided or justified?
- Are focus states and keyboard flows preserved?

Performance:

- Are `transform` and `opacity` preferred?
- Are layout properties animated without verification?
- Does the animation jank during interaction?
- Are canvas/WebGL/Three.js scenes nonblank and responsive?

Responsive behavior:

- Does motion still fit mobile screens?
- Do text and controls overlap during transitions?
- Do tap targets move unexpectedly?
- Does the first frame make sense on small viewports?

## Common Review Findings

Use these as patterns, not canned responses:

- The animation gives visual feedback only after async work completes, so the click feels ignored.
- The modal panel and backdrop animate with unrelated timing, so the entrance feels disconnected.
- Reduced-motion mode removes movement but also removes the only success indication.
- The list reorder fades items out and in, making it hard to track what changed.
- The animation moves text while it is being read, reducing legibility.
- A large transform on mobile causes controls to overlap during the peak frame.
- The WebGL scene starts blank while assets load, leaving no meaningful first frame.

## Verification Checklist

- Interact with the animated state at normal speed.
- Repeat the interaction several times.
- Check first frame, peak motion frame, and resting frame.
- Check mobile and desktop viewports.
- Check reduced-motion mode.
- Check keyboard and focus behavior where relevant.
- Run build, lint, typecheck, or tests when available.
