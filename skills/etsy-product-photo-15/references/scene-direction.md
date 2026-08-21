# Etsy Lifestyle Scene Direction

Use this reference only when planning or auditing generated lifestyle, aspirational, gifting, human-use, or emotional-ownership images. It does not replace product-truth, dimension, variation, licensing, or publishing-readiness rules in `SKILL.md`.

## 1. Start With a Product-Specific Story

Write one sentence that connects the verified product to a real buyer moment:

`This product helps <buyer> experience or express <specific outcome> during or after <real use moment>.`

Then define a three-beat scene progression:

1. `desire`: the buyer immediately imagines the product in the right world;
2. `use`: a believable action proves how the product participates in that world;
3. `ownership`: the product remains meaningful, useful, displayable, giftable, or memorable after the first use.

The story must depend on this product's category, design, personalization, material, or function. Reject concepts that would work unchanged after swapping in an unrelated product.

Examples are patterns, not mandatory scenes:

- wedding or event goods: anticipation, real ritual/use, quiet keepsake or anniversary ownership;
- home decor: arrival or placement, lived-in interaction, identity or memory within the home;
- jewelry: choosing or dressing, worn scale and movement, gifting or everyday identity;
- craft objects: tactile use, evidence of making, long-term display or heritage;
- apparel: outfit decision, natural movement and fit, repeated everyday styling.

Do not invent a ceremony, heritage claim, recipient, packaging, production process, or included accessory that is not supported by the product and request.

## 2. Build Scene Worlds, Not Background Swaps

Create two to four `scene_worlds`. Each world needs:

- a purpose in the buyer journey;
- an environment and time or light condition;
- a deliberate palette and value structure;
- one primary surface or spatial anchor;
- a distinct product state or interaction;
- a camera family and visual distance;
- no more than one anchor prop family unless additional props are essential.

Keep cohesion through two or three devices such as consistent product color, shadow softness, editorial restraint, recurring material, or grading. Create variety through meaningful changes in moment and visual structure.

For each lifestyle shot, compare it with all earlier lifestyle shots. It should change at least three of:

- environment;
- light/dark value structure or dominant palette;
- camera height, angle, or lens feeling;
- wide, medium, close, or macro distance;
- product state, position, or action;
- human-presence mode;
- lighting direction or time of day;
- anchor prop family.

A new tabletop, flower arrangement, fabric color, or wall is insufficient by itself.

### Scene-bearing standard

Classify the actual image, not the prompt label. A scene-bearing image should make at least two of these visible and believable:

- a recognizable real place or spatial anchor, such as room architecture, furniture relationship, workspace, body, appliance, wall, shelf, landscape, or event setting;
- product-to-environment contact or use, such as hanging, resting with weight, being worn, installed, filled, opened, gripped, selected, packed, operated, or displayed at a meaningful scale;
- foreground, midground, and background depth or another clear spatial hierarchy;
- evidence of a buyer moment, action, transition, or owner presence that would be incomplete without the product.

A solid color, seamless sweep, paper/fabric texture, isolated plinth, gradient, cast-leaf shadow, foliage corner, or bokeh lights do not make a scene by themselves. Treat these as `studio_evidence` unless a real place, use relationship, or ownership moment is also legible.

### Dual-duty evidence scenes

Do not isolate every factual role on a plain board. When fidelity and readability allow:

- prove scale through a truthful body, furniture, room, workspace, appliance, or use relationship;
- prove material and craft where light, touch, edge, or contact makes the quality understandable;
- show personalization during choosing, gifting, displaying, remembering, or using the completed item;
- show contents or components in the workspace or sequence where their relationship becomes clear;
- place deterministic measurements or instructions over a restrained contextual base rather than automatically using a blank gradient.

The evidence question remains primary. If context reduces color, condition, text, option, or compatibility accuracy, keep that individual shot controlled and spend the scene budget elsewhere.

### Environmental specificity and depth

For every scene-bearing shot, specify:

- exact place and buyer moment;
- time of day or motivated light source;
- foreground, midground, and background elements;
- the surface, wall, body, fixture, or object physically anchoring the product;
- product contact, weight, reflection, shadow, displacement, tension, or motion;
- one sign of real use or owner presence;
- what makes this environment different from every other scene world.

Avoid “product on a table in a beautiful room.” Describe the observable spatial relationships that make the scene photographable.

## 3. Design the Visual Hierarchy

State the intended order in which the eye should read the frame. In most small-product lifestyle images:

1. product or product-in-action;
2. relevant hand, wearer, recipient, or usage result;
3. environment and props.

Use value, hue, texture, depth of field, leading lines, negative space, and directional light to separate the product. For small products, roughly 30%–60% frame occupancy is a useful starting range for ordinary lifestyle scenes; wider scale proof is an explicit exception, not the default.

Reject the scene when:

- the cake, plant, furniture, architecture, model, or decorative prop becomes the real subject;
- the product is difficult to identify at Etsy thumbnail size;
- pale product, pale surface, pale props, and flat light merge into one low-contrast field;
- shallow depth of field hides buyer-critical texture, engraving, hardware, edges, or personalization.

