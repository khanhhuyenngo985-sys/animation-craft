---
name: animation-craft
description: Use when creating, refining, or reviewing animation videos, animated shorts, storyboards, animatics, AI-video shots, character performance, scene timing, camera motion, action beats, continuity, editing rhythm, sound cues, or image-to-video prompt plans for Seedance/即梦/可灵/海螺 style workflows. Do not use this as a frontend/UI motion skill unless the user explicitly asks for interface animation.
---

# Animation Craft

## Core Positioning

This skill is for making animation videos. It is not a frontend animation or UI micro-interaction skill.

Use it to turn an idea, scene, character, reference, or rough prompt into a watchable animated sequence with clear story beats, readable staging, stable identity, useful camera movement, and video-model-ready shot instructions.

## Start Here

Before producing assets or prompts, identify:

- Format: animated short, 5-15s AI-video shot, multi-shot sequence, animatic, storyboard, action segment, ad film, MV beat, or style test.
- Audience effect: joke, emotion, awe, clarity, product proof, character charm, suspense, or action impact.
- Main subject: character, creature, object, environment, product, vehicle, or abstract force.
- Change: what is visibly different by the end of the shot or sequence.
- Production target: storyboard, shot list, animatic timing, Seedance/即梦/可灵/海螺 prompt, review notes, or repair plan.

If the user asks for a quick prompt, still define the shot's beginning, motion, and ending before adding style words.

## Video Brief

For substantial work, produce this compact brief first:

| Field | Answer |
| --- | --- |
| Premise / task |  |
| Format + duration |  |
| Main subject |  |
| Visual change |  |
| Emotional beat |  |
| Camera logic |  |
| Continuity anchors |  |
| Sound / rhythm cue |  |
| Model target | Seedance / 即梦 / 可灵 / 海螺 / other |
| Output needed | beat sheet / shot list / prompt / review / repair |

## Runtime Flow

1. Lock the story or motion job.
   - One shot should establish, reveal, pressure, turn, release, or land a final beat.
   - Remove decorative movement that does not change attention, emotion, information, or consequence.

2. Stage the first readable frame.
   - The viewer should immediately know subject, location, scale, pressure, and visual direction.
   - Keep one main action per shot unless controlled chaos is the point.

3. Design movement as cause and effect.
   - Want becomes reach, gaze, lean, travel direction, grip, or camera pursuit.
   - Obstacle becomes distance, threshold, surface, opposing force, prop failure, crowd, weather, or timing pressure.
   - Consequence becomes residue, deformation, prop state, body state, lighting change, silence, or next-shot inheritance.

4. Plan timing.
   - Use setup, anticipation, action, impact, reaction, and settle.
   - For AI video, timebox changes with visible 0-2s / 2-5s / 5-8s / 8-15s beats when useful.
   - Let big turns breathe; do not fill every second with new information.

5. Protect continuity.
   - Lock character identity, scene identity, prop ownership, screen direction, light source, weather, damage, and ending state.
   - For multi-segment work, state what the next segment must inherit in its first two seconds.

6. Handoff to production.
   - For storyboard: output panels with duration, camera, action, and transition.
   - For AI video: output prompt-ready shot blocks with timing, camera, subject motion, environment reaction, audio cue, and forbidden drift.
   - For review: lead with story/staging/timing/continuity findings before polish.

## Knowledge Base

Load optional references only when needed:

| File | Read when |
| --- | --- |
| `references/animated-shorts.md` | Planning animated shorts, beat sheets, shot lists, storyboards, animatics, character action |
| `references/visual-storytelling.md` | Making a beat readable through pose, props, setting, silence, and consequence |
| `references/animation-fundamentals.md` | Timing, spacing, anticipation, follow-through, arcs, squash/stretch, silhouette |
| `references/motion-principles.md` | Video motion language, staging, rhythm, camera/object hierarchy, state change |
| `references/motion-rules.md` | Practical rules for readable shot motion, continuity, loops, action, and camera movement |
| `references/implementation-notes.md` | AI-video production notes, model handoff, prompt timing, review, and verification |
| `references/review-rubric.md` | Reviewing generated animation videos or animatics with severity and fixes |
| `examples/storyboard-template.md` | Storyboard panel planning |
| `examples/ai-video-shot-template.md` | Seedance/即梦/可灵 style timed shot prompt |
| `examples/continuity-ledger.md` | Multi-shot continuity ledger |

## Output Patterns

### Shot Prompt Block

```text
SHOT [number] / [duration] / [aspect]
Purpose:
Mounted references:
First frame:
0-2s:
2-5s:
5-8s:
8-15s:
Camera:
Character / object motion:
Scene reaction:
Audio:
Continuity inheritance:
Forbidden drift:
```

### Review Order

When reviewing an animation video, diagnose in this order:

1. Story clarity: can the viewer explain what changed?
2. Staging: is the main action readable in the first frame and peak frame?
3. Timing: do anticipation, action, impact, reaction, and settle have enough space?
4. Performance: does the body/face/prop motion reveal intention?
5. Continuity: do identity, scene state, prop state, screen direction, and light track?
6. Production polish: camera smoothness, flicker, morphing, texture, sound, edit point.

Do not polish style before story, staging, timing, and continuity work.

## AI Video Guardrails

- Do not describe only a beautiful still image; describe visible change over time.
- Do not rely on abstract emotion words. Convert emotion into posture, gaze, breath, hesitation, contact, residue, or silence.
- Do not overpack 15 seconds. Give each beat a physical action and a readable ending state.
- Do not let character identity drift while the state changes.
- Do not invent UI, subtitles, text, logos, app screens, or webpage behavior unless the project explicitly requires them.

## When To Hand Off

- Character identity, bone structure, costume, or drift → `character-design`
- Scene space, light, environment continuity, or scene drift → `scene-design`
- Final model-specific prompt packet → `prompt-framework`
- Shot-by-shot reference study → `shot-study`
- Sound design or music timing → `sound-design-to-prompt` / `score-editing-to-prompt`
- Larger local project routing or creative team workflow → `animation-studio`
