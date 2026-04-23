# Implementation Notes

Use this reference when choosing animation technology or implementing motion details.

## Tool Selection

CSS transitions:

- Best for hover, focus, pressed states, opacity, color, transform, and simple component state.
- Low overhead and easy to maintain.
- Use custom properties for shared durations and easing.

CSS keyframes:

- Best for simple entrance, loop, shimmer, pulse, and decorative sequences.
- Keep loops subtle and avoid long-running layout or paint-heavy animation.

Web Animations API:

- Best for imperative control without a dependency.
- Useful when animation starts from measured runtime values.
- Good for canceling, reversing, or coordinating individual elements.

Framer Motion:

- Best in React projects that already use it or need shared layout transitions.
- Good for route transitions, layout changes, presence, and gestures.
- Avoid adding it for a single hover state.

GSAP:

- Best for timeline-heavy choreography, SVG sequences, scroll-linked scenes, and complex coordination.
- Useful when animation design has many beats.
- Keep product UI usable while timelines run.

Canvas and WebGL:

- Best for particles, simulations, games, data visuals, and full-bleed interactive scenes.
- Verify the first frame, resize behavior, device pixel ratio, and nonblank rendering.
- Keep DOM controls and readable text stable where possible.

Three.js:

- Best for true 3D scenes, cameras, lighting, spatial motion, and interactive objects.
- Verify camera framing across desktop and mobile.
- Check that assets load, canvas pixels are nonblank, and controls remain responsive.

## Performance

Prefer:

- `transform`
- `opacity`
- composited layers when appropriate
- lightweight shadows
- measured animation scopes

Avoid unless verified:

- animating `top`, `left`, `width`, `height`, `margin`, or `padding`
- animating large blur filters
- animating heavy shadows over large surfaces
- forcing layout inside animation frames
- starting many independent animations at once

Use `will-change` only for elements that are about to animate. Too much layer promotion can hurt memory and performance.

## Responsive Motion

Desktop and mobile may need different motion scale:

- Reduce travel distance on small screens.
- Keep important controls visible during transitions.
- Avoid parallax that makes mobile reading harder.
- Verify tap targets do not move away from the user during interaction.
- Check landscape and portrait if the scene is spatial.

## Reduced Motion

Reduced-motion mode should keep the state change understandable:

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

For important state changes, replace movement with instant state, opacity, color, icon, text, or layout change.

## Verification Techniques

Use the strongest available check for the risk:

- Manual interaction for feel, timing, and cause/effect.
- Browser devtools for layout shift, paint, and frame timing.
- Playwright screenshot for first/resting frame and layout stability.
- Pixel checks for canvas, WebGL, and Three.js nonblank rendering.
- Reduced-motion emulation for accessibility.
- Mobile viewport checks for overlap and tap target movement.
- Build, lint, typecheck, and test commands when available.
