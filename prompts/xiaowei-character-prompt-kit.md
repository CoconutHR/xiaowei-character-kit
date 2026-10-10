# 小微非官方拟人形象：参考图生图提示词包

> 内容许可：CC BY 4.0，署名“小微角色创作工具包项目维护者与贡献者”。模型名称 `GPT Image 2.5 Sunburst` 是维护者在原对话中的平台显示标签，未独立验证，不作为可直接调用的 API 模型标识。
>
> **已有母图：** 本项目的 `assets/reference/xiaowei-master-v1.png` 即初始提示词中所称 `XiaoWei_Master.png`。复现现有角色应上传该母图，再选 Prompt 02–12；Prompt 01 仅保留初始设计流程，不用于重新定义当前角色。
>
> **优先级：** 母图 > 辅助图 > 文字与近似色值。约 2.5 头身及双高光是初始设计目标，不覆盖母图实际比例或闭眼表情。标准复现要求不是限制 CC BY 4.0 改编的许可条款。
>
> **现有素材：** 表情板 4 列 × 3 行，动作板 4 列 × 2 行，状态板 3 列 × 2 行，贴纸板 3 列 × 3 行，道具板 4 列 × 2 行；全部未拆分。主题插画实际为方形而非 Prompt 10 的 16:9。完整索引见项目 `assets/reference/README.md`；关联提示词不是逐图精确生成记录。

> 方向：原创二创概念角色，不冒充官方形象。核心气质是「住在聊天气泡里的薄荷绿小助手」：可爱、可靠、行动派，偶尔有一点小傲娇。
>
> **核心工作流：先生成并选定一张主参考图，再把它作为图片参考附加到所有后续生成任务中。** 仅靠文字重复描述，很难让角色每次都完全一致。

## 1. 角色圣经（固定设定）

建议将以下设定视为不可随意变更的角色规范：

- **名字**：小微 / Xiao Wei
- **定位**：聊天与生活服务 AI 助手的拟人吉祥物
- **比例**：以已定稿母图实际比例为准；初始设计目标约 2.5 头身，大头、小身体，轮廓简洁
- **发型**：薄荷绿短波波头，整齐但略有层次的齐刘海，两侧各有一缕微微上翘的发束
- **眼睛**：清透的翡翠绿大眼睛，固定双高光；脸颊淡淡的蜜桃色腮红
- **服装**：奶油白宽松连帽卫衣，薄荷绿帽里、袖口和下摆；简洁的白色百褶短裙，裙边有一圈薄荷绿细线；奶油白短袜、薄荷绿运动鞋
- **识别配件**：角色自身左侧（正面看为观者右侧）有奶油白圆角聊天气泡发夹，绿边与三个绿点；斜挎圆润薄荷绿任务包，挂着母图造型的暖黄色小星星
- **标志性视觉元素**：一个半透明的薄荷绿小聊天气泡，里面有一颗暖黄色小星星
- **性格**：热心、机灵、效率高、略带小傲娇；接任务时认真，完成任务时会小小得意
- **配色**：薄荷绿 `#8EDBC2`、深薄荷绿 `#238B6B`、奶油白 `#FFF7E8`、浅灰绿 `#E9F0ED`、暖星黄色 `#FFD56A`、蜜桃肤色 `#FFE1D1`
- **画风**：高完成度 2D anime chibi 插画；干净流畅的深绿色线稿；轻柔赛璐璐阴影；低噪点、柔和粉彩色、形状圆润、轮廓清晰
- **品牌边界**：聊天气泡是原创通用造型；不要照搬微信标志、二维码、真实 app 界面或其他现成角色的设计

## 2. 生成规则：怎样最大限度保持一致

1. 第一张图只生成**一个角色、一个视角、全身、白底**，不要一开始就要求多视图或复杂场景。
2. 从第一张图中选定最满意的一张，命名为 `XiaoWei_Master.png`。以后所有提示词都附上这张图作为图片参考。
3. 如果某次输出改变了刘海、眼睛颜色、卫衣结构、裙边、发夹或斜挎包，就继续以主参考图重新生成，不要把偏离的输出升级为新标准。
4. 一次生成一个任务、一个成品。如果需要透明贴纸或正式游戏资源，最好每张单独生成；九宫格适合做设计草案，不适合直接当作九张独立素材。
5. 如果生成器支持设置参考图强度、角色一致性或种子：保持主参考图和相关设置不变；多张同系列图片尽量沿用同一组参数。
6. 生成图中不要要求排版文字。需要标题、标签、状态名称时，后期用设计工具添加，避免文字乱码。