## 4. Use Props as Evidence

Every visible prop must do at least one job:

- establish the real use context;
- prove scale;
- enable the action;
- identify the buyer or occasion;
- support a verified season or style;
- reinforce material or color contrast.

Remove props that only fill empty space. Avoid default filler clusters such as flowers plus linen plus coffee plus books, or their category equivalent, unless each item has a specific role. Reusing the same prop family in multiple scenes requires a different moment and composition, not merely a rearrangement.

Never let styling imply that a non-included item, premium venue, gift box, stand, frame, tool, or accessory is part of the purchase.

## 5. Make Human Interaction Believable

Specify the exact body crop, grip, direction of force, point of contact, and product detail that must remain visible.

Prefer:

- two hands when the real action naturally involves coordination;
- partial-body or point-of-view framing when it makes the buyer imagine ownership;
- natural pressure, weight, wrinkles, crumbs, motion, or displacement caused by the action;
- hands that hold the product at structurally plausible points.

Reject:

- mannequin-like hands posed only to decorate the frame;
- impossible grip, scale, finger count, contact, or tool angle;
- action with no physical effect on nearby material;
- perfect untouched food, fabric, packaging, or surfaces when the scene claims active use;
- people who obscure the product or turn the image into generic lifestyle stock.

## 6. Prompt for the Moment, Not for Adjectives

Replace vague directions such as `luxury`, `beautiful`, `cozy`, or `Pinterest style` with observable decisions:

- exact environment and buyer moment;
- product position and action;
- background value relative to the product;
- primary and secondary colors;
- surface materials;
- camera height, angle, distance, and focal emphasis;
- light source, direction, softness, time, shadow, and reflection behavior;
- one or two authenticity cues;
- props to include and default filler to exclude;
- what must differ from the other shots.

Add a shot-specific `anti_template` line to each lifestyle prompt. It should name the repeated treatment that this shot must avoid, based on the current coverage matrix, rather than using a universal negative list.

## 7. Scene Probes

After the factual `shot-01` probe passes, `experience_led` and `balanced` campaigns must generate two different probes:

1. `contextual_evidence_probe`: a buyer fact such as scale, material, contents, finish, placement, or personalization proved inside a real environment;
2. `use_or_ownership_probe`: a believable action, fit, ritual, workflow, display, or emotional ownership moment.

For a `proof_led` product, use one or two probes according to safe context. When there is no truthful emotional story, use installation, compatibility, workspace, or workflow scenes instead. Choose visually ambitious but truthful scenes, not the easiest pale-background setup.

Audit the actual probe for:

- accurate product and included items;
- clear product-first hierarchy at thumbnail size;
- product-specific story rather than generic decor;
- sufficient contrast and material separation;
- believable action, contact, shadows, and scale;
- fit with intended price position;
- enough creative headroom for the other scene worlds to remain distinct.
- clear foreground/midground/background or another convincing spatial structure;
- observable product-to-environment contact rather than a cutout floating in a scene.

If the probe fails, revise the scene direction or prompt structure before generating more scenes. Do not treat a technically valid image as a style pass.

## 8. Creative Score and Contact-Sheet Audit

Score each lifestyle image from 0 to 2 on five dimensions:

1. `narrative_specificity`: could the scene only plausibly belong to this product or buyer moment?
2. `product_prominence`: is the product the clear subject and identifiable at thumbnail size?
3. `visual_distinction`: is the scene materially different from the other lifestyle shots while still cohesive?
4. `interaction_authenticity`: does use, contact, motion, scale, and physical response look believable?
5. `price_and_brand_fit`: do palette, materials, lighting, styling, and restraint support the intended positioning?

Creative pass threshold: at least 8/10 and no dimension scored 0. Product truth and source safety remain separate hard gates; a high creative score cannot rescue inaccurate product depiction.

Build a contact sheet and inspect the full set at once. Reject and replace a cluster when three or more lifestyle images share the same broad palette/value structure, surface family, prop family, camera family, and static product state without a buyer-journey reason. Also reject when multiple images are effectively the same composition with background substitutions.

Reclassify every final image as `studio_evidence`, `contextual_evidence`, `functional_use`, `ownership_story`, or `deterministic_graphic`. Record the actual counts and compare them with the declared scene-capacity floor and plain-background budget. An intended scene that rendered as a product on a colored or blurred field is `studio_evidence`, even if the prompt asked for a room.

For an `experience_led` set, reject the set-level mix when fewer than eight of 15 images are scene-bearing, fewer than two of the first five are scene-bearing, or more than two plain/studio or information-board images run consecutively. Apply the corresponding lower floor from `SKILL.md` to `balanced` and `proof_led` sets.

Record the weak cluster, retained images, replacement roles, and new scene-world requirements before regenerating. Regenerate only rejected scenes, then rebuild and reread the contact sheet.
