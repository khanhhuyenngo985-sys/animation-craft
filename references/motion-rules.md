# Motion Rules Of Thumb

Use this reference when the task needs practical UI animation judgment.

## Rule 1: Feedback Comes First

Every direct user action should acknowledge input quickly.

- Clicks, taps, drags, saves, deletes, and toggles should respond before or during async work.
- Loading that appears only after a delay can make the product feel broken.
- Use visual feedback even when the final result takes time.

Good motion starts by making the interface feel attentive.

## Rule 2: One Moment Leads

Each screen or interaction should have a clear motion leader.

- Let one element carry the main change.
- Keep nearby elements quieter.
- Use stagger to reveal hierarchy, not to decorate.
- Avoid simultaneous animations with equal contrast.

If the user cannot tell what changed, there is too much motion or the wrong thing is moving.

## Rule 3: Stillness Is Part Of Motion

Stillness makes motion legible.

- Keep reading areas calm.
- Keep controls stable while the user is deciding.
- Use ambient motion only where it does not compete with task flow.
- Let motion finish before asking the user to interpret a new state.

A calm interface can make a small animation feel more intentional.

## Rule 4: Direction Should Mean Something

Motion direction should support the mental model.

- Down often suggests reveal, expansion, or incoming detail.
- Up can suggest dismissal, elevation, or return.
- Left/right often maps to previous/next, before/after, or navigation.
- Toward the trigger suggests connection.
- Away from the trigger suggests dismissal or completion.

Do not reverse direction casually between related states.

## Rule 5: Preserve Object Identity

When users care about an item, help them track it.

- Move the object instead of replacing it when location changes.
- Keep selected items visually connected across navigation or filtering.
- Animate list reorder when order matters.
- Use fade-only transitions for content where identity is not important.

Object constancy reduces cognitive load.

## Rule 6: Match Motion Scale To Importance

The bigger the motion, the more important it feels.

- Buttons and inputs usually need small movement.
- Modals, drawers, and pages can use medium movement.
- Hero scenes and games can use larger movement.
- Destructive, error, or system-critical states should avoid playful excess.

If a small action gets a large animation, the interface can feel theatrical instead of useful.

## Rule 7: Exit Faster Than Enter

Users usually need more time to understand what appears than what disappears.

- Entrances can introduce information.
- Exits should get out of the way.
- Modal, drawer, and tooltip exits often feel better at about 70-80% of the enter duration.

Do not let dismissal animations slow the user down.

## Rule 8: Motion Should Not Hide State

Animation must not be the only state carrier.

- Pair error motion with text, color, icon, or focus.
- Pair success motion with persistent confirmation when needed.
- Preserve keyboard and screen reader behavior.
- Reduced-motion users should still understand what happened.

Motion can emphasize state, but it should not replace state.

## Rule 9: Loops Need A Reason

Looping animation is expensive in attention.

- Use loops for loading, waiting, living scenes, or clearly ambient contexts.
- Keep loops slow, subtle, or spatially separated from reading.
- Pause or reduce loops when they are no longer useful.
- Avoid multiple unrelated loops in the same viewport.

If the user is trying to read or decide, the loop should be quiet.

## Rule 10: Verify The Peak Frame

Many animation bugs appear only mid-transition.

- Check first frame, peak motion frame, and final frame.
- Look for text overlap, clipped surfaces, moving tap targets, and unexpected layout shifts.
- Test reduced motion and mobile viewports.
- For canvas and WebGL, confirm the scene is nonblank and correctly framed.

The final screenshot is not enough.

## Rule 11: Use Motion To Explain Relationship

Motion can show how things belong together.

- A menu should emerge from or near its trigger.
- A selected card should preserve continuity when opening details.
- A toast should appear from a consistent region.
- A filter change should make changed results trackable.

When spatial relationships are unclear, motion can act like a visual sentence.

## Rule 12: Keep The Interface Playable

Animation should not block interaction unless the blocked period is intentional and brief.

- Avoid locking the whole UI for decorative sequences.
- Allow repeated actions to cancel, reverse, or finish cleanly.
- Prevent animation queues from stacking up after rapid clicks.
- Make loading and disabled states explicit.

The user should feel in control of the interface.
