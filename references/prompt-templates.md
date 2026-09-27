# 7 大排版设计生图 Prompt 模板库 (Prompt Templates)

本文档提供 7 种排版风格的完整提示词装配模板。所有模板均包含：
- **占位符规范**：`{MAIN_TITLE}`（主标题）、`{SUB_TITLE}`（副标题）、`{ENGLISH_SLOGAN}`（英文口号/点缀词）、`{ACCENT_COLOR}`（点缀主色，默认 lime green / bright red）。
- **通用环境配置**：`clean white background with subtle engineering grid texture, high-end graphic design poster, premium typography art direction`。
- **画幅配置**：默认 `--ar 5:2`（X Articles 长文封面），推文可用 `--ar 16:9`。

---

## 模板 01: 色块聚焦堆叠风 (Color Block Stack)
> **参考图**：`assets/examples/01-color-block-stack.jpg`  
> **适用题材**：态度宣言、认知颠覆、防坑指南、极客金句  
> **排版结构法则**：
> - **纯平面正圆贴纸（无发光羽化）**：居中色块必须是**纯平面、锐利矢量边缘、无外发光、无渐变软晕**的浅绿/荧光马卡龙色圆盘；
> - **大字微破框张力**：上下两行大黑体汉字（`{MAIN_TITLE}`）的左右笔画**微微探出正圆边缘**，形成破框视觉冲击；
> - **缝隙紧凑小英文**：在两行紧凑汉字的水平接缝间嵌入一行整齐大写英文（`{ENGLISH_SLOGAN}`）。

```text
High-end Swiss typography poster, adhering strictly to the exact composition of the reference image. Centered on the canvas is a perfectly crisp flat solid circular disc in soft light pastel lime-green, featuring clean sharp vector edges with zero outer glow, zero blur, and no lighting gradient. Superimposed in the center are Chinese characters rendered in massive ultra-bold jet-black sans-serif font, vertically stacked in two lines with tight line spacing: top line "{TOP_TITLE_2CHARS}", bottom line "{BOTTOM_TITLE_2CHARS}". The horizontal width of the characters slightly overhanging beyond the left and right borders of the green circle. In the tight gap between the two lines, a single compact line of neat capitalized English "{ENGLISH_SLOGAN}". Pristine white background with subtle light-grey engineering grid notebook paper lines, modern minimalist graphic design poster --ar 5:2 --v 6.1
```

---

## 模板 02: 灵动曲线穿插风 (Line Weave)
> **参考图**：`assets/examples/02-line-weave.jpg`  
> **适用题材**：进阶跃迁、持续成长、产品思维、AI 工作流联动

```text
Sophisticated editorial typography graphic poster. In the center, horizontal single-line Chinese characters "{MAIN_TITLE}" in massive heavy black sans-serif font. Above the title, an elegant widely tracked small Chinese subtitle "{SUB_TITLE}". Below the title, a clean line of capitalized English text "{ENGLISH_SLOGAN}". A single continuous vibrant bright lime green 3D vector doodle ribbon curves gracefully, weaving in and out through the strokes of the main characters, passing partially in front and partially behind the black strokes to create 2.5D layer depth. Pristine white background with faint subtle technical grid texture, masterclass graphic design layout, crisp contrast, minimalist modern tech branding --ar 5:2 --v 6.1
```

---

## 模板 03: 刚柔双字体碰撞风 (Script Clash)
> **参考图**：`assets/examples/03-script-clash.jpg`  
> **适用题材**：审美随笔、独立开发心情、灵感手记、极客探索、工具干货

### 模式 03-A: 4 字单行居中版 (推荐用于 4 汉字标题，完美重心平衡)
> **排版结构法则**：4 个汉字保持**单行水平横向排列，居中显示**。红色连笔草书英文横向贯穿在 4 个大字的**正中心（垂直居中对齐）或中下部**。上方居中放置一行精致全大写英文标题，形成上下左右对称、重心极度均衡的现代设计感。

