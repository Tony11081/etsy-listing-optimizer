# Etsy Product Photo 15 for Codex

A reusable Codex skill bundle for planning and generating a cohesive,
reference-locked set of 15 Etsy listing images with Codex's built-in
`image_gen` tool.

The bundle contains:

- `etsy-product-photo-15`: the Chinese 15-image Etsy campaign entrypoint.
- `product-photo-campaign-openrouter`: the Codex-native planning, generation,
  and fidelity-audit workflow required by the entrypoint. Despite the legacy
  name, it does not use OpenRouter or require an external API key.

## Requirements

- Codex with access to the built-in `image_gen` tool.
- At least one readable product reference image.
- Both skill folders from this repository.

## Install

Clone or download this repository, then copy both folders inside `skills` to
your Codex skills directory.

### Install by asking Codex

Paste this request into Codex:

```text
Install both Codex skills from https://github.com/Tony11081/etsy-listing-optimizer: skills/etsy-product-photo-15 and skills/product-photo-campaign-openrouter.
```

### One-command installer

PowerShell:

```powershell
python "$env:USERPROFILE\.codex\skills\.system\skill-installer\scripts\install-skill-from-github.py" --repo Tony11081/etsy-listing-optimizer --path skills/etsy-product-photo-15 skills/product-photo-campaign-openrouter
```

macOS or Linux:

```bash
python ~/.codex/skills/.system/skill-installer/scripts/install-skill-from-github.py --repo Tony11081/etsy-listing-optimizer --path skills/etsy-product-photo-15 skills/product-photo-campaign-openrouter
```

### PowerShell

```powershell
$skillsDir = Join-Path $env:USERPROFILE '.codex\skills'
New-Item -ItemType Directory -Path $skillsDir -Force | Out-Null
Copy-Item -Recurse -Force '.\skills\etsy-product-photo-15' $skillsDir
Copy-Item -Recurse -Force '.\skills\product-photo-campaign-openrouter' $skillsDir
```

### macOS or Linux

```bash
mkdir -p ~/.codex/skills
cp -R skills/etsy-product-photo-15 ~/.codex/skills/
cp -R skills/product-photo-campaign-openrouter ~/.codex/skills/
```

Restart Codex after installation so the new skills are discovered.

## Use

Attach one or more product reference images and ask:

```text
Use $etsy-product-photo-15 with my product images to create a complete Etsy listing photo set.
```

The skill plans exactly 15 images by default, generates each image separately,
and audits reference fidelity, scene diversity, product details, dimensions,
and included-item accuracy.

## 中文说明

这是一个使用 Codex 自带 `image_gen` 的 Etsy 商品图 Skill 套装，不需要
OpenRouter 或外部图片 API Key。安装时必须同时复制 `skills` 目录下的两个
Skill 文件夹。使用时上传清晰的商品参考图，然后调用
`$etsy-product-photo-15` 即可生成包含 15 张图片的完整方案。

尺寸数据、商品结构、材质、颜色、文字和配件数量必须以参考资料为准；没有
提供准确尺寸时，Skill 不会虚构数字。

## License

MIT License. See [LICENSE](LICENSE).