## 3. Prompt 01：第一次确定主造型（不附参考图）

**用途：** 生成第一张角色母图。这个阶段最重要的是全身轮廓、配色和识别配件，不要追求复杂背景。

```text
Create an original character concept for “Xiao Wei”, a cute fictional AI assistant mascot inspired by the idea of a helpful chat companion. This is an original fan-made concept, not an official brand mascot.

Show exactly ONE character in a full-body, front three-quarter view, standing in a relaxed friendly pose, centered on a clean pure-white background. Make the complete silhouette easy to read, with comfortable white space around the character. No extra characters, no panels, no text, no watermark.

CHARACTER DESIGN — keep every detail clear and memorable:
- Super-deformed 2.5-head-tall chibi anime proportions, a large expressive head and a small compact body.
- Short fluffy mint-green bob haircut, neat piecey bangs, two tiny slightly upturned side locks.
- Large clear jade-green eyes with two consistent catchlights in each eye, soft peach blush, warm friendly smile.
- An oversized cream-white hoodie with cream-white sleeve bodies and mint-green hood, cuffs and hem.
- A simple white pleated skirt with a thin mint-green edge, cream ankle socks and mint-green sneakers.
- One original cream-white rounded speech-bubble hair clip with a mint-green outline and three green dots, on the character’s left side (viewer’s right).
- A small rounded mint-green crossbody utility pouch, with one tiny warm-yellow star charm.
- A single small translucent mint speech bubble with a warm-yellow star may float beside her as her signature motif.

COLOR PALETTE: mint green #8EDBC2, deep mint #238B6B, cream white #FFF7E8, pale gray-green #E9F0ED, warm star yellow #FFD56A, peach skin #FFE1D1. Keep the palette limited and harmonious.

ART STYLE: polished 2D anime chibi illustration, clean dark-green line art, soft cel shading, smooth rounded shapes, gentle pastel colors, crisp silhouette, professional mobile-game mascot quality. Cute, approachable, clever, energetic and reliable, with a tiny hint of playful confidence.

DESIGN PRIORITIES: recognizable silhouette, simple shapes that remain readable at small sizes, consistent costume construction, clear separation between hair and clothing, appealing face, production-friendly design.

Avoid photorealism, 3D rendering, overly glossy plastic, excessive gradients, complicated lace, excessive accessories, huge weapons, sexualized styling, harsh shadows, busy background, logos, readable lettering, watermarks, signature marks, extra fingers, malformed hands, duplicated accessories, multiple versions of the character.
```

## 4. Prompt 02：标准角色设定三视图（附主参考图）

**用途：** 统一正面、侧面、背面设计，方便之后画动作或交给美术制作。附上 `XiaoWei_Master.png`。

```text
Use the attached image as the authoritative identity reference for Xiao Wei. Reproduce the exact same character, not a redesign. Preserve the same face, eye color and highlights, mint bob haircut and bangs, speech-bubble hair clip, hoodie, skirt, shoes, crossbody pouch, star charm, proportions and palette.

Create a clean professional CHARACTER TURNAROUND SHEET on a plain white background. Show exactly three full-body views of the same character, aligned at the same scale and baseline:
1. straight front view,
2. exact left-side profile,
3. straight back view.

Keep the body proportions identical across all three views. Make the side profile genuinely side-on and the back view genuinely rear-facing. Clearly show how the hood, sleeves, skirt hem, pouch strap, pouch and hair clip look from each angle. The speech-bubble hair clip stays on the same physical side of the character in every view. Neutral relaxed standing pose, arms slightly away from the torso so the outfit silhouette remains visible.

Polished 2D chibi model sheet, clean dark-green line art, soft cel shading, flat consistent lighting, restrained pastel palette, precise construction and easy-to-read silhouette. Equal spacing, no overlap between views.

Do not add a fourth view, alternate outfits, facial-expression variations, props in the hands, scenery, labels, measurements, logos, text, watermark or decorative frame. Do not change or embellish the design. One character model repeated in three views.
```

## 5. Prompt 03：头部、服装与配件细节板（附主参考图）

**用途：** 固定脸部画法、发夹和包包等易漂移细节。

