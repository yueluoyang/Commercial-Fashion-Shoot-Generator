---
name: commercial-fashion-shoot-generator
description: "Analyze user-provided model and womenswear product images through the womenswear AI shooting-script guide; recommend or accept indoor commercial shoot set styles; generate a confirmed four-shot ecommerce script; create a 3:4 four-image gallery with the same model, fixed body proportions, same indoor set, exact garment preservation, styling completion for separates, no barefoot unless requested, and GPT Image 2.0/image_gen prompts; allow product-led low-angle/perspective/unconventional poses for creative-feature shots; ask for satisfaction/corrections; optionally generate color-variant galleries. Use for commercial womenswear photography, ecommerce display, AI try-on campaign images, scripts, creative-feature generation, color variants, and workflow templating."
---

# Commercial Fashion Shoot Generator

Use this skill to turn a model reference plus product images into a polished four-image commercial womenswear gallery. The workflow is intentionally gated: use the shooting-script guide as the primary analysis frame, propose or accept the indoor set style, wait for user selection, write a four-shot shooting script for approval, generate the first gallery from the approved script, ask for satisfaction/corrections, then optionally generate color variants after the user confirms the first batch is fully correct.

Do not invoke `fashion-img2img-script-writer` or any local fashion img2img skill while using this skill. Use GPT Image 2.0 through the built-in `image_gen` flow unless the user explicitly asks for another image-generation path.

## Required Inputs

- Model reference image: preserve the model identity, face, body type, hair, makeup mood, and skin tone.
- Product front image: primary source for front construction, neckline, waist, seams, ruffles, closures, length, fabric, color, and silhouette.
- Product back or side/back image: primary source for back construction, armholes, straps/sleeves, back seams, closure visibility, skirt shape, and hem.
- Optional user-provided indoor set style: if provided, use it after checking that it fits the garment and ecommerce purpose.

If a required image is missing, ask only for the missing image. If all required inputs are present but no set style has been chosen, do not generate final images yet.

## Workflow

1. Load and inspect the visible input images. If local paths are referenced but not visible in the conversation, use `view_image` first so the images are in context.
2. Study `references/shooting-script-guide.md` first. Use it as the primary analysis frame to produce one fused garment analysis covering style, product attributes, physical selling point, four-image ecommerce logic, and fixed model proportion protection. Use `references/garment-analysis.md` only as a supporting checklist inside this fused analysis, not as a separate workflow stage.
3. Recommend 2-3 indoor shoot styles using `references/indoor-set-styles.md`, unless the user already supplied a set style. If the user supplied a set style, validate it against the guide-based product analysis before accepting it.
4. Present the fused multimodal product analysis, fixed model proportion lock, and set options concisely, then ask the user to choose one option or provide their own.
5. After the user chooses or confirms the set style, create a four-shot ecommerce shooting script for user confirmation using the exact four Chinese deliverable labels specified in `references/shooting-script-guide.md`: front image, back image, detail close-up image, and creative-feature image.
6. Do not generate images until the user confirms the shooting script. If the user requests script changes, revise the script and ask for confirmation again.
7. After confirmation, use one `image_gen` call per deliverable, with separate prompts based on `references/prompt-templates.md` and the approved shooting script.
8. Keep the four prompts aligned on the same model identity, fixed model body proportions, same indoor set, same lighting, same styling, same garment invariants, and approved shot intent.
9. Inspect results. If a result clearly breaks garment construction, model identity, fixed body proportions, ratio, set consistency, or the approved script, iterate with one targeted correction for that image.
10. After delivering the first batch, ask whether the user is satisfied or wants any edits/corrections. Do not move to color variants until the user confirms the first batch is fully correct.
11. If the user requests corrections, revise only the specified image(s) and issue(s), then ask for satisfaction again.
12. After the user confirms the first batch is fully correct, ask whether they want color variants.
13. If the user wants color variants, follow `references/color-variant-workflow.md`: ask for additional color reference images, keep the same model, same fixed body proportions, same base indoor set, exact garment construction, same four-shot script structure, GPT Image 2.0/image_gen path, and 3:4 ratio; optionally adjust only small props or decor to fit each color.
14. For each confirmed color variant, generate four images using the same approved script structure and the color-variant prompt rules in `references/prompt-templates.md`.
15. Report final paths grouped by original batch and color variant.

## Fixed Model Body Proportions

Carry this lock through the analysis, scene recommendation, shooting script, prompt writing, image generation, and iteration stages:

