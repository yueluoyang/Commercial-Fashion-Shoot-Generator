# Shooting Script Guide

Use this guide from the beginning of the workflow. It merges garment style analysis with product attributes, physical selling points, and four-image ecommerce logic. Use it before recommending or accepting an indoor set style, then use it again after the user chooses the set style to create the four-shot script before image generation. It is distilled from the user's womenswear AI shooting-script DOCX guide and adapted to this skill's required deliverables: 正面图, 背面图, 细节特写图, and 创意特性图.

## Core Principle

Treat the four images as a conversion-oriented ecommerce sequence, not four isolated photos. Each shot must translate garment physics into visual selling value:

- 正面图: first-look trust, true color, full silhouette, exact front construction.
- 背面图: remove uncertainty about back cut, waist shaping, closures, seams, and hem.
- 细节特写图: reduce the "cannot touch fabric online" problem through texture, stitching, drape, edge, and construction fidelity.
- 创意特性图: the most important feature shot; project a wearing scenario and amplify the strongest physical selling point through scene, pose, camera, light, and motion when appropriate.

## Fixed Model Proportion Lock

Use these body proportions throughout planning, script writing, prompt writing, and image critique:

- Height: 1.68m.
- Head-to-body ratio: 7.5 heads.
- Leg-length ratio: lower-body length from navel/pubic symphysis to floor divided by height equals 0.64.
- Preserve the reference model identity while standardizing the body to these proportions.
- Do not rely on camera distortion to fake a different real body in the neutral product images.
- In 创意特性图 only, controlled low angle, perspective, or unconventional poses may be used as visual engineering when they clearly amplify the product's physical selling point. Keep anatomy plausible and make the script state the perspective purpose.

## RACE Planning Frame

Use this frame for the first product analysis and for the later confirmed script:

- Role: act as a multimodal visual planning expert with more than 10 years of womenswear ecommerce visual-director and senior fashion-photographer experience. Be highly sensitive to fabric, cut, silhouette, construction, camera, lighting, model body language, and perspective.
- Action: inspect the uploaded womenswear product images, ignore hangers/background boards/flat-lay props/non-garment artifacts, produce a multidimensional fashion-attribute analysis, then tailor a high-conversion four-image ecommerce shooting plan that maximizes the product's physical and cutting features.
- Context: follow the four core ecommerce images and their physical-to-visual translation rules, while honoring the selected indoor set, online sales purpose, product invariants, fixed model proportions, and same-model/same-location constraints.
- Example logic: map fabric, cut, silhouette, and key details to camera, lighting, pose, scene psychology, and commercial purpose.

## Fused Product Analysis Before Set Recommendation

Do not run a separate generic garment-analysis stage before this guide. Before proposing or accepting a set style, analyze the garment directly through this guide and produce a concise report covering:

- Clothing category and basic silhouette.
- Material/fabric physical expression: drape, structure, surface texture, sheen, transparency, stretch, weight.
- Core product highlight or creative selling point: slit, ruffle, sleeve volume, waist shaping, wide leg, texture, back detail, etc.
- Core wearing mindset: commuting, elegance, relaxed home, vacation, formal event, spring freshness, quiet luxury, etc.
- Ecommerce shot logic: what 正面图, 背面图, 细节特写图, and 创意特性图 must each prove.
- Scene compatibility: which indoor environments best support the product's mood without hiding key construction.
- Model proportion protection: whether the set, lens height, furniture, or pose could distort the locked 1.68m / 7.5-head / 0.64 leg-ratio body.

## Script Inputs

Before writing the script, carry forward:

- Garment category, silhouette, length, color, fabric, and construction invariants.
- Core product highlight or "physical selling point": ruffle, slit, drape, waist shaping, texture, sleeve volume, back detail, wide leg, etc.
- Selected indoor set style and its props/light.
- Fixed model proportions: 1.68m height, 7.5-head body ratio, 0.64 leg-length ratio.
- Styling completion plan for separates or non-full-body products, including footwear. Unless the user requests otherwise, the model must not be barefoot.
- Drift risks that must be blocked during image generation.

## Four-Shot Logic

### 1. 正面图（正面视觉锤）

- Use standard eye-level medium or mid-long framing.
- Use a clean centered composition so shoulder line, chest width, waist, hem, color, and overall silhouette are readable.
- Keep the model's posture direct, natural, and symmetrical.
- Use a minimal background and soft focus/softbox-style light with no harsh shadows.
- Avoid hands, props, hair, or furniture covering key front details.

### 2. 背面图（版型细节展示）

