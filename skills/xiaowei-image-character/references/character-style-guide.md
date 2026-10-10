# Standalone Character Style Guide

Use this guide and the adjacent `xiaowei-master-v1.png` when the full repository is unavailable. Resolve both relative to the installed skill folder.

## Identity and priority

Match the actual master image first: mint-green short bob, curved bangs, outward side locks and one upward ahoge; emerald eyes and peach blush; cream-white hoodie with mint hood/cuffs/hem; white pleated skirt with mint piping; cream socks and mint sneakers; cream speech-bubble hair clip with green outline and three green dots; rounded mint pouch and warm-yellow star charm.

Keep the clip on the character physical left (viewer right in a frontal view). Preserve the master pouch construction and strap orientation. Use the reference proportions rather than imposing the initial approximate 2.5-head-tall text target. Closed-eye expressions do not require iris highlights.

Use soft pastel anime illustration, clear dark-green contours and gentle shadows. Vary pose, emotion, framing and scene by default. Accept explicit outfit, style or redesign requests as labeled variants. Do not claim this is an official product character.

Approximate prompt palette: mint `#8EDBC2`, deep mint `#238B6B`, cream `#FFF7E8`, pale gray-green `#E9F0ED`, yellow `#FFD56A`, peach skin `#FFE1D1`. These are design targets, not measured master swatches; image colors take priority.

## Copy-ready general template

Upload the actual bundled master image together with this prompt. Replace bracketed task fields with one specific request.

```text
Use the attached Xiao Wei master image as the authoritative identity reference. Reproduce the same unofficial fan-made character, not a new design. Match the master face, emerald eyes, mint bob, segmented curved bangs, outward side locks and upward ahoge, actual proportions and palette. Preserve the cream-white hoodie with cream sleeves and mint hood/cuffs/hem, white pleated skirt with mint edge, cream socks, mint sneakers, cream speech-bubble hair clip with green outline and three green dots, mint crossbody pouch and yellow star charm. Keep the clip on the same physical side of the character.

OUTPUT: exactly one illustration.
ACTION / EXPRESSION: [one specific pose and emotion].
COMPOSITION: [full body or explicitly requested portrait, aspect ratio, camera view].
BACKGROUND: [simple setting, flat white background or true transparency if supported].

Change only the requested action, expression, framing or background. Keep the reference identity and costume. Use polished pastel 2D chibi anime art, clear dark-green contours, soft shading and a readable silhouette. Avoid extra characters, unrelated props, logos, watermark, accidental lettering, duplicated accessories or limbs. Keep safe margins around all visible body parts. Do not inherit a sticker halo unless a sticker border is requested.
```

## Clean isolated character addendum

Use this with the general template for UI/game assets, not sticker sheets.

```text
Output one isolated full-body character with the entire hair silhouette, both hands and both feet inside generous safe margins. Use a genuinely transparent background only if supported; otherwise use a flat pure-white background and state that removal is still required. Do not add a white sticker border, outer colored stroke, glow, halo, floating symbols, drop shadow or ground shadow. Preserve only the established hair clip, pouch and star charm. Prioritize clean natural contours and fidelity to the master over reinterpretation.
```

Verify the alpha pixels and inspect edges on both dark and light backgrounds. A PNG filename alone does not imply transparency. Do not claim successful generation if the environment only returned a prompt.

## Provenance and license

Credit: **小微角色创作工具包项目维护者与贡献者 / Xiaowei Character Kit maintainers and contributors**.

This skill instruction text, guide and bundled reference image are offered under **Creative Commons Attribution 4.0 International (CC BY 4.0)**, to the extent the licensors hold the relevant rights. Copying, modification, redistribution and commercial use are permitted subject to the formal terms in the adjacent [LICENSE.txt](LICENSE.txt).

Provide appropriate credit, a license link (<https://creativecommons.org/licenses/by/4.0/>), the project source (<https://github.com/CoconutHR/xiaowei-character-kit>) and a modification notice. No ShareAlike or noncommercial restriction is added. Character consistency requirements are task defaults, not extra license terms.

The project is unofficial. No third-party trademark permission or endorsement is granted. AI-output rights and service terms depend on applicable law and actual generation context; no warranty of exclusive copyright or noninfringement is provided. The master was supplied by the maintainer as an AI-generated image. Exact generation settings and postprocessing history were not recorded. The reported model label is not a verified API identifier.
