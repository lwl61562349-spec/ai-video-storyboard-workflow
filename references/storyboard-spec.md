# Storyboard Specification

Use this reference to write or audit the authoritative storyboard document.

## Document header

Record:

- project title and storyboard version
- target duration and aspect ratio
- approved script or brief version
- canonical character, product, environment, and style references
- selected mode: written, image-backed, or pencil
- image-generation approval and cost state, when applicable
- current review status and unresolved decisions

Add a compact shot index with shot ID, title, time range, duration, story purpose, and visual-asset status.

## Per-shot contract

Use one section per shot, in playback order.

1. **Identity**: shot ID, title, master-timeline range, and duration.
2. **Story purpose**: what visibly changes and why the shot exists. Optionally classify the beat as setup, reveal, reversal, callback, suspense, reaction, tenderness, chase, climax, or resolution.
3. **Bound references**: exact character, product, environment, wardrobe, prop, or brand sources used by this shot.
4. **Opening state**: first-frame composition, shot size, angle, subject positions, gaze, expression, product/prop state, lighting, and inherited continuity.
5. **Spatial anchors**:
   - fixed landmarks and screen-relative positions
   - each subject's screen position, depth, facing direction, and initial pose
   - exited-character or off-screen status when continuity needs it
   - geography or screen-direction rule that must not flip accidentally
6. **Timed visual beats**: contiguous, non-overlapping action ranges that cover the full shot once. Every range specifies body/hand action, expression and gaze path, prop/product state, camera behavior, and the state handed to the next range.
7. **Audio timing**: dialogue, voiceover, SFX, music, breath, and intentional silence with time windows. Keep audio nested under the visual timeline. Mark visible speaker mouth behavior only when lip-sync is intended.
8. **Camera plan**: focal framing, physical camera movement, handheld baseline when used, motivated move, and endpoint settle. Treat optical zoom, subject lean, and camera travel as separate motion owners.
9. **Final state**: exact last-frame composition, pose, gaze, expression, product/prop state, camera state, and measurable hold.
10. **Continuity handoff**: what the next shot must inherit or the explicit cut that permits a change.
11. **Deterministic post**: exact typography, UI, captions, CTA, disclosure, logo, or product copy to create outside the generative image/video layer.
12. **Visual panel**: asset path or ID, provenance label, version, and approval status when the mode is image-backed or pencil.

## Timing audit

- Shot ranges cover `0.0s` through the declared duration exactly once.
- Sub-second beats are allowed when action order or a critical pose requires them.
- Narration and dialogue timing does not shorten the visual runtime; visual acting may begin before or continue after speech.
- Reserve intentional breathing room, reaction time, transitions, and a post-line visual hold where the ending needs one.
- The sum of shot durations matches the target runtime or the document clearly records an allowed variance.

## Continuity audit

Read only each shot's final state followed by the next shot's opening state. Check:

- character identity, age/state, wardrobe, and side of frame
- eye-line and travel direction
- hand, prop, product, packaging, and label state
- environment geography and fixed landmarks
- camera height, angle, and screen-direction change
- lighting and time-of-day change
- emotional and causal progression

Any discontinuity must be a named transition such as a hard cut, time jump, location change, match cut, or deliberate axis break.

## Visual modes

### Image-backed board

Every shot card contains an actual generated still or a clearly labeled approved reference/composite. Start with one risk-bearing test frame before a batch. Preserve rejected versions and record prompts, source references, provider settings, cost, QA, and approval status.

### Pencil board

Use one sheet per shot. Create panels for meaningful timed states rather than decorative coverage. Each panel should show timecode, pose/expression, camera direction, audio/anchor cue, and continuity handoff. Sketches are human-review aids; the written storyboard remains authoritative.

If image generation repeatedly fails to preserve identity, layout, or legibility, stop after bounded targeted revisions. Offer a simpler block-value sketch, a user-supplied reference, a split shot, or the written storyboard alone. Do not multiply retries silently.

## Approval audit

Before marking the board approved, confirm:

- the user reviewed the exact version now designated canonical
- all shot-specific comments are resolved or explicitly deferred
- any generated frame cost is recorded
- all visual assets have provenance and status labels
- unresolved production risks and the next approval gate are visible