- Height: 1.68m.
- Head-to-body ratio: 7.5 heads.
- Leg-length ratio: lower-body length from navel/pubic symphysis to floor divided by height equals 0.64.
- Preserve the reference model identity while standardizing the body to these proportions.
- Keep neutral product views anatomically proportional. In the creative-feature image only, controlled low angle, perspective, or unconventional poses may visually dramatize the garment's selling point, but must keep anatomy believable and must not mutate the actual body, face, or garment construction.
- Mention this lock in product risk notes and final image prompts.

## Styling Completion Rules

For non-full-body products such as pants, tops, jackets, coats, capes, vests, or separate skirts:

- Build a complete outfit using `references/styling-completion-rules.md`.
- Supporting garments, shoes, and accessories must be minimal and selected to flatter the target product.
- The target product remains the visual hero; supporting styling must not hide or alter its construction.
- Unless the user explicitly requests barefoot styling, the model must always wear suitable footwear.

## Non-Negotiable Output Rules

- Produce four images, all 3:4 vertical.
- Use the same model in all images.
- Use the same indoor shooting location, style, lighting, props, and seasonal mood across all images.
- Preserve the product garment exactly. Do not change silhouette, neckline, sleeve/strap design, length, hem, seams, ruffles, pleats, closures, fabric type, color family, or decorative details.
- Keep the images suitable for online womenswear sales: clear garment visibility, flattering but honest fit, realistic fabric, commercial lighting, no distracting props.
- Allow interaction with set elements only when it does not hide or distort the garment.
- Never make the model barefoot unless the user explicitly asks for barefoot styling.
- Avoid logos, watermark, visible prompt artifacts, text, unapproved or distracting extra garments, invented accessories, face masks, color blobs, and reference-image defects.

## Response Pattern Before Generation

When the user has not chosen a set style, respond with:

- Fused guide-based multimodal analysis: clothing category/basic silhouette, material physics, core product highlight/creative selling point, and core wearing mindset.
- Four-image ecommerce logic: what the guide's front image, back image, detail close-up image, and creative-feature image must each prove for this product.
- Styling completion plan for separates and non-full-body products, including footwear.
- Fixed model proportion lock: 1.68m height, 7.5-head ratio, 0.64 leg-length ratio.
- Product risk notes: details most likely to drift during generation.
- 2-3 indoor set style options: each with mood, props, light, why it fits the garment.
- A direct request for the user to choose one option or provide a custom style.

Do not write the final shooting script in the same turn as initial set recommendations unless the user already selected a set style.

## Response Pattern After Set Selection

After the user chooses or confirms the set style, respond with a shooting script instead of generating images. Use `references/shooting-script-guide.md` and follow its required output format:

- Section one: use the exact Chinese multimodal garment-attribute report title defined in `references/shooting-script-guide.md`.
- Section two: use the exact Chinese four-image ecommerce storyboard title defined in `references/shooting-script-guide.md`.
- The script table must have exactly the four Chinese row labels defined in `references/shooting-script-guide.md`, corresponding to front image, back image, detail close-up image, and creative-feature image.
- The script table must use exactly the five Chinese column labels defined in `references/shooting-script-guide.md`.
- Keep the fixed model proportion lock in the analysis and script content, but do not add extra table columns.
- A direct request for user confirmation before image generation.

Do not call `image_gen` until the user explicitly confirms the script or says to proceed.

## Response Pattern After Generation

After generating the first batch, keep the response focused but do not end the workflow:

- Name the four deliverables.
- Provide final saved paths if available.
- State that the workflow used the approved shooting script, GPT Image 2.0/built-in image generation prompting, and did not use the local fashion img2img skill.
- Ask whether the user is satisfied with the generated images or needs any corrections.

Do not ask about color variants until the user confirms the first batch is fully correct.

## Response Pattern For Color Variants

After the user confirms the first batch is fully correct and asks for color variants:

- Ask the user to upload product reference images for each additional color.
- For each color, identify the target color and preserve all non-color garment construction from the approved original workflow.
- Ask whether to keep the base set exactly the same or allow small color-matched prop/decor adjustments.
- If adjustments are allowed, propose small prop/decor changes only; do not change architecture, room identity, model identity, body proportions, garment style, or four-shot script structure.
- Generate four 3:4 images per confirmed color using GPT Image 2.0/image_gen and the same approved script structure.

## References

- `references/garment-analysis.md`: use to extract exact product construction and invariants.
- `references/shooting-script-guide.md`: primary analysis and script reference; use it from the first product-analysis step and again after set selection to create the four-shot script for user confirmation.
- `references/indoor-set-styles.md`: use to recommend or validate indoor shoot styles after guide-based product-attribute thinking.
- `references/prompt-templates.md`: use to write the four final image prompts.
- `references/color-variant-workflow.md`: use after the user confirms the first batch is fully correct and wants additional color variants.
- `references/styling-completion-rules.md`: use whenever the product is not a complete full-body look or needs supporting garments/footwear.