```text
Use the attached Xiao Wei master image as the strict character reference. Do not redesign any feature.

Create a neat CHARACTER DETAIL REFERENCE BOARD on a pure-white background. Arrange a few clear, separate studies with generous spacing:
- one large straight-on head portrait,
- one three-quarter head portrait,
- one close-up of the cream-white speech-bubble hair clip with a mint outline and three green dots,
- one close-up of the rounded mint utility pouch and its tiny yellow star charm,
- one close-up of the cream hoodie fabric, mint cuffs and skirt piping,
- a row of six simple flat color swatches matching the character palette.

All details must match the attached reference exactly: same mint bob and bangs, same jade-green eyes and double catchlights, same blush, same hoodie construction, same hair clip, same pouch and star charm. Use simple callout-like arrangements but NO written labels or lettering.

Clean 2D anime character-design artwork, crisp line art, soft cel shading, consistent studio lighting, flat white background, high readability. These are reference studies of one existing design, not alternate designs.

No new accessories, no different hairstyle, no color changes, no logos, no watermark, no decorative background, no illegible text, no extra characters.
```

## 6. Prompt 04：面部表情表（附主参考图）

**用途：** 让角色在不同情绪下仍然像同一个人。先生成表情表，再按需要单独扩展某个表情。

```text
Use the attached Xiao Wei master image as the strict identity reference. Preserve the exact same head shape, mint bob haircut, bangs, jade-green eyes, double eye highlights, speech-bubble hair clip, skin tone and line-art style.

Create a clean 4-by-3 EXPRESSION SHEET containing exactly 12 separate head-and-shoulders portraits of the same character. Every cell has the same crop, scale and plain white background. Only the facial expression and small head tilt may change; the hairstyle, accessories, face proportions and colors must remain identical.

Expressions in reading order, left to right and top to bottom:
1. calm friendly neutral,
2. bright open smile,
3. cheerful closed-eye laugh,
4. focused and determined,
5. thinking with eyes looking slightly upward,
6. surprised with widened eyes,
7. gently listening with a slight head tilt,
8. confused with one raised eyebrow,
9. proud and a little smug,
10. embarrassed with stronger blush,
11. worried but trying to help,
12. relieved and happy after completing a task.

Polished 2D chibi anime expression reference, clean dark-green line art, soft cel shading, consistent pastel palette, readable emotions at small icon size. Keep each portrait fully inside its own cell and do not let any portrait overlap another.

No captions, no numbers, no text, no extra characters, no costume changes, no different eye colors, no hairstyle changes, no watermark, no borders that obscure the drawings.
```

## 7. Prompt 05：动作与姿态设定表（附主参考图）

**用途：** 给动态头像、宣传图、动画关键帧或表情包提供姿势参考。

```text
Use the attached Xiao Wei master image as the strict identity and costume reference. Keep her design unchanged: mint bob, jade-green eyes, cream-and-mint hoodie, white pleated skirt with mint edge, cream socks, mint sneakers, speech-bubble hair clip, crossbody pouch and tiny star charm.

Create a clean ACTION POSE SHEET in exactly 2 rows and 4 columns, with exactly eight full-body versions of the same character, each in its own evenly spaced area on a plain white background. Keep the same 2.5-head-tall proportions, outfit, palette and face design in every pose. Make each pose readable and physically coherent, with no overlap between characters.

Poses in reading order:
1. friendly two-handed greeting,
2. listening carefully with one hand near her ear,
3. thinking with one finger lightly touching her chin,
4. presenting a floating mint chat bubble with a yellow star,
5. checking a small blank task card,
6. energetically hurrying forward with her pouch bouncing slightly,
7. celebrating a completed task with a small fist pump,
8. apologetically explaining a small problem with a gentle worried expression.

Polished 2D anime chibi game-character reference sheet, clean dark-green line art, soft cel shading, consistent proportions and lighting, simple readable gestures and clear silhouettes.

No text, no UI screenshots, no brand logos, no new outfit pieces, no extra people, no duplicate limbs, no merged poses, no cropped feet, no watermark, no detailed scenery.
```

## 8. Prompt 06：AI 助手状态图（附主参考图）

**用途：** 用作应用中的待机、聆听、思考、执行、成功和需要帮助等状态图。状态差异主要通过表情和气泡符号表达，不靠文字。

