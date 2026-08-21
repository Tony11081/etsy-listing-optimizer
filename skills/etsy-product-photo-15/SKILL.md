---
name: etsy-product-photo-15
description: Create a reference-locked, conversion-oriented 15-image Etsy listing photo set from supplied product images. Use when a Chinese-speaking Etsy seller asks for 15 product photos, hero and detail images, lifestyle and scale views, personalization or variation images, dimension graphics, packaging/process images, or a listing-photo CRO audit. This skill keeps the user's fixed Chinese prompt mandatory while applying current Etsy image, mockup, mobile, and listing-video safeguards.
---

# Etsy Product Photo 15

## Overview

Use this skill as the user's fixed Etsy 15-image campaign entrypoint. The goal is not to create 15 attractive background swaps. The set must help the right buyer identify the product, understand exactly what is sold, judge size and material, choose options, and buy with fewer expectation gaps.

Knowledge baseline: `Etsy 运营知识库 06｜Listing 页面、主图、图片组、视频与转化率 SOP`, V1.0, verified 2026-08-19.

Always load and follow the sibling skill:

`../product-photo-campaign-openrouter/SKILL.md`

When rules overlap, this skill supplies the Etsy-specific sequence, publishing-readiness, and conversion safeguards. The sibling skill supplies the full campaign planning, prompt generation, image generation, and fidelity-audit workflow.

## Mandatory Prompt

Every final campaign plan must include this user instruction verbatim:

```text
我是etsy卖家，根据我提供的产品图，帮我生成15张符合etsy顾客喜欢的产品图，镜头需要有近有远，有大有小，整体要有生活气息，图片需包含产品展示，产品细节展示，产品尺寸效果图，尺寸图不的随意修改和线条叠加错乱，人物使用效果展示，生成时注意产品摆放角度和场景图需多样化，不的集中在某一角度和某一场景展示，你是资深的
etsy产品设计师，发挥你的设计才能开始设计吧
```

Do not paraphrase, translate, shorten, or replace this prompt. Add the product-truth, category-safety, dimension-safety, Etsy compliance, and reference-fidelity constraints in this skill around it.

## Current Etsy Capacity and Scope

- The knowledge baseline says a current Listing can contain up to 20 images and 2 videos. The older limits of 10 images and 1 video are not the operating baseline.
- This skill still plans exactly 15 image roles because that is the user's requested campaign format; 15 is not Etsy's platform maximum and is not a ranking guarantee.
- Every image must answer a distinct buyer question or provide distinct proof. Do not pad the set with repeated scenes, angles, or props merely to reach 15.
- Plan all 15 roles, but place only independently audited `pass` images in the final set. If truth, source evidence, or generation quality blocks a role, report the run as `PARTIAL` or `BLOCKED`; never fill the gap with a misleading or duplicate image.
- Do not upload, reorder, or edit a live Etsy Listing unless the user separately gives explicit authorization.
- Do not promise that photos or videos will produce a fixed conversion increase, ranking gain, favorite rate, or order volume.

## Input and Product-Truth Gate

Before planning, require at least one readable reference image and inspect every reference needed to establish product truth.

Record confirmed facts separately from unknowns:

- product identity, category, structure, proportions, component count, and included items;
- material, color, finish, texture, construction, hardware, seams, labels, engraving, artwork, and buyer-critical details;
- exact dimensions and units, if supplied;
- visible Variations and their exact customer-facing names;
- personalization fields, character limits, capitalization/date rules, and a completed sample, if applicable;
- packaging and accessories that are actually included;
- items shown for styling or scale that are not included;
- whether each source is an own real-product photo, authorized customer photo, permitted stock mockup, render, or AI image;
- Production Partner and POD context when it changes which mockups are acceptable;
- the pictured/default Listing version and its displayed price, when supplied.

Preserve `Unknown` as unknown. Do not invent dimensions, materials, processes, inclusions, personalization examples, packaging, prices, shipping promises, or Production Partner facts.

## Publishing-Readiness and Mockup Gate

Classify the campaign before generation:

- `real_product_supported`: real completed-product references exist and generated scenes are supplemental;
- `permitted_pod_mockup_supported`: an original seller design is shown on an accurate base-product mockup, with the base product and print placement verified;
- `concept_only`: only renders, incomplete prototypes, blank personalized products, or unverifiable sources exist;
- `prohibited_or_unlicensed`: competitor imagery, unauthorized buyer/review photos, or a materially inaccurate mockup is involved.