```text
High-end modern editorial typography poster, perfectly balanced and horizontally centered composition. In the center foreground, four Chinese characters "{MAIN_TITLE_4CHARS}" rendered in massive ultra-bold jet-black sans-serif font in a single horizontal line. An elegant flowing handwritten cursive script in vivid crimson red "{RED_SCRIPT_WORD}" is placed horizontally across the middle of the Chinese characters, perfectly centered vertically and horizontally, artfully intertwining with the black strokes. Centered directly above the main title, a neat line of spaced uppercase sans-serif English "{ENGLISH_SLOGAN}". Minimalist pristine white background with faint subtle engineering grid notebook paper texture, Swiss graphic design aesthetic, ultra-clean vector edges, powerful centered visual weight --ar 5:2 --v 6.1
```

### 模式 03-B: 5~6 字非对称错落版 (适用于 2+4 或 2+3 结构)
> **排版结构法则**：上行 2 汉字，下行 3~4 汉字，统一**向左对齐 + 倾斜 (Italic Slant)**。上行右侧留出的空缺区域，由 2 行紧凑全大写英文块填补。红色手写连笔草书横向跨越在两行大字的水平缝隙中，形成阶梯互补的视觉重心平衡。

```text
A sophisticated modern editorial typography poster adhering strictly to the layout structure of the reference image. The overall composition is balanced and centered. In the foreground, heavy solid black Chinese characters with an energetic forward italic slant, left-aligned in two lines: The top line has exactly 2 characters "{TOP_TITLE_2CHARS}"; the bottom line directly below has exactly 4 characters "{BOTTOM_TITLE_4CHARS}". Because the top line has only two characters, the upper-right empty corner above the bottom line is neatly filled with a small compact two-line uppercase sans-serif English text block "{ENGLISH_BLOCK}". Exactly in the horizontal gap between the top line ("{TOP_TITLE_2CHARS}") and the bottom line ("{BOTTOM_TITLE_4CHARS}"), an elegant flowing handwritten cursive script in vivid crimson red "{RED_SCRIPT_WORD}" is placed horizontally, overlapping the two lines in the middle gap. Pure white canvas with subtle light-gray engineering grid texture, high-end Swiss editorial graphic design, perfectly balanced rectangular visual weight --ar 5:2 --v 6.1
```

---

## 模板 04: 虚实线框超大衬底风 (Outline Underlay)
> **参考图**：`assets/examples/04-outline-underlay.jpg`  
> **适用题材**：时代风口、破浪前行、宏大视野、战略布局、新版本重磅发布  
> **排版结构法则**：
> - **背景超大线框贯穿全屏**：背景浅绿描边空心英文（`{MASSIVE_BG_WORD}`）尺寸必须**极其巨大，左右直接贴近画布边缘，上下贯通**；
> - **实心居中大字**：纯黑极粗主标题（`{MAIN_TITLE}`）居中叠在镂空线框正前方，产生强烈的虚实景深张力；
> - **底部宽距副标**：精致细字中文副标（`{SUB_TITLE}`）拉大字距居中置底。

```text
High-end typography digital banner poster, strictly following the layout and proportion of the reference image. In the center foreground, Chinese characters "{MAIN_TITLE}" displayed in massive ultra-bold solid jet-black sans-serif font. Directly beneath the title, an elegant small Chinese subtitle "{SUB_TITLE}" with wide letter spacing. In the background layer, spanning across the entire canvas width from the extreme left margin to the extreme right margin, a colossal hollow wireframe English word "{MASSIVE_BG_WORD}" drawn in crisp clean thin lime-green contour lines, creating dramatic spatial contrast between the solid black foreground and the gigantic wireframe background. Light-gray architectural grid paper background, perfectly balanced minimalist tech poster --ar 5:2 --v 6.1
```

---