```text
Use the attached Xiao Wei master image as the strict character reference. Preserve the same character identity, body proportions, hairstyle, clothing, palette and accessories in every panel.

Create an ASSISTANT STATE SHEET in exactly 2 rows and 3 columns on a clean white background, showing six separate waist-up illustrations of the same character, same scale and same framing. Each state has one small floating mint speech bubble as a secondary visual indicator. Keep the visual language simple enough for a mobile app.

States in reading order:
1. IDLE: relaxed posture, gentle smile, one tiny star in the bubble.
2. LISTENING: attentive expression, slight head tilt, two small sound-wave arcs beside the bubble.
3. THINKING: thoughtful gaze, three tiny dots inside the bubble, no written words.
4. WORKING: focused expression, a simple circular progress motif made of dots around the bubble; no percentages or text.
5. SUCCESS: bright smile, tiny yellow star burst in the bubble.
6. NEEDS ATTENTION: kind, mildly concerned expression, a small amber dot beside the bubble; not alarming or scary.

Make each state visually distinct but unmistakably the same character. Polished 2D chibi illustration, clean dark-green line art, soft cel shading, pastel palette, consistent crop and lighting, plain white background.

No real app UI, no words or letters, no numbers, no logos, no watermark, no dramatic warning signs, no costume or hairstyle changes.
```

## 9. Prompt 07：九宫格贴纸草案（附主参考图）

**用途：** 先探索贴纸表情。生成后挑选满意格子，再逐张单独生成高清版本。

```text
Use the attached Xiao Wei master image as the strict identity reference. Preserve her exact appearance and outfit.

Create a 3-by-3 grid of nine cute chat stickers featuring the same Xiao Wei chibi mascot. Each sticker must be a separate, fully visible composition with generous clear spacing; no sticker may overlap another. Use a clean white background and a consistent thick-but-neat mint-green outer sticker contour. The character should occupy most of each cell.

Sticker concepts in reading order:
1. waving hello,
2. nodding eagerly,
3. thinking with tiny floating dots,
4. typing rapidly on a tiny generic device,
5. holding up a yellow star to celebrate,
6. giving a gentle thumbs-up,
7. hiding half her face behind the pouch in embarrassment,
8. apologetically bowing her head,
9. curled up beside a floating chat bubble, sleepy but content.

Consistent polished 2D anime chibi art, clear expressions, simple shapes, pastel mint-and-cream palette, crisp outlines, charming messenger-sticker energy. Keep hands, face, hair clip and pouch cleanly drawn.

Do not include words, captions, speech text, numbers, logos, watermarks or backgrounds beyond plain white. Do not change her hairstyle or clothes. Avoid cropping ears, hair, hands, feet or sticker outlines.
```

### 单张贴纸扩展模板（每次只替换方括号里的内容）

```text
Use the attached Xiao Wei master image as the strict identity reference. Create ONE standalone chat sticker only, featuring the same Xiao Wei with exactly the same face, mint bob haircut, jade-green eyes, cream-and-mint hoodie, white pleated skirt, hair clip, pouch and yellow star charm.

ACTION / EMOTION: [写一个明确动作和情绪，例如 “a cheerful two-handed wave, bright smile”].

Composition: one full character, centered, clear silhouette, no cropping, expressive readable gesture, thick clean mint-green sticker outline, isolated on a plain white or transparent background if supported. Polished 2D chibi anime sticker, soft cel shading, pastel palette, crisp line art.

No words, no captions, no extra characters, no logos, no watermark, no redesign, no unnecessary props. Leave generous margin around the sticker.
```

## 10. Prompt 08：头像 / 应用图标（附主参考图）

**用途：** 社交头像、小微入口图标、启动器图标概念。图形本身不依赖文字。

```text
Use the attached Xiao Wei master image as the strict identity reference. Preserve her exact mint bob haircut, jade-green eyes, hair clip and cream-and-mint outfit.

Create a polished SQUARE MASCOT AVATAR ICON. Frame Xiao Wei from the chest up, facing slightly toward the viewer with a warm confident smile. Her face should be large and instantly recognizable at very small sizes. Place one simple translucent mint speech bubble and a tiny warm-yellow star behind her shoulder, without covering her face.

Use a simple softly rounded pale cream background with a subtle mint halo. Strong central composition, balanced negative space, clear silhouette, no tiny decorative details. Polished 2D anime chibi illustration, clean line art, soft cel shading, restrained pastel colors, professional mobile-app icon concept.

No text, no letters, no app name, no exact WeChat logo, no watermark, no border, no extra characters, no hairstyle or costume changes. Keep all important elements inside a safe margin for a square crop.
```

