# AI Video Storyboard Workflow

A portable Codex skill extracted from a larger approval-led AI-video workflow. It creates timing-aware written storyboards and, when requested and authorized, image-backed or pencil storyboard review assets.

The skill stops at storyboard approval. It does not authorize motion-video generation, voice generation, or final rendering.

## Install

Copy the `ai-video-storyboard-workflow` folder into your Codex skills directory, preserving `SKILL.md`, `references/`, and `assets/`.

## Use

Ask Codex to use `$ai-video-storyboard-workflow` with a brief, script, reference set, or existing storyboard that needs revision.

The default output is an authoritative written storyboard. For an image-backed visual review, explicitly choose that mode and approve any required image provider, cost, and bounded generation batch.

## Contents

- `SKILL.md`: routing, workflow, safeguards, and completion boundary
- `references/storyboard-spec.md`: per-shot schema plus timing, continuity, and approval audits
- `assets/STORYBOARD.template.md`: copyable storyboard document
- `assets/STORYBOARD_REVIEW.template.json`: review, provenance, cost, and approval manifest