Apply these rules:

- Default to the seller's own real completed-product photos as the strongest proof.
- AI may supplement a real product by changing or creating a scene only when product size, proportions, material, color, structure, components, and included items remain accurate.
- Do not make every Listing image a fictional AI scene with no real completed-product evidence.
- A unique physical product made by a Production Partner requires real completed-product evidence; a 3D render alone is not publish-ready.
- An original seller design on a standard POD base product may use an accurate stock mockup, but it must match the actual base item, color, print size, placement, and material. Recommend a real sample before treating the Listing as fully verified.
- For personalized products, the hero must show a completed personalized example similar to what the buyer will receive. A blank product, `Your Text Here`, `Your Name`, a dotted placeholder, or an option chart cannot be the hero.
- A previously completed personalized sample may be used when authorized, but the plan must identify it as an example rather than the buyer's exact final personalization.
- Never use a customer/review image without permission or a competitor's product photo.
- If the campaign is `concept_only`, assets may be delivered as concepts or drafts, but set `publish_readiness=BLOCKED` and clearly state the missing real-product evidence.
- If the campaign is `prohibited_or_unlicensed`, stop that route and do not generate or publish derivative assets from the source.

## Etsy 15-Image Buyer-Journey Template

Use this as a flexible role map, not a rigid one-size-fits-all composition list. Substitute category-native proof when a role is not applicable, but preserve the buyer journey and avoid duplicates.

1. `hero`: completed product, immediately recognizable, truthful, and sized for the search thumbnail.
2. `what_you_receive`: full product or set inventory, with included-item accuracy.
3. `size_and_scale`: locked numeric dimensions when supplied and/or a truthful real-world scale view.
4. `variations`: visible color, material, finish, shape, font, or style choices when applicable.
5. `material_and_craft`: texture, finish, edge, stitch, hardware, print, engraving, or construction proof.
6. `personalization_or_unique_value`: finished personalization or the strongest category-specific differentiator.
7. `use_or_lifestyle`: natural use context that proves use, fit, atmosphere, or buyer outcome.
8. `back_inside_or_structure`: the important area the hero cannot show.
9. `packaging_and_gifting`: actual packaging and gift readiness only when verified.
10. `process_or_provenance`: real making, finishing, personalization, or vintage evidence only when supported.
11. `installation_care_or_use`: how to install, handle, wear, clean, or use the item.
12. `limits_and_exclusions`: non-included props, color/size caveats, compatibility, or other decision-critical limits.
13. `alternate_angle_or_state`: a genuinely new angle, configuration, opening, movement, or component relationship.
14. `category_specific_trust`: fit, capacity, clasp, base, label, flaw, thickness, wash result, delivery condition, or other category-native proof.
15. `premium_closing_context`: an aspirational but truthful closing image that reinforces ownership, gifting, or use without changing the product.

Put the most important purchase answers early. The first five images should normally establish product identity, what is included, size/scale, visible choices, and quality. Do not hide exclusions or major limitations at the end.

## Category Adaptation Gate

Before assigning the 15 roles, read [references/category-adaptation.md](references/category-adaptation.md) and add a `category_adapter` object to the campaign plan with:

- `product_form`: how the item physically or digitally exists, such as wearable, handheld, freestanding, wall-mounted, furniture-scale, consumable, kit, digital, or one-of-a-kind;
- `primary_decision_modes`: the buyer decisions that matter most, such as appearance, fit, scale, compatibility, function, installation, condition, personalization, or file contents;
- `proof_priorities`: three to six product-specific questions the image set must answer;
- `category_native_states`: the truthful positions, configurations, actions, or use states worth showing;
- `safe_contexts` and `forbidden_contexts`: settings that support or misrepresent natural use, buyer intent, or price positioning;
- `scale_proof_method`: locked dimensions, a category-native scale cue, a worn/room view, or `not_applicable`;
- `human_presence_mode`: none, hand, POV, worn, partial body, or another justified mode tied to a buyer question;
- `scene_capacity`: `experience_led`, `balanced`, or `proof_led`, based on how much real context helps the buyer understand or desire this product;
- `role_substitutions`: every template role that lacks evidence or does not apply, paired with a supported replacement role;
- `style_source`: verified product design, target buyer, natural use, and price positioning—not the palette or props of a previous campaign.

