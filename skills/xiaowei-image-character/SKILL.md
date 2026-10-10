---
name: xiaowei-image-character
description: Create or revise illustrations, expressions, poses, stickers, avatars and comics of the unofficial Xiaowei mascot using a bundled master image, while preserving the project visual identity and reporting asset limitations.
agent_created: true
---

# Xiaowei Image Character

## Purpose

Create consistent, non-official fan illustrations. Use this skill for character references, expressions, actions, assistant states, stickers, avatars, themed art or comic panels. Do not imply affiliation with WeChat, Tencent or any model provider. Treat consistency rules as default task and repository acceptance criteria, not additional restrictions on CC BY 4.0 adaptations.

## Load the correct references

1. Resolve paths relative to this `SKILL.md` directory, not the shell working directory.
2. In the full repository, read `../../CHARACTER_SPEC.md`, `../../assets/reference/README.md` and the relevant section of `../../prompts/xiaowei-character-prompt-kit.md`. Use `../../assets/reference/xiaowei-master-v1.png` as the primary visual reference.
3. In a standalone installation, read `references/character-style-guide.md` and view the bundled `references/xiaowei-master-v1.png`. Use the two copy-ready templates in the style guide if the full prompt pack is absent.
4. Add the repository turnaround or detail board only when relevant to the requested angle or costume detail. Prioritize the master over auxiliary images and text if they disagree.
5. If neither master image exists or the runtime cannot view/upload it, request the image or clearly state the reference limitation; do not claim text alone ensures character identity.

## Identity anchors

- Preserve a short mint-green bob, curved segmented bangs, outward side locks and one curved upward ahoge.
- Preserve an emerald-eyed rounded chibi face, soft highlights and peach blush; allow naturally closed eyes in expressions.
- Preserve a cream-white hoodie with cream sleeve bodies and mint hood/cuffs/hem, a white pleated skirt with mint edge, cream socks and mint sneakers.
- Preserve a cream speech-bubble hair clip with green outline and three green dots on the character left side (viewer right in a frontal view).
- Preserve a rounded mint crossbody pouch and warm-yellow star charm in the master shape; allow natural occlusion in close-ups or rear views.
- Match the actual master proportions and colors instead of forcing the initial approximate 2.5-head-tall target or uncalibrated color swatches.

## Workflow

1. Identify the output: reference sheet, expression, pose/state, sticker, avatar, isolated character, illustration or comic.
2. Confirm or state practical defaults for quantity, aspect ratio, crop, background, transparency and outfit variation. Preserve the base outfit unless variation is requested. Request clarification when an ambiguous choice affects the result materially.
3. Attach the master as an actual reference input when the available generator supports it. Do not merely mention a filename and assume the generator can see it.
4. Adapt the closest repository prompt or standalone template. Specify exactly what may change and what must remain fixed. Explicitly state rows and columns for sheets.
5. For one standalone sticker or UI asset, request exactly one image, generous margins and the desired border policy. Do not inherit master sticker glow when a clean UI asset is requested.
6. If direct generation is unavailable, return a complete copy-ready prompt, required image inputs and intended dimensions/background; do not promise a file that was not created.
7. Inspect identity, anatomy, clip side, accessories, layout, crop, actual transparency and edge quality after generation. Distinguish an alpha channel from actual transparent pixels and from white borders/halos.
8. Record source/reference version, creator credit, reported model label, known settings, prompt and manual edits. Mark unrecorded settings as unknown rather than inventing seeds or exact reproduction history.

## Existing asset limitations

Treat expression, action, state, sticker and prop sheets as unsplit reference boards, not independent PNGs or animation frames. Describe the actual layouts: expressions 3 rows/4 columns, actions 2 rows/4 columns, states 2 rows/3 columns, stickers 3 rows/3 columns and props 2 rows/4 columns. Check state symbols visually instead of promising exact UI status mapping. Treat the existing themed illustration as a square transparent composition, not an exported 16:9 splash screen. Do not assume the avatar is a multi-platform icon bundle.

## Preservation and licensing

- Never overwrite the master or original reference boards with generated variants. Save derivatives separately and record transformations.
- Never modify a user-designated read-only source directory; copy selected files only into an authorized output directory.
- License the supplied project content under CC BY 4.0, allowing adaptations and commercial use with attribution, license link and modification notice. Preserve the notices in `references/character-style-guide.md` and formal text in `references/LICENSE.txt` when distributing this standalone skill.
- Do not imply third-party trademark permission, official endorsement, guaranteed copyright protection of AI output or blanket permission for newly introduced third-party material.
- Treat `GPT Image 2.5 Sunburst` as a maintainer-reported label, not a verified API model ID or runtime capability.

## Deliver

Provide a concise result or complete prompt with reference inputs, framing, background, allowed variation and any unresolved quality limits. For repository contributions, add accurate provenance, settings and license records. Do not claim to have generated, validated or published assets without actually doing so.