- Keep background and lighting visually continuous with the front view.
- Use back or side-back angle; optional gentle over-shoulder head turn only when it does not hide the back design.
- Show shoulder/strap/sleeve construction, back waist, darts or seams, closure area, skirt/pants back, and hem.
- Avoid inventing back bows, cutouts, exposed zippers, or extra closures.

### 3. 细节特写图（面料肌理雕刻）

- Use close-up or macro-style framing with shallow depth of field.
- Choose the detail based on product value: neckline, ruffle edge, button, zipper, waist seam, sleeve cuff, pocket, stitching, fabric texture, hem, drape, or back closure.
- Use lighting based on material:
  - Knit, linen, cotton texture, tweed, rib, rough or raised surfaces: angled side light to reveal micro-shadows.
  - Silk, satin, glossy synthetic, smooth crepe: broad diffused light to avoid blown highlights while preserving sheen.
  - Sheer/chiffon/lace: backlight or soft side light to show translucency and edge detail.
- Hands may indicate scale or touch fabric lightly, but must not cover the detail being sold.

### 4. 创意特性图（场景心智投射）

- Treat this as the core selling image, not a generic dynamic candid.
- Identify the most unique physical creative point in the garment and design the most persuasive scene, camera angle, lighting, and model posture to amplify it.
- Allow controlled low-angle camera work, perspective, and unconventional poses when they better sell the product feature, including crouching, kneeling, deep seated poses, crossed or propped legs, leaning, twisting, or other editorial body language.
- Use the user's examples as valid creative logic: for wide-leg pants, a crouched pose with an upward camera can exaggerate volume and fabric width; for a high-slit skirt or dress, a chair pose with crossed/propped legs can reveal the slit and add feminine appeal while keeping the product readable.
- For unlisted product types, think from the garment's physical behavior first; if the best creative solution is not obvious, optionally search the web for current fashion ecommerce/editorial references, then adapt only the idea, not any brand identity or copyrighted composition.
- Choose the creative logic based on garment physics:
  - Pajamas/loungewear/homewear: morning bedroom or relaxed indoor home scene; sleeping, turning, stretching, leaning, or soft waking gestures.
  - Slit or large hem/swing design: breezy environment; confident forward stride or controlled turn so the hem moves backward and the slit or swing becomes visible. Keep it commercial and elegant.
  - Wide-leg pants/high-waist trousers: minimal geometric modern interior; use controlled low angle, crouching, kneeling, or asymmetric leg placement to exaggerate pant volume, fabric fall, and spatial width while keeping anatomy believable.
  - Other categories: infer the strongest physical creative point and design a pose, light, set interaction, or perspective that makes that point immediately desirable.
- Keep the garment readable; avoid extreme motion blur, anatomy distortion, or body-ratio drift.

## Required Script Output

After set selection, output a concise script in this structure and ask for confirmation:

```markdown
一、服装多模态属性解析报告
- 服装品类与基本版型: <category and silhouette>
- 材质面料物理表现: <fabric behavior, drape, structure, texture, sheen>
- 产品核心亮点/创意卖点: <one or more physical selling points>
- 核心穿搭心智定位: <wearing mindset / consumer projection>

固定模特比例锁: 身高1.68m；头身比7.5；腿长比例0.64。保持同一模特身份，并让四张图中的身体比例一致。

生成风险备注: <details most likely to drift and must be locked>

二、4张电商主图拍摄分镜脚本
| 主图序号 | 构图、景别与机位角度 | 空间场景与环境布光 | 模特调度（肢体动作与细节展现） | 视觉呈现目的 |
|---|---|---|---|---|
| 正面图 | ... | ... | ... | ... |
| 背面图 | ... | ... | ... | ... |
| 细节特写图 | ... | ... | ... | ... |
| 创意特性图 | ... | ... | ... | ... |

Please confirm this shooting script, or tell me which shot to revise. I will generate images only after confirmation.
```

## Script Quality Rules

- Be specific enough that each row can become an image prompt without reinterpretation.
- Tie every pose, camera angle, and light choice to a garment property or sales purpose.
- Keep the selected indoor set consistent across all rows.
- Keep the model's height, head-to-body ratio, and leg-length ratio consistent across all rows by writing the proportion lock into camera and model-direction decisions, not as an extra table column. For 创意特性图, controlled perspective is allowed only as a shot effect and must not mutate anatomy or garment construction.
- Do not introduce props or actions that hide the product.
- Never replace 创意特性图 with a generic dynamic candid; motion is allowed only when it expresses the product's core physical selling point.
- For separates or non-full-body items, include tasteful supporting outfit pieces and footwear in the script. Never make the model barefoot unless the user explicitly requests it.
- Keep the user's original four-image constraints unchanged.