Apply these gates:

- Do not inherit a previous product's palette, surfaces, props, actions, or narrative unless the current product independently supports them.
- Do not force lifestyle, gifting, people, packaging, process, care, back/inside, or installation images into a category that does not need them or lacks source evidence.
- Replace unsupported roles before writing prompts. Never generate an unseen back, inside, mechanism, label, flaw, package, process, result, or care claim as if it were factual proof.
- Let factual proof dominate when that is how the category is bought. Replacement parts, tools, raw materials, collectibles, vintage goods, and digital products may need fewer or no lifestyle scenes.
- Use category families as decision aids, not visual templates. A category label alone does not justify a luxury, cozy, minimalist, rustic, wedding, seasonal, or gift-ready art direction.
- If a planned image cannot answer a real buyer question or create truthful desire for this product, remove or replace it.

## Scene Coverage Gate

For every 15-image campaign, create a `scene_coverage_plan` before the coverage matrix. Use [references/category-adaptation.md](references/category-adaptation.md) to select the tier and [references/scene-direction.md](references/scene-direction.md) to design the actual environments.

Classify each shot as one of:

- `studio_evidence`: seamless, solid, gradient, paper, fabric, plinth, or isolated macro whose main purpose is clean factual proof;
- `contextual_evidence`: factual proof embedded in a recognizable, category-native place or spatial relationship;
- `functional_use`: the product being worn, handled, installed, operated, filled, opened, selected, or otherwise used truthfully;
- `ownership_story`: a believable before/during/after ownership moment that creates product-specific desire or meaning;
- `deterministic_graphic`: a comparison, option, instruction, or dimension composition whose exact text or lines are added after generation.

The plan must include:

- `scene_capacity` and the evidence for that classification;
- `target_mode_counts` across the five modes;
- `scene_bearing_shots`: every planned `contextual_evidence`, `functional_use`, and `ownership_story` shot;
- `pure_background_budget`: the maximum combined `studio_evidence` and visually plain `deterministic_graphic` shots;
- `environment_roster`: the distinct real environments, buyer moments, and spatial anchors used across the set;
- `dual_duty_roles`: factual roles that will also carry scale, use, setting, identity, or ownership context;
- `plain_background_exceptions`: each shot that genuinely needs visual isolation and why;
- `sequence_check`: how the carousel avoids long runs of studio or information-board images.

Use these 15-image defaults as a planning target and audit floor:

| Scene capacity | Typical products | Scene-bearing target | Minimum | Direction |
| --- | --- | ---: | ---: | --- |
| `experience_led` | decor, apparel, jewelry, gifts, personalized goods, food, beauty, leisure | 9–11 | 8 | combine desire, real use, scale, material, gifting or ownership without repeating one environment |
| `balanced` | furniture, craft supplies, many tools, kits, vintage goods, digital products with a real workflow | 6–8 | 5 | balance environmental proof with clean component, condition, compatibility, or content proof |
| `proof_led` | replacement parts, industrial components, raw materials, compatibility-critical goods, highly technical downloads | 3–5 | 3 when truthful context exists | favor real installation, workspace, compatibility, or workflow context; do not fabricate emotional lifestyle scenes |

A scene-bearing image must show a recognizable place, use relationship, or ownership moment. A new solid color, seamless sweep, fabric sheet, paper texture, isolated plinth, shadow pattern, foliage corner, or bokeh-only background does not count as a scene by itself.

Apply these gates:

- For `experience_led` sets, at least two of the first five images must be scene-bearing, and no more than two plain/studio or information-board images may appear consecutively anywhere in the carousel.
- For `balanced` sets, at least one of the first five images must be scene-bearing. Place contextual proof between factual studio images when it improves comprehension.
- Design evidence images as dual-duty scenes when accuracy remains clear: show size in a real spatial relationship, material in situ, personalization during selection or display, contents in a believable workspace, or variations in a controlled category-native context.
- Do not convert every evidence image into lifestyle. Exact color comparison, fragile detail, condition, compatibility, and deterministic text may require isolation; record those exceptions and keep the rest of the set spatially rich.
- Every scene-bearing shot must name an `environment_anchor`, `foreground_midground_background_plan`, `product_environment_contact`, and `scene_presence_evidence` in the coverage matrix and prompt.
- Count the actual final images, not their planned labels. If an intended room, use, or ownership scene renders as an isolated product on a colored field, audit it as `studio_evidence` and replace or rebalance it.

