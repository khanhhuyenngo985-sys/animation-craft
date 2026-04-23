---
name: animation-craft
description: Use when creating, refining, or reviewing UI animation, motion design, transitions, micro-interactions, hover effects, loading states, scroll effects, canvas/SVG motion, Three.js motion, or interfaces that should feel more alive.
---

# Animation Craft

## Overview

Use animation to clarify cause and effect, guide attention, provide feedback, and add character. Motion should make the interface easier to understand first, more delightful second.

## Start Here

Before adding motion, inspect the existing product, audience, design language, and technical stack. If the context is unclear, make a reasonable assumption and keep the first pass restrained.

Identify the animation's job:

- Feedback: acknowledge a click, hover, drag, save, error, or success.
- Continuity: make show/hide, route changes, tabs, drawers, modals, and layout changes feel connected.
- Guidance: direct attention to the next meaningful thing.
- Expression: give a hero, game scene, empty state, or brand moment a memorable personality.

Choose one primary motion moment, then add supporting micro-interactions. A few coordinated animations usually feel better than many unrelated ones.

## Animation Brief

For substantial animation work, write a tiny working brief before editing:

- Intent: what should the user understand or feel after the motion?
- Subject: what is the main moving element, and what should stay calm?
- Trigger: load, hover, click, drag, scroll, route change, data update, or time.
- Scale: micro, component, page, scene, or full experience.
- Tone: calm, precise, playful, cinematic, technical, organic, or game-like.
- Constraint: performance budget, device class, accessibility, or framework limits.

If a motion idea cannot be tied to intent, cut or simplify it.

## Knowledge Base

Load optional references only when the task needs more depth:

- `references/animation-fundamentals.md`: animation basics such as timing, spacing, anticipation, follow-through, arcs, squash/stretch, and silhouette.
- `references/motion-principles.md`: planning motion language, hierarchy, staging, rhythm, object constancy, and state storytelling.
- `references/motion-rules.md`: practical UI motion rules of thumb for feedback, hierarchy, continuity, restraint, and scene composition.
- `references/implementation-notes.md`: choosing CSS, Web Animations API, Framer Motion, GSAP, Canvas, WebGL, or Three.js, plus performance and verification details.
- `references/review-rubric.md`: reviewing existing animation and writing actionable findings with severity, risk, recommendation, and verification.
- `examples/README.md`: small public snippets for buttons, modals, list changes, and reduced-motion behavior.

## Motion Plan

For non-trivial work, form a short plan before implementation:

- Signature moment: the one animation users should remember.
- Feedback layer: interactions that need immediate visual acknowledgment.
- Transition layer: state changes that currently feel abrupt.
- Accessibility layer: how reduced-motion users experience the same flow.
- Verification target: screenshot, Playwright check, browser inspection, or manual interaction.

## Timing

Use durations by purpose:

| Purpose | Duration |
| --- | --- |
| Tap, click, toggle, pressed state | 80-160ms |
| Hover, focus, small feedback | 120-220ms |
| Menu, popover, tooltip, tab content | 180-300ms |
| Drawer, modal, accordion, layout transition | 250-450ms |
| Page entrance, hero sequence, scene reveal | 450-800ms |

Exit animations should usually be faster than entrance animations. Use about 70-80% of the enter duration.

Prefer natural deceleration:

```css
:root {
  --ease-out-quart: cubic-bezier(0.25, 1, 0.5, 1);
  --ease-out-quint: cubic-bezier(0.22, 1, 0.36, 1);
  --ease-out-expo: cubic-bezier(0.16, 1, 0.3, 1);
  --ease-in-out-soft: cubic-bezier(0.65, 0, 0.35, 1);
}
```

Avoid default-feeling motion. Avoid bouncy or elastic easing unless the product style explicitly calls for playfulness.

## Staging And Rhythm

Borrow from animation staging without overcomplicating UI:

- Establish stillness before motion so the moving element has contrast.
- Move the most important element first; supporting elements follow.
- Use stagger to reveal hierarchy, not to decorate every item.
- Let motion settle cleanly before asking for the next decision.
- Keep repeated loops subtle; looping motion should not compete with reading or clicking.
- Use distance to imply importance: important elements can travel farther, utility controls should move less.
- Use scale changes sparingly; large scale shifts can feel cheap or destabilizing.

For page or scene animation, think in beats: setup, reveal, response, settle. Most UI moments only need two or three beats.

## Implementation Guidance

Use the simplest tool that can express the motion well:

- CSS transitions for hover, focus, pressed states, color, opacity, and transform.
- CSS keyframes for simple repeated or entrance sequences.
- Web Animations API for controlled imperative animations without adding a library.
- Framer Motion in React projects that already use it or need shared layout transitions.
- GSAP for timeline-heavy animation, complex choreography, or SVG/canvas-heavy sequences.
- Canvas or WebGL for particle systems, games, simulations, and full-bleed interactive scenes.
- Three.js for 3D motion; verify the canvas is nonblank, framed correctly, and interactive.

Prefer animating `transform` and `opacity`. Avoid animating layout properties such as `top`, `left`, `width`, `height`, and `margin` unless there is a strong reason and performance is verified.

Use `will-change` sparingly and remove it when the element is no longer animating if possible.

## Layering

Good motion often comes from layered changes, not one dramatic effect:

- Primary layer: the element whose state is changing.
- Context layer: nearby labels, icons, shadows, or surfaces that explain the change.
- Ambient layer: background or decorative motion, used only when it does not reduce clarity.

