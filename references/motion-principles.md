# Motion Principles

Use this reference when planning animation language, interaction hierarchy, staging, rhythm, and state storytelling.

## Motion Has A Job

Every animation should do at least one useful thing:

- Feedback: acknowledge that an input was received.
- Continuity: connect one state to the next.
- Guidance: draw attention to the next meaningful area.
- Explanation: reveal cause and effect.
- Expression: give the product an appropriate sense of character.

If the animation does not make the interface clearer, faster to understand, or more emotionally appropriate, simplify it.

## Hierarchy

Motion creates hierarchy faster than color or typography. Use it carefully:

- Primary objects move first.
- Supporting objects follow or stay still.
- Background motion should be slower, lower contrast, or absent.
- Utility controls should rarely travel far.
- Repeated items can stagger, but the stagger should communicate grouping or order.

When everything moves, nothing leads.

## Staging

Good UI staging makes the moving subject obvious:

- Start from a readable first frame.
- Keep the most important element visually isolated during the motion.
- Avoid moving text while the user is expected to read it.
- Preserve stable controls during lively scene animation.
- Let the final resting frame communicate completion without extra explanation.

For scene-like animation, think in beats:

1. Setup: show the current state clearly.
2. Change: move the subject or camera to express the transition.
3. Response: show affected objects reacting if needed.
4. Settle: return to a stable, usable interface.

Most product UI only needs setup, change, and settle.

## Rhythm

Rhythm comes from contrast:

- Short feedback can feel immediate.
- Longer entrance can feel intentional.
- Stagger can make dense content easier to parse.
- Stillness gives motion room to be noticed.
- Pauses can be useful when the user needs to understand a change.

Avoid making all durations similar. A page where every element moves for 300ms can feel mechanical.

## Object Constancy

When possible, preserve the user's sense that an object remains the same object across states:

- Move an item from old location to new location instead of fading it out and replacing it.
- Keep avatars, icons, cards, and selected items visually connected across transitions.
- Animate sorting, filtering, and reordering so the user can track what changed.
- Use fade-only transitions when object identity does not matter.

## State Storytelling

Loading:

- Communicate that work is happening.
- Prefer skeletons or progress when the shape or duration is known.
- Avoid indefinite motion that competes with reading.

Error:

- Locate the problem.
- Keep motion brief and respectful.
- Pair motion with text or icon state.

Success:

- Confirm completion.
- Return the user to flow quickly.
- Avoid large celebration unless completion is rare or emotionally meaningful.

Disabled:

- Communicate unavailability without making the UI feel broken.
- Avoid animated disabled controls that invite interaction.

Data updates:

- Preserve object constancy when changes are spatial.
- Highlight changed values briefly when the user needs to notice updates.

## Accessibility

Motion-sensitive users may experience discomfort from large movement, parallax, zoom, repeated loops, or aggressive shake. Always provide reduced-motion behavior. Reduced motion should preserve meaning, not simply remove state feedback.

Avoid flashing, rapid oscillation, repeated shake, and large moving backgrounds unless there is a clear domain reason and accessibility has been considered.
