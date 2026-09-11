---
name: ai-video-storyboard-workflow
description: Create review-ready, timing-aware AI-video storyboards from an approved brief, script, and locked references, using an authoritative written board plus optional image-backed or pencil visualization. Use when the requested deliverable is a storyboard or when a video project needs storyboard approval before motion generation; stop before producing video clips.
---

# AI Video Storyboard Workflow

Turn an approved concept or script into a production-ready storyboard whose timing, composition, performance, camera, audio ownership, and continuity can be reviewed before video generation.

This skill owns storyboard creation and revision only. It does not treat a storyboard as authorization to generate motion clips, voices, or a final render.

## Choose the deliverable

Use one of these modes and label it clearly:

- **Written storyboard**: the authoritative shot-by-shot production document. No image generation is required.
- **Image-backed storyboard**: the written storyboard plus one truthful visual frame for every shot. Use approved references where they accurately represent the shot; otherwise generate stills only after the user approves the image method, provider, cost, and bounded batch.
- **Pencil storyboard**: the written storyboard plus multi-panel sketch sheets for human review. Sketches are supplemental and never replace the written timing and continuity specification.

If the user asks to review how the film will actually look, a text-only board is not a visual storyboard. Do not describe boxes, placeholders, or prose-only cards as image-backed or visually review-ready.

## Inputs and locks

Before storyboarding, resolve or explicitly mark as pending:

- target duration, aspect ratio, audience, language, and delivery context
- approved concept/script and exact dialogue or voiceover
- character, product, environment, brand, and style references
- physical orientation, wardrobe, props, geography, and on-screen text that must remain exact
- storyboard mode and whether any still generation is authorized

Freeze the canonical sources. Do not silently mix old revisions, rejected assets, or conflicting references.

## Workflow

1. Build a shot spine. Give every shot a stable ID such as `S01`, a duration, a narrative change, an opening state, and an ending handoff.
2. Draft the authoritative written storyboard using [the storyboard specification](references/storyboard-spec.md) and [the template](assets/STORYBOARD.template.md).
3. Audit timing and continuity. Visual action ranges must cover each shot from first frame to last frame without gaps or overlaps. Dialogue, voiceover, SFX, and silence are nested audio timing, not competing visual ranges.
4. Unless the user requests a locked-off shot, use restrained motivated camera movement: controlled handheld breathing drift plus one subtle push, pull, correction, recoil, pan, tilt, or subject-follow. Avoid jitter, random zooms, gimbal float, and horizon wobble. Reserve a clean 0.3–0.5-second endpoint settle when the shot permits it.
5. For recurring people or creatures, lock character identity before visualizing the full board. For product-sensitive work, lock product geometry, visible side, label orientation, and use state before generating frames.
6. If the selected mode uses generated images, create one representative frame first. Choose the frame that tests the largest identity, composition, product, lighting, or spatial risk. Show the result and actual cost, then obtain approval before the remaining still batch.
7. Create or assemble one truthful visual asset per shot for an image-backed board. Version replacements instead of overwriting rejected frames. Record provenance and status in [the review manifest](assets/STORYBOARD_REVIEW.template.json).
8. Present shots in order and collect shot-specific feedback. Revise only affected text, assets, or compositions, then re-run timing and continuity checks.
9. Obtain explicit approval of the exact storyboard version. Handoff the approved written board, visual assets when used, review manifest, unresolved risks, and the next production gate.

## Required quality checks

- Every shot has a visible story purpose and changes the situation, information, emotion, or product state.
- Each shot defines composition, spatial anchors, action, performance, camera behavior, audio ownership, exact final state, and continuity handoff.
- Character identity, product truth, screen direction, eye-lines, prop state, lighting, and geography remain consistent or the change is explicitly motivated.
- Each spoken line has a speaker and time window; off-screen narration does not accidentally imply visible lip-sync.
- Important silent acting, reaction, transition, and end-hold time is intentional and measurable.
- Exact UI, clock digits, CTA, captions, legal copy, and fragile product text are marked for deterministic post unless the user accepts generated text.
- Every visual panel is labeled as generated, approved reference, temporary composite, or sketch. Do not imply that planning text is generated media.
- No motion-video, voice, or render job is submitted under storyboard approval alone.

## Handoff boundary

The completed deliverable is an approved storyboard package, not a finished video. Stop after storyboard approval unless the user separately asks to continue into motion production.
