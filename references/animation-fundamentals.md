# Animation Fundamentals

Use this reference when the task needs basic animation craft before choosing a UI implementation.

## Timing

Timing is the duration of a motion and the distribution of events inside it.

- Short timing feels responsive, decisive, or lightweight.
- Long timing feels important, cinematic, or heavy.
- Feedback should be fast enough that the user knows the input was received.
- Entrances can take longer than exits because they introduce new information.
- Repeated loops should be slow or subtle enough to avoid attention fatigue.

When a motion feels wrong, first check whether the duration matches the importance of the event.

## Spacing

Spacing is how far an object moves between frames. It creates the feeling of acceleration, deceleration, and weight.

- Even spacing feels mechanical.
- Tight spacing at the end creates a soft settle.
- Tight spacing at the beginning creates a gentle start.
- Wider spacing in the middle creates speed.
- Sudden spacing changes create impact or surprise.

In CSS and UI tools, easing controls spacing. Choose easing based on how the object should feel, not only on what looks smooth.

## Ease In And Ease Out

Most natural motion does not start or stop at full speed.

- Ease-out is useful for UI feedback and entrances because the object arrives cleanly.
- Ease-in is useful for exits because the object leaves quickly after starting.
- Ease-in-out is useful for repositioning or two-way state changes.
- Linear motion is useful for progress, clocks, marquee movement, or mechanical systems.

Avoid using the same easing everywhere. Motion should reflect the role of the object and the type of state change.

## Anticipation

Anticipation prepares the user for a change.

- A pressed button can compress slightly before triggering a larger response.
- A drawer can begin with a small directional hint before opening.
- A draggable item can lift before it moves.
- A scene transition can shift focus before the main motion starts.

In UI, anticipation should usually be brief. If it delays action, it may feel like latency.

## Follow-Through And Settle

Motion often feels better when it does not stop abruptly.

- A panel can decelerate into place.
- A selected item can settle after being moved.
- A count or value update can briefly emphasize the changed number.
- A success state can finish with a small confirmation.

Settle should support clarity. Do not add extra movement after the user is ready to continue.

## Overlap

Overlapping action means related elements do not all move at exactly the same time.

- The main element can move first.
- Labels, shadows, icons, or supporting elements can follow shortly after.
- Groups can stagger by small intervals to reveal hierarchy.

Use overlap to make relationships readable. Avoid stagger for every list item if the order does not matter.

## Arcs

Natural motion often follows arcs rather than perfectly straight lines.

- Small arcs can make icons, cursors, particles, or scene objects feel less robotic.
- Straight movement can feel precise, technical, or mechanical.
- UI layout transitions usually need restrained arcs so elements still feel aligned.

Choose arcs only when they improve meaning or feel. Many product surfaces should stay geometrically calm.

## Squash And Stretch

Squash and stretch communicates softness, elasticity, and impact.

- Use tiny scale changes for pressed states.
- Use it more freely in games, playful empty states, or expressive illustrations.
- Avoid large squash/stretch on serious product controls.
- Never distort readable text.

In UI, scale is a seasoning, not the meal.

## Silhouette

The user should understand the moving object even during motion.

- Keep important shapes recognizable.
- Avoid overlapping text and controls during transitions.
- Make the first frame and final frame readable.
- For canvas and 3D scenes, check the object against the background at peak motion.

If the silhouette becomes unclear, reduce motion, simplify the path, or quiet the background.

## Weight

Perceived weight comes from distance, speed, easing, scale, shadow, and reaction.

- Heavy objects usually start slower and settle more deliberately.
- Light objects can respond quickly and travel less.
- Large surfaces need calmer motion than small icons.
- Shadows and depth changes should agree with the movement.

Do not make every element feel equally heavy. Motion hierarchy helps the interface feel organized.

## Camera And Viewport

For scenes, games, canvas, WebGL, and Three.js, the camera is part of the animation.

- Decide whether the object moves, the camera moves, or both.
- Keep UI controls and text stable while the scene moves.
- Check the first rendered frame before assets finish loading.
- Verify framing on mobile and desktop.

Camera motion is powerful. Use it to clarify space, not to show off.