## Lifestyle Scene Creative-Direction Gate

When the set contains generated lifestyle, aspirational, human-use, gifting, or ownership scenes, read [references/scene-direction.md](references/scene-direction.md) before writing the coverage matrix or prompts.

Add a `scene_direction` object to the campaign plan with:

- `product_specific_story`: the product-specific ownership, use, memory, identity, or transformation the scenes should make visible;
- `emotional_payoff`: the feeling the target buyer should anticipate, tied to a real product use or ownership moment;
- `price_positioning`: the visual signals that support the product's intended market position without inventing luxury claims;
- `scene_worlds`: two to four related but visibly distinct environments, each with its own palette, surfaces, lighting, and moment;
- `visual_contrast_plan`: how the product separates from the background in value, hue, texture, scale, or focus;
- `scene_progression`: how the lifestyle images move from attraction to real use to emotional ownership rather than repeating one setup;
- `authenticity_cues`: natural interaction, believable wear or motion, physical contact, shadows, and small imperfections appropriate to the category;
- `forbidden_template_cluster`: the repeated palette, prop, background, camera, and product-state combination that would make the set look like generic stock imagery;
- `product_prominence_plan`: the intended visual hierarchy for each scene, including justified exceptions such as room-scale or fit proof.

Apply these gates:

- Write the product story before choosing props. A scene that can be reused unchanged for an unrelated product is too generic.
- Every lifestyle shot must show a distinct moment, not merely a new background. For a 15-image set, include a truthful functional interaction and an emotional ownership or outcome scene when the category and evidence support them.
- Count a scene as materially different only when at least three of these change for a reason: environment, palette/value structure, camera height or angle, visual distance, product state/action, human presence, lighting direction/time, or anchor prop family.
- Use props only when they establish context, scale, action, buyer identity, season, or story. Decorative filler is not a scene concept.
- Keep a small product unambiguously primary in ordinary lifestyle shots; normally plan it to occupy roughly 30%–60% of the frame unless the shot's stated purpose requires a wider scale context. Do not apply this range blindly to furniture, wall art, apparel fit, or room-scale products.
- Build contrast around the verified product. Do not default an entire campaign to pale neutral surfaces, flat high-key light, or one repeated color family merely because it looks clean.
- Human presence must create a believable action or relationship. Reject stiff display hands, impossible grips, pristine staged food, floating contact, or gestures that do not match actual use.
- Clean inventory, dimension, variation, and comparison images may intentionally use controlled backgrounds, but each one counts against the declared plain-background budget. Do not let this exception dominate a scene-capable set.

## Hero Image Rules

The hero is for correct clicks, not maximum clicks.

- Show one clear, complete, finished product or a clearly defined sold-together set.
- Keep the product large enough to identify quickly, well lit, sharp, and inside a center safe area.
- Avoid collages, poster-like layouts, small text, excessive badges, and dense option grids.
- Do not imply that props, frames, stands, inserts, tools, or accessories are included when they are not.
- When price/version data is supplied, do not show a premium version as the hero while a materially different low-cost option creates the displayed starting price without a clear explanation.
- Use a plain or lifestyle background according to category and buyer intent. Etsy does not require every hero to be pure white or every hero to be lifestyle photography.
- Do not describe square 1:1 as an Etsy requirement. Plan a square or landscape-friendly hero with enough breathing room to survive square, landscape, portrait, and mobile thumbnail crops.
- For Etsy framing, this rule overrides the sibling skill's square-first wording: 1:1 may remain the production default, but it must not be presented as Etsy's only accepted hero format.
- For personalized products, apply the completed-example rule from the publishing-readiness gate.

## Image Technical and Text Rules

