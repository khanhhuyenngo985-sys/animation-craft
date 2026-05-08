# Animation Video Review Rubric

Use this reference when reviewing generated animation videos, animatics, storyboards, or AI-video prompt results.

## Review Output

Lead with findings. For each issue, include:

- Severity: P0, P1, P2, or P3.
- Finding: what is wrong on screen.
- Risk: why it hurts the video.
- Recommendation: the smallest useful repair.
- Verification: how to confirm the fix.

If there are no findings, say so and list unverified areas.

## Severity

| Severity | Meaning |
| --- | --- |
| P0 | The shot is unusable: wrong subject, no readable action, severe identity drift, broken continuity, or unsafe/unwanted content. |
| P1 | Major story, staging, timing, or continuity failure that blocks delivery. |
| P2 | Noticeable quality issue: rough timing, weak performance, flicker, morphing, unclear camera, weak ending state. |
| P3 | Polish suggestion with low story risk. |

## What To Inspect

Story clarity:

- Can a viewer explain what changed without reading the prompt?
- Is the first frame readable?
- Does the final frame land a new state, reaction, or question?

Staging:

- Is there one clear main action?
- Does silhouette, contrast, camera distance, and light support readability?
- Are props and obstacles positioned so cause and effect can be seen?

Timing:

- Is there enough setup before action?
- Does impact have a clear contact or transformation frame?
- Does the reaction or settle happen long enough to read?
- Are cuts or beat changes too fast for the information density?

Performance:

- Does posture, gaze, breath, or hand action reveal intention?
- Does the face support the body instead of replacing the body acting?
- Are secondary motions helping weight and emotion?

Continuity:

- Does character identity remain stable?
- Do scene layout, light source, weather, and screen direction track?
- Do prop ownership, damage, residue, and body state carry across shots?

Production artifacts:

- Flicker, melting, morphing, warped hands, smeared faces, texture popping.
- Camera hiding the key action.
- Unwanted text, logos, subtitles, app screens, UI overlays, or watermarks.
- Shot starts blank or ends without an inheritable state.

## Common Findings

- The clip looks like a still image with camera drift; add timed subject/environment change.
- The main action happens before the viewer understands the setup; add a readable first frame.
- The face morphs during camera movement; lock bone/face/hair anchors and simplify motion.
- The scene resets between shots; carry dust, broken prop, door state, light direction, and body position.
- The camera is energetic but not informative; choose static, push, track, or reveal based on the beat.
- The sound cue is missing from the rhythm; add silence, impact, tail, or ambient bed timing.

## Verification Checklist

- Watch at normal speed.
- Pause first frame, peak action, impact frame, and final frame.
- Compare final frame to the next shot's first frame.
- Check identity anchors against character reference.
- Check scene anchors against scene reference.
- Check for unwanted text or UI artifacts.
- Confirm the repair prompt names a specific visible replacement, not just "make it better".
