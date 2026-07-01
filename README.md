# Etsy Listing Optimizer

A Codex skill for Etsy listing SEO and conversion work.

It helps diagnose Etsy titles, rewrite English listing titles, generate Etsy-ready tags, improve product descriptions, review image/click-through strategy, and give practical positioning advice for furniture and custom decor listings.

## What It Does

- Scores Etsy title and SEO quality.
- Rewrites product titles with the strongest keywords early.
- Generates exactly 13 Etsy-ready tags by default.
- Reviews listing images, first-image click-through quality, and missing product shots.
- Scores description/CRO quality and rewrites the opening copy.
- Gives practical pricing, positioning, customization, and Etsy Ads suggestions.
- Includes safety rules for uncertain claims such as `solid wood`, `glider`, `handmade`, branded terms, and medical/orthopedic language.

## Install

Copy this folder into your Codex skills directory:

```powershell
$skillsDir = "$env:USERPROFILE\.codex\skills"
git clone https://github.com/Tony11081/etsy-listing-optimizer.git "$skillsDir\etsy-listing-optimizer"
```

Restart Codex after installing so the skill appears in the available skills list.

## Use

In Codex, invoke:

```text
$etsy-listing-optimizer
```

Then send the product data you want reviewed, such as:

- Current title
- Tags
- Description
- Product photos or image descriptions
- Price
- Materials
- Size
- Production time
- Shipping details
- Customization options

## Output

The default diagnosis uses Chinese analysis and English Etsy-facing listing assets:

- Title/SEO diagnosis
- 3 optimized English titles
- 13 Etsy tags on one comma-separated line
- Visual merchandising advice
- Description/CRO diagnosis
- Rewritten first three description lines
- Competitive strategy
- Important missing facts to confirm

## Notes

The skill references official Etsy Seller Handbook and Etsy Help Center pages when current Etsy policy or policy-sensitive claims need verification.