- Target at least 2000 px in both practical image dimensions when the generation/export route supports it. Treat 635 × 635 px for the first image as a lower platform threshold, not the production target.
- Use sRGB, consistent white balance, controlled reflections, accurate color, and enough sharpness to inspect materials and edges.
- Preserve a high-resolution uncropped original before making Listing-specific crops.
- Do not apply obvious overlay watermarks. Prefer natural brand cues such as actual packaging or consistent styling when they are real.
- Keep the hero nearly text-free. Use text only on later information graphics where it answers one primary question.
- Add exact text, option labels, icons, arrows, and measurements deterministically after image generation. Do not trust image generation to spell or position them correctly.
- Any text-based image must remain readable at normal mobile width without zooming.

## Dimension and Scale Rules

Treat numeric dimension graphics as a deterministic step, not an ordinary generated lifestyle image.

- Lock every supplied number, unit, and label before image work. For international buyers, include inches and centimeters when both can be derived from confirmed source data without ambiguity.
- Generate or select a clean text-free base composition, then add numbers, lines, dots, arrows, and icons with deterministic graphics such as SVG, HTML/CSS, Pillow, or another exact overlay method.
- Verify every visible number, unit, endpoint, and line against the locked data before delivery.
- If exact dimensions are absent, do not invent them. Use a `dimension-ready_inventory` image or a `scale_effect` image with an ordinary object, hand, body crop, furniture, or room context whose relationship is realistic and non-deceptive.
- A scale scene must not enlarge or shrink the product relative to its confirmed dimensions.
- Clearly label styling or scale props that are not included when a reasonable buyer could misunderstand the bundle.
- Reject changed or extra numbers, misspelled units, tangled/crossing lines, overlapping labels, random arrows, unreadable mobile text, or measurements that cover buyer-critical product details.

## Variations and Personalization Rules

- Give each visible Variation a truthful visual representation when reference evidence exists.
- Use the exact same names in the image labels and Listing options; do not silently interchange names such as `Cream` and `Ivory`.
- Use consistent light, background, white balance, and scale across color/material comparison images.
- Do not replace real fabric, wood, metal, thread, or finish samples with generic screen color blocks.
- Create a `variation_mapping` in the plan that maps exact option names to source evidence and intended images. Live Listing association and switch behavior remain unverified until checked on Etsy.
- For personalization, show actual process-appropriate results. A computer font preview is not proof of embroidered, engraved, cut, or printed output.
- Keep option numbers, field names, character limits, capitalization, date format, and proof instructions consistent across images and Listing inputs.

## Optional Listing Video Briefs

This image skill does not create videos by default. If the user asks for Listing Video support, plan up to two separate briefs without counting them among the 15 images:

- `Video 1 — product and use`: size, movement, fit, capacity, operation, included items, or a common question;
- `Video 2 — craft and personalization`: making, engraving, embroidery, finishing, personalization, or packaging.

Use the knowledge-base production standard: 5–15 seconds, at least 1080 px when possible, under 100 MB, and understandable without sound. Do not make a static slideshow, depend on audio, use unreadable subtitles, repeat both videos, show a different product, or include unauthorized music, people, brands, or content. Do not promise a fixed sales lift from video.

## Alt Text

For a Listing-ready handoff, include an English alt-text draft for each final image when useful:

- describe only what is visibly present, including appearance, texture, scale, action, and relevant setting;
- keep each entry within 250 characters;
- do not copy the Title or Tags and do not use keyword-list stuffing;
- mark alt text as a draft until it is checked against the final uploaded image.

## Workflow