## 11. Prompt 09：透明背景单角色素材（附主参考图）

**用途：** 需要后续放进 UI、海报或游戏里的单独角色图。若模型不稳定地产生透明底，先用纯白底生成，再用抠图工具去背。

```text
Use the attached Xiao Wei master image as the strict identity reference. Recreate the same character without redesigning her.

Generate ONE full-body Xiao Wei character asset in [指定姿势，例如 “a relaxed friendly standing pose”]. Front three-quarter view, full head and both feet visible, arms and accessories separated clearly from the body, no overlap that would make background removal difficult.

Plain pure-white background or transparent background if supported. Even soft lighting, clean closed outlines, crisp edges, minimal soft shadow directly beneath the feet only. Polished 2D chibi anime game asset, consistent mint-and-cream palette, clean dark-green line art, soft cel shading.

This is a production asset, not a poster or character sheet. No scenery, no props beyond her established hair clip, pouch and star charm, no text, no logo, no watermark, no frame, no cropped body parts, no extra characters.
```

## 12. Prompt 10：主题插画 / 启动画面（附主参考图）

**用途：** 宣传海报、社交媒体配图、应用启动页。此类图可以有环境，但角色造型不能变化。

```text
Use the attached Xiao Wei master image as the strict character identity reference. Keep her face, hairstyle, proportions, outfit, hair clip, pouch and color palette unchanged.

Create a charming horizontal 16:9 key illustration of Xiao Wei, the helpful mint-green chat assistant mascot. She stands slightly right of center, smiling and presenting a glowing translucent mint speech bubble containing a small warm-yellow star. Around her float a few simple abstract message cards, tiny stars and rounded geometric shapes, suggesting that she is helping organize everyday tasks. Keep the elements generic and symbolic, not a real app interface.

The atmosphere is bright, welcoming, clever and gently magical. Use a soft cream background with mint-green gradients and a few pale aqua accents. Preserve plenty of clean negative space on the left for a title to be added later, but do not render any text.

Polished 2D anime chibi illustration, clean line art, soft cel shading, smooth shapes, controlled lighting, tasteful depth and clear focal hierarchy. Xiao Wei remains the strongest visual focus.

No real logos, no readable text, no watermark, no extra characters, no change to her established design, no busy UI mockups, no photorealism, no 3D render.
```

## 13. Prompt 11：原创小道具素材板（附主参考图）

**用途：** 建立角色周边的统一图形语言。可以做 UI 装饰、贴纸配件或轻量游戏资源。

```text
Use the attached Xiao Wei master image as the style and palette reference. Do not include the full character in this image.

Create a clean asset sheet of eight original small mascot props associated with Xiao Wei, arranged in exactly 2 rows and 4 columns, evenly spaced on a pure-white background:
1. a simple rounded mint chat bubble,
2. a warm-yellow four-point star,
3. a small rounded mint utility pouch,
4. a blank cream task card with a mint checkmark symbol,
5. three small thinking dots,
6. a simple mint circular progress motif,
7. two gentle sound-wave arcs,
8. a tiny cream-and-mint sneaker charm.

Every asset should use rounded geometry, a consistent dark-green outline, soft cel shading and the same restrained mint, cream, pale gray-green and warm yellow palette as the reference. Keep each item isolated with generous spacing and a clean readable silhouette. These are original generic symbols, not copies of an existing app icon set.

No written labels, no letters, no numbers, no brand logos, no watermark, no scene, no gradients that reduce legibility, no overlapping props.
```

## 14. Prompt 12：后续二创通用模板

**用途：** 想让小微做新动作、穿主题服装或进入新场景时，用这个模板；最稳妥的是只改动作和场景，先不要改服装。

