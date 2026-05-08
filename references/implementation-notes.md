# AI Video Production Notes

Use this reference when turning animation craft into model-ready video work, image-to-video prompts, repair notes, or delivery checks.

## Model Handoff

Write video prompts as timed visual events:

- First frame: subject, place, scale, posture, camera distance, light source.
- Motion path: where the subject/camera starts, where it moves, and how quickly.
- Physical cause: what pushes, pulls, interrupts, attracts, blocks, or transforms the subject.
- Reaction: body, prop, environment, light, sound, or camera response.
- Ending state: what must be visible in the final frame and inherited by the next shot.

Avoid writing a still image with style words. A video model needs visible change.

## Prompt Timing

Useful timing patterns:

| Duration | Pattern |
| --- | --- |
| 5s | 0-1s setup, 1-3s action, 3-5s reaction/settle |
| 8s | 0-2s setup, 2-5s escalation, 5-8s turn/settle |
| 10s | 0-2s setup, 2-6s main motion, 6-8s impact, 8-10s reaction |
| 15s | 0-3s setup, 3-7s attempt, 7-11s complication/turn, 11-15s consequence |

Do not force every shot to use every beat. Use only the structure needed for readability.

## Camera Notes

Camera motion should explain the shot:

- Static camera: lets performance, composition, or transformation read clearly.
- Slow push-in: pressure, realization, intimacy, reveal.
- Pull-back: consequence, loneliness, scale, aftermath.
- Tracking: pursuit, travel, chase, inspection, procession.
- Pan/tilt: reveal relationship, follow gaze, disclose hidden object.
- Handheld drift: tension, fragility, subjective instability.

Name camera speed and relationship to subject. Avoid vague phrases like "dynamic camera" without a path.

## Continuity Checks

Before generating a multi-shot sequence, lock:

- Character identity: silhouette, face/hair, costume, prop, posture habit.
- Scene identity: fixed architecture, light source, weather, ground/surface marks.
- Prop state: ownership, location, damage, glow, liquid, dust, cloth, opening/closing state.
- Screen direction: who faces left/right, who enters/exits, where the camera axis sits.
- Body state: fatigue, wounds, wetness, dust, deformation, emotional residue.
- Ending inheritance: what the next shot must show in the first two seconds.

## Verification

Review the generated clip at least twice:

- Normal speed for audience readability.
- Paused on first frame, peak action, impact, and final frame.

Check:

- The shot has actual motion, not a drifting still.
- The main action is readable without the prompt.
- Character and scene identity did not drift.
- Camera motion does not hide the key action.
- Light direction, weather, and prop state remain consistent.
- The final frame can connect to the next shot.
- No unwanted text, subtitles, logos, UI screens, or watermarks appeared.

## Repair Language

Repair prompts should name the failure and the replacement behavior:

```text
Problem: the character face morphs during the turn.
Repair: keep the same oval face, high crown, black tied hair, and left cheek mole throughout; only the gaze moves from the door to the falling lantern.
```

```text
Problem: the shot feels like a still image.
Repair: add visible 0-8s progression: sleeve lifts in wind, lantern swings left to right, dust rises from floor cracks, camera slowly pushes from medium shot to close-up.
```
