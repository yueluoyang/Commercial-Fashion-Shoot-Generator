---
name: commercial-fashion-shoot-generator
description: "Analyze user-provided model and womenswear product images, infer exact garment construction, recommend or accept 2-3 indoor commercial shoot set styles, wait for the user to choose a set, then generate a four-image 3:4 online fashion gallery with the same model, same indoor set, exact garment preservation, and GPT Image 2/image_gen prompts. Use for commercial womenswear photography, ecommerce product display, AI try-on campaign images, front/back/dynamic/detail fashion image generation, and requests that ask to template this workflow."
---

# Commercial Fashion Shoot Generator

Use this skill to turn a model reference plus product images into a polished four-image commercial womenswear gallery. The workflow is intentionally gated: analyze first, propose or accept the indoor set style, wait for user selection, then generate final images.

Do not invoke `fashion-img2img-script-writer` or any local fashion img2img skill while using this skill. Use the built-in `image_gen` flow unless the user explicitly asks for another image-generation path.

## Required Inputs

- Model reference image: preserve the model identity, face, body type, hair, makeup mood, and skin tone.
- Product front image: primary source for front construction, neckline, waist, seams, ruffles, closures, length, fabric, color, and silhouette.
- Product back or side/back image: primary source for back construction, armholes, straps/sleeves, back seams, closure visibility, skirt shape, and hem.
- Optional user-provided indoor set style: if provided, use it after checking that it fits the garment and ecommerce purpose.

If a required image is missing, ask only for the missing image. If all required inputs are present but no set style has been chosen, do not generate final images yet.

## Workflow

1. Load and inspect the visible input images. If local paths are referenced but not visible in the conversation, use `view_image` first so the images are in context.
2. Analyze the garment using `references/garment-analysis.md`.
3. Recommend 2-3 indoor shoot styles using `references/indoor-set-styles.md`, unless the user already supplied a set style.
4. Present the analysis and set options concisely, then ask the user to choose one option or provide their own.
5. After the user chooses or confirms the set style, generate exactly four 3:4 images:
   - front product view
   - back product view
   - dynamic candid/action view
   - detail close-up
6. Use one `image_gen` call per deliverable, with separate prompts based on `references/prompt-templates.md`.
7. Keep the four prompts aligned on the same model identity, same indoor set, same lighting, same styling, and same garment invariants.
8. Inspect results. If a result clearly breaks garment construction, identity, ratio, or set consistency, iterate with one targeted correction for that image.
9. Report the final output paths and summarize the chosen set style and any caveats.

## Non-Negotiable Output Rules

- Produce four images, all 3:4 vertical.
- Use the same model in all images.
- Use the same indoor shooting location, style, lighting, props, and seasonal mood across all images.
- Preserve the product garment exactly. Do not change silhouette, neckline, sleeve/strap design, length, hem, seams, ruffles, pleats, closures, fabric type, color family, or decorative details.
- Keep the images suitable for online womenswear sales: clear garment visibility, flattering but honest fit, realistic fabric, commercial lighting, no distracting props.
- Allow interaction with set elements only when it does not hide or distort the garment.
- Avoid logos, watermark, visible prompt artifacts, text, extra garments, invented accessories, face masks, color blobs, and reference-image defects.

## Response Pattern Before Generation

When the user has not chosen a set style, respond with:

- Garment analysis: concise but specific.
- Product risk notes: details most likely to drift during generation.
- 2-3 indoor set style options: each with mood, props, light, why it fits the garment.
- A direct request for the user to choose one option or provide a custom style.

Do not produce the final four images in the same turn as initial set recommendations unless the user already selected a set style.

## Response Pattern After Generation

After generating, keep the final answer short:

- Name the four deliverables.
- Provide final saved paths if available.
- State that the workflow used built-in image generation/GPT Image 2 style prompting and did not use the local fashion img2img skill.

## References

- `references/garment-analysis.md`: use to extract exact product construction and invariants.
- `references/indoor-set-styles.md`: use to recommend or validate indoor shoot styles.
- `references/prompt-templates.md`: use to write the four final image prompts.