1. Inspect all required references and complete the product-truth and source-classification gates.
2. Load `product-photo-campaign-openrouter`, `references/category-adaptation.md`, and `references/scene-direction.md`. Create the product intelligence, `category_adapter`, `scene_coverage_plan`, image-set strategy, applicable `scene_direction`, coverage matrix, shot briefs, and one prompt per shot.
3. Map the 15 shots to distinct buyer questions and background modes using the buyer-journey template and documented role substitutions. Verify the scene-bearing floor, plain-background budget, early-carousel mix, environment roster, and sequence before generation. Reject a plan that repeats role, question, angle, distance, product state, prop logic, or scene-world combination without a documented reason.
4. Add `publish_readiness`, `source_classification`, `missing_evidence`, `variation_mapping`, `dimension_data_locked`, `non_included_items`, and `mobile_qa_plan` to the campaign plan.
5. Generate `shot-01` as a health and fidelity probe and inspect the actual image. Before the remaining set, `experience_led` and `balanced` campaigns must generate two different scene probes: one `contextual_evidence_probe` that proves a buyer fact inside a real environment, and one `use_or_ownership_probe` that proves action or emotional meaning. A `proof_led` campaign may use one or two context/workflow probes according to safe use. Audit product fidelity, spatial depth, environmental specificity, story, visual hierarchy, contrast, and authenticity. If the user has rejected an earlier direction or explicitly wants approval, pause after the probes; otherwise use them as internal gates. Preserve passed shots and resume only missing or rejected shots.
6. Use deterministic overlays for all exact measurement and option graphics.
7. Independently compare each output with the references and locked facts. Only `pass` images enter the final set by default.
8. Build a contact sheet for final-set review, not as an image-generation reference. Reclassify every actual image by background mode, count scene-bearing versus plain images, and inspect thumbnail-size repetition in palettes, surfaces, prop clusters, camera positions, product states, and consecutive studio/info-board runs.
9. Run the Etsy-specific final audit below. A generation tool success or an existing file alone is not evidence that the image is usable.

## Etsy-Specific Final Audit

For each image, record:

- shot role and buyer question answered;
- source type and whether real-product evidence remains visible/available;
- product structure, proportions, component count, material, color, hardware, artwork, text, and included-item fidelity;
- dimensions/scale fidelity and non-included prop clarity;
- personalization and Variation label accuracy where applicable;
- scene, angle, distance, crop, and prop uniqueness;
- actual background mode, environmental anchor, depth layers, product-environment contact, and whether the scene-bearing test passes;
- for lifestyle images, the five-part creative score from `references/scene-direction.md` and any failed dimension;
- mobile thumbnail safety and mobile text readability;
- `pass`, `borderline`, or `reject`, with the reason.

Also verify the set as a whole:

- the hero is a clear finished product, not a collage or text poster;
- the first five images answer the main purchase questions;
- the `category_adapter` matches the product form and dominant buyer decisions;
- every inapplicable or unsupported template role was replaced with evidence-supported category-native proof;
- no palette, prop cluster, action, or story was inherited from an unrelated product campaign without current-product justification;
- the actual scene-bearing count meets the declared tier floor, or a documented evidence limitation correctly changes the status from `VERIFIED_SUCCESS`;
- the actual pure/studio and deterministic-graphic count stays within budget, and intended scenes that collapsed into colored fields were reclassified rather than excused;
- `experience_led` sets contain at least two scene-bearing images among the first five and never run more than two plain/studio or information-board images consecutively;
- real-product evidence and permitted mockup use satisfy the publishing-readiness gate;
- all 15 roles add buyer value and no filler scene remains;
- the contact sheet does not reveal a template cluster, repeated pale-neutral setup, or multiple background swaps posing as distinct lifestyle scenes;
- lifestyle scenes progress through different buyer moments while preserving one coherent visual identity;
- key exclusions, size information, and limitations are not buried;
- the set does not imply unverified price, shipping, delivery, review, or conversion claims;
- square, landscape, portrait, and mobile crops keep the product identifiable;
- optional video briefs are distinct, silent-first, and technically compliant.

Do not call a campaign `VERIFIED_SUCCESS` unless all 15 final images exist, independently pass the fidelity and Etsy-specific audits, and every required source/fact gate is satisfied. If the assets have not been uploaded and checked on Etsy, report asset production separately from live Listing verification.

## Output

Save durable outputs under the user-requested directory; otherwise use an `outputs/` folder in the current workspace:

```text
<out-dir>/
  plan.codex-direct.json
  source-manifest.json
  prompts/
    shot-01.txt
    ...
    shot-15.txt
  shot-01.png
  ...
  shot-15.png
  alt-text.json
  fidelity-audit.json
  listing-readiness-audit.json
  video-01-brief.txt        # only when requested
  video-02-brief.txt        # only when requested
```

In the final report, separate:

- references and confirmed facts checked;
- images generated and final files delivered;
- rejected, regenerated, reference-based, or missing shots;
- locked dimension data versus scale-only cues;
- real-photo, mockup, AI, personalization, Variation, and licensing status;
- asset audit result;
- live Etsy Listing verification status;
- blockers and the smallest seller action required.