## 模板 05: 东方呼吸竖排风 (Vertical Inset)
> **参考图**：`assets/examples/05-vertical-inset.jpg`  
> **适用题材**：深度长文、底层架构解析、哲学思考、代码美学、高质量沉淀  
> **排版结构法则**：
> - **等宽阔气留白**：4 个大汉字（`{MAIN_TITLE}`）单行横排，字间距拉大，呼吸感极强；
> - **拼音水平基线统一**：各汉字右上侧的垂直微缩拼音/英文，必须**统一定位在字符右上肩的相同水平基线高度**，字号微缩精致。

```text
High-end minimalist editorial graphic design poster, adhering strictly to the exact composition of the reference image. A single horizontal row of four Chinese characters "{MAIN_TITLE}" with wide generous spacing between each character, rendered in deep solid black architectural sans-serif font. In the negative space immediately to the upper right of each character, a tiny elegant vertical line of uppercase Romanized Pinyin: {VERTICAL_PINYIN_MAP}. All vertical Pinyin text blocks are perfectly aligned with identical vertical baseline and neat typography. Pure white background with faint subtle geometric graph paper grid, serene Japanese editorial design, masterclass spacing and visual rhythm --ar 5:2 --v 6.1
```


---

## 模板 06: 赛博机能波点 3D 胶囊风 (Halftone 3D Badge)
> **参考图**：`assets/examples/06-halftone-3d-badge.jpg`  
> **适用题材**：极客编程实战、AI Agent 攻坚、黑客竞赛、硬核工具、极限突破

```text
Futuristic techwear typographic poster design. Massive bold Chinese title "{MAIN_TITLE}" with an aggressive modern angular silhouette. The surface of the black characters is textured with a refined halftone dot pattern gradient fading from top to bottom. The characters feature a striking 3D offset extrusion drop-shadow in glowing electric lime green, creating intense cyber depth. Directly below the main title, a sharp slanted black parallelogram banner badge containing white inverted text "// {SLOGAN_BANNER} //". In the top right corner, neat dual-line techwear uppercase English "{ENGLISH_SLOGAN}". Light grey technical grid background, energetic high-contrast visual identity, cyber-athletic developer aesthetic --ar 5:2 --v 6.1
```

---

## 模板 07: 故障切片镜像抽离风 (Glitch Slice)
> **参考图**：`assets/examples/07-glitch-slice.jpg`  
> **适用题材**：先锋突破、颠覆性创新、思维破界、潮牌派对、前沿实验  
> **排版结构法则（严禁切割实心大字）**：
> - **实心大字完整无损**：中心黑体主标题必须是**100% 完整实心、无横截切线、饱满清晰**的黑色汉字（`{MAIN_TITLE}`）；
> - **上下线框微距切片（低高度）**：切割抽离的只是**描边线框（Outline Stroke）**，且仅截取顶部尖端（top 20~25% tips）向上微移、截取底部脚部（bottom 20~25% feet）向下微移，线框高度较小紧凑，绝不喧宾夺主；
> - **顶部超宽字距英文**：画布最上方排布一行极宽字距的小字全大写英文（`{ENGLISH_SLOGAN}`）。

```text
High-end minimalist editorial graphic design poster, strictly adhering to the exact composition and visual design of the reference image. In the center, Chinese characters "{MAIN_TITLE}" in massive heavy solid jet-black sans-serif font. The central black characters are completely solid, fully intact, and completely unbroken, with zero lines cutting through them. Positioned slightly above the solid black characters, there is a short, low-profile wireframe slice showing only the top tips (top 20-25% edge) of the characters drawn in crisp thin black outline. Positioned slightly below the solid black characters, there is a short, low-profile wireframe slice showing only the bottom feet (bottom 20-25% edge) of the characters drawn in crisp thin black outline. Both wireframe outline slices have low height. At the very top, a widely-spaced single line of uppercase sans-serif English "{ENGLISH_SLOGAN}". Pure white background with very faint subtle light-grey engineering graph paper grid, Swiss modernist typography, ultra-clean vector graphic art --ar 5:2 --v 6.1
```