```text
Use the attached Xiao Wei master image as the authoritative character reference. The attached image has priority over any incidental interpretation of the text. Keep Xiao Wei unmistakably the same character: same mint-green bob, bangs and curved upward ahoge, jade-green eyes with the reference highlights when open, same face proportions, cream-white speech-bubble hair clip with a green outline and three green dots, cream-white hoodie with cream sleeve bodies and mint hood/cuffs/hem, white pleated skirt with mint piping, cream socks, mint sneakers, rounded mint crossbody pouch and tiny yellow star charm. Match the actual proportions and pastel palette of the master image; do not force a numeric head-to-body ratio that contradicts the reference.

NEW SCENE OR ACTION: [清晰描述一个动作、情绪或环境。]

COMPOSITION: [描述构图、镜头远近、角色位置、画面比例。]

BACKGROUND: [描述简单背景；如果要做可抠图素材，写 “plain pure-white background, isolated character”.]

STYLE: polished 2D anime chibi illustration, clean dark-green line art, soft cel shading, rounded readable shapes, consistent pastel colors, production-friendly design.

IDENTITY LOCK: by default, change only the requested action, expression, camera framing or background. Preserve the face, hairstyle, costume, accessories, actual master proportions and color palette. If the NEW SCENE OR ACTION explicitly requests an alternate outfit, art style or redesign, allow only those stated changes and identify the result as a variant; otherwise retain the base design. Keep the speech-bubble hair clip on the same physical side for standard reproductions. Keep the pouch and star charm present unless they are naturally out of frame or their change is explicitly requested.

No text, no captions, no watermark, no real brand logos, no unrelated character designs, no unrequested accessories or costume drift, no extra fingers or limbs, no cropped body parts unless the framing explicitly requests a close-up.
```

## 15. 建议的生成顺序

### 第一阶段：把角色定下来
1. Prompt 01：生成 3–6 个候选版本，每次只出一张；选出最满意的全身图。
2. 将定稿保存为 `XiaoWei_Master.png`，之后不要随便替换。
3. Prompt 02：生成三视图；检查背面、侧面细节是否合理。
4. Prompt 03：生成细节板，确认发夹、眼睛、服装和包包没有漂移。

### 第二阶段：让角色可复用
5. Prompt 04：表情表。
6. Prompt 05：动作表。
7. Prompt 06：AI 状态表。
8. Prompt 07：贴纸草案；再用单张贴纸模板逐一重做选中的贴纸。

### 第三阶段：做成品素材
9. Prompt 08：头像或图标。
10. Prompt 09：需要独立使用的角色 PNG。
11. Prompt 11：道具素材。
12. Prompt 10：最后再做宣传图、启动图或场景图。

## 16. 无白边单角色修正模板（附母图）

母图是身份参考，不代表后续每张图都要继承贴纸描边。若目标是干净的 UI 或游戏单角色素材，在 Prompt 09 后加上以下段落，并明确上传母图；不得在没有透明工具支持时虚称已输出透明图片。

```text
Use the master image for character identity, not for the sticker border or floating decoration. Preserve the exact face, mint-green bob and ahoge, emerald eyes, cream-white hoodie with mint hood/cuffs/hem, pleated skirt, sneakers, cream speech-bubble hair clip with three green dots, crossbody pouch and yellow star charm.

Output exactly one full-body isolated character in the requested pose, with generous safe margins around the hair, hands and both feet. Use a genuinely transparent background if the tool supports it; otherwise use a flat pure-white background and clearly state that background removal is still required.

Do not add a white sticker border, colored outer stroke, halo, glow, drop shadow, ground shadow, floating chat bubble, text, logo or extra decoration. The existing hair clip, pouch and star charm must stay. Use clean natural character contours and preserve the reference proportions. Prioritize fidelity over reinterpretation.
```

透明通道、白色描边与光晕是不同概念。处理后仍需在深色与浅色背景下检查边缘；原图不覆盖，修正结果另存为派生版本并记录修改。

## 17. 生成质量检查清单

每次准备保留一张图之前，检查：

- [ ] 刘海形状和薄荷绿短波波头是否一致？
- [ ] 眼睛是否保持翡翠绿和相同的双高光？
- [ ] 聊天气泡发夹是否在正确一侧，形状是否一致？
- [ ] 卫衣是否仍然是奶油白主体、薄荷绿细节？
- [ ] 白色百褶短裙的薄荷绿裙边是否保留？
- [ ] 斜挎任务包和黄色小星星是否存在且位置合理？
- [ ] 头身比例和线稿风格是否与主参考图一致？
- [ ] 有没有擅自出现品牌标志、乱码文字或额外装饰？
- [ ] 如果是素材图，边缘是否干净、是否留足安全边距、是否便于去背？

**最实用的原则：** 先用角色表确定“她是谁”，再制作“她会做什么”。每次扩展都保留同一张主参考图，优先只修改动作、表情和背景，不要同时改脸、发型、服装和画风。