Use no more layers than the moment needs. If three animated things compete for attention, choose the one that carries meaning and quiet the rest.

## Patterns

Entrance:

- Fade plus subtle translate or scale.
- Stagger related elements by 60-140ms.
- Keep the primary action available quickly.

Micro-interactions:

- Buttons: hover lift or color shift, pressed scale, loading state.
- Inputs: focus transition, validation color, success/error icon motion.
- Toggles and switches: thumb translation plus color transition.
- Drag/drop: lift on grab, highlight valid targets, animate settle.

State transitions:

- Modals and drawers: fade backdrop, transform panel, manage focus.
- Tabs and filters: animate active indicator and crossfade content.
- Expand/collapse: prefer grid, transform, or measured transitions that avoid jumpy layout.
- Loading: skeletons or progress indicators that reduce perceived wait.

Expressive moments:

- Hero sections: one strong reveal or continuous scene, not decorative clutter.
- Empty states: gentle movement that does not distract from the next action.
- Completion: small success flourish; avoid oversized celebration unless the domain warrants it.

State as story:

- Loading should communicate progress, not just waiting.
- Error motion should locate the problem without punishing the user.
- Success motion should confirm completion and return the user to flow.
- Disabled states should feel unavailable without feeling broken.
- Data changes should preserve object constancy when possible.

Scene-based or game-like motion:

- Define the camera or viewport relationship before animating objects.
- Keep controls and readable text stable even when the scene is lively.
- Use motion to communicate rules, physics, and consequences.
- Verify the first rendered frame is meaningful; avoid blank or confusing starts.

## Examples

Use examples as neutral starting points, then adapt to the product's existing design language.

Button feedback:

```css
.button {
  transition:
    transform 140ms var(--ease-out-quart),
    box-shadow 180ms var(--ease-out-quart),
    background-color 180ms var(--ease-out-quart);
}

.button:hover {
  transform: translateY(-1px);
}

.button:active {
  transform: translateY(0) scale(0.98);
}
```

Modal entrance:

```css
.modal-backdrop {
  opacity: 0;
  transition: opacity 180ms var(--ease-out-quart);
}

.modal-panel {
  opacity: 0;
  transform: translateY(12px) scale(0.98);
  transition:
    opacity 220ms var(--ease-out-quart),
    transform 260ms var(--ease-out-quart);
}

.modal[data-open="true"] .modal-backdrop,
.modal[data-open="true"] .modal-panel {
  opacity: 1;
}

.modal[data-open="true"] .modal-panel {
  transform: translateY(0) scale(1);
}
```

Loading handoff:

```css
.content-shell {
  transition: opacity 220ms var(--ease-out-quart);
}

.content-shell[data-loading="true"] {
  opacity: 0.62;
}

.content-shell[data-loading="false"] {
  opacity: 1;
}
```

These snippets are intentionally plain starting points.

## Accessibility

Always respect reduced motion:

```css
@media (prefers-reduced-motion: reduce) {
  *,
  *::before,
  *::after {
    animation-duration: 0.01ms !important;
    animation-iteration-count: 1 !important;
    scroll-behavior: auto !important;
    transition-duration: 0.01ms !important;
  }
}
```

Do not use animation as the only way to communicate state. Preserve focus states, labels, text, icons, and ARIA behavior as appropriate.

Avoid motion that flashes, shakes repeatedly, moves large backgrounds aggressively, or blocks interaction longer than necessary.

## Review Mode

When asked to review existing animation, prioritize actionable findings over compliments. Inspect the live behavior when possible, not only the source code.

Report in this order:

- Findings: bugs, jank, accessibility issues, timing problems, unclear cause/effect, layout shifts, overlap, or state confusion.
- Risk: what the issue does to usability, performance, accessibility, or product feel.
- Recommendation: the smallest change that would improve the motion.
- Verification: how to confirm the fix, such as viewport checks, reduced-motion checks, screenshot comparison, interaction testing, or build commands.

Use severity when helpful:

| Severity | Meaning |
| --- | --- |
| P0 | Breaks interaction, causes severe accessibility risk, or makes content unusable. |
| P1 | Noticeable usability, performance, or layout regression. |
| P2 | Quality issue that makes motion feel rough, confusing, or inconsistent. |
| P3 | Polish suggestion with low user impact. |

If no issues are found, say that clearly and list any unverified areas, such as mobile, reduced motion, or low-end device performance.

## Verification

Before claiming the animation work is done:

- Run the app and interact with the animated states.
- Check desktop and mobile viewports when layout could change.
- Check the first frame, peak motion frame, and final resting frame.
- Confirm reduced-motion behavior exists.
- Confirm text and controls do not overlap during animation.
- Confirm animations do not resize fixed UI unexpectedly.
- For canvas, WebGL, or Three.js, use a screenshot or pixel check to prove the scene renders.
- Run the relevant lint, typecheck, test, or build command when available.

When possible, inspect the work at normal speed and with slower playback or repeated interaction. Many animation problems only appear during the transition, not in the final frame.

## Common Mistakes

- Adding motion everywhere instead of coordinating one main moment.
- Choosing animation because a screen feels plain, without defining what it explains.
- Using long feedback animations that make the UI feel slow.
- Animating expensive layout properties without measuring.
- Forgetting reduced-motion users.
- Hiding loading, error, or disabled states behind decorative animation.
