---
name: etsy-product-photo-15
description: Fixed Chinese Etsy 15-image product-photo campaign prompt. Use when the user provides product images and asks in Chinese to generate 15 Etsy listing photos with close/far views, lifestyle scenes, product display, detail shots, dimension/size effect images, human-use images, varied angles/scenes, or when the user prompt begins "我是etsy卖家，根据我提供的产品图". This skill wraps product-photo-campaign-openrouter and makes the user's fixed Etsy prompt mandatory.
---

# Etsy Product Photo 15

## Overview

Use this skill as the user's fixed Etsy product-photo campaign entrypoint. It turns supplied product reference images into a 15-image Etsy listing set by delegating the campaign planning and image generation rules to `product-photo-campaign-openrouter`.

Always load and follow the sibling dependency skill:

`../product-photo-campaign-openrouter/SKILL.md`

In a standard Codex installation this resolves under
`$CODEX_HOME/skills/product-photo-campaign-openrouter/SKILL.md` or
`~/.codex/skills/product-photo-campaign-openrouter/SKILL.md`. If the dependency
is missing, stop and ask the user to install both skill folders from the same
repository.

## Mandatory Prompt

Every final campaign plan must include this user instruction verbatim:

```text
我是etsy卖家，根据我提供的产品图，帮我生成15张符合etsy顾客喜欢的产品图，镜头需要有近有远，有大有小，整体要有生活气息，图片需包含产品展示，产品细节展示，产品尺寸效果图，尺寸图不的随意修改和线条叠加错乱，人物使用效果展示，生成时注意产品摆放角度和场景图需多样化，不的集中在某一角度和某一场景展示，你是资深的
etsy产品设计师，发挥你的设计才能开始设计吧
```

Do not paraphrase, translate, shorten, or replace this prompt. Add product-lock, category-safety, dimension-safety, and reference-fidelity constraints around it as needed.

## Workflow

1. Require at least one readable product reference image. If the user provides disk paths, inspect them with `view_image` before planning.
2. Load `product-photo-campaign-openrouter` and use its full planning workflow: product intelligence, image set strategy, coverage matrix, shot briefs, one prompt per shot, generation, and validation.
3. Generate exactly 15 final images unless the user explicitly asks for a different count.
4. Include these buyer-facing roles across the set:
   - strong Etsy cover / hero image
   - clean product display image
   - alternate angles and back/side views where useful
   - product detail and material/craftsmanship shots
   - lifestyle room scenes with near/far and large/small framing
   - scale or size-effect image
   - dimension infographic when exact dimensions are supplied
   - human-use or anonymous partial-body interaction when category-safe
   - premium closing lifestyle image
5. Keep product truth locked to the supplied references: structure, proportions, material, color, grain, hardware, seams, labels, included items, and buyer-critical details.
6. Do not concentrate the set in one angle or one scene. Vary camera distance, angle, product state, background, placement, props, and buyer question.

## Dimension Image Rules

Treat dimension images as a special deterministic step, not an ordinary generated lifestyle image.

- If exact dimensions are supplied, lock every number and unit before image work.
- Do not let image generation invent, rewrite, or draw exact dimension text.
- Prefer this workflow:
  1. Generate or select a clean text-free product/base composition.
  2. Add measurement text, lines, dots, and weight icons with deterministic graphics such as SVG, HTML/CSS, Pillow, or another exact overlay method.
  3. Verify every visible number and line before final delivery.
- If exact dimensions are not supplied, do not invent them. Make a dimension-ready inventory image or a scale-effect lifestyle image using real objects such as a bed, lamp, phone, book, hand, or chair.
- Do not copy the background, pose, or layout of a supplied dimensions reference unless the user explicitly asks for a replica. Use the reference for data and diagram logic only.
- Reject or redo any dimension output with changed numbers, extra numbers, misspelled units, tangled lines, overlapping labels, random arrows, or hard-to-read text.

## Output

Save durable outputs in the user-requested directory. If none is supplied, use
`E:\Codex_Output` on Windows when that drive exists; otherwise use an `outputs`
folder in the current workspace:

```text
<out-dir>/
  plan.codex-direct.json
  prompts/
    shot-01.txt
    ...
    shot-15.txt
  shot-01.png
  ...
  shot-15.png
  fidelity-audit.json
```

Report the output folder, reference images used, any rejected/regenerated shots, and whether the dimension image used locked numeric data or only scale-effect cues.
