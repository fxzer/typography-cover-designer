# 排版设计规范与生图控制指南 (Layout Rules & Prompting Guidelines)

本文档定义了将 9 种平面文字排版技巧转化为 AI 生图（Midjourney / FLUX / Imagen / Qwen-Image）时的核心规则与参数标准。

---

## 1. 画幅比例与安全边距 (Canvas & Safe Margins)

### ① X (Twitter) Articles 封面标准
- **比例**：严格遵循 **5:2**（如 2500×1000 像素，对应 `--ar 5:2`）。
- **四周安全边距**：必须预留至少 15% 的四周安全区（Safe Zone），防止在 X 移动端列表、桌面端文章详情或个人主页 Pin 顶时被圆形头像或顶部信息遮挡。
- **生图工具内置比例**：若工具支持 16:9（如 `generate_image`），采用 16:9 构图并强化水平横向延展，中心保留 5:2 核心视觉带。

### ② X (Twitter) 推文单图配图
- **比例**：推荐 **16:9**（1920×1080）或 **3:2**（1500×1000）。

---

## 2. 9 种排版核心结构解构与 Prompt 关键词映射

| 技巧代号 | 中文技巧要素 | 核心 Prompt 英语控制词 | 空间景深层级 |
| :--- | :--- | :--- | :--- |
| **01 色块聚焦** | 上下双行大字、小字英文居中、圆形荧光色块 | `bold heavy sans-serif typography, vertically stacked two-line title, small capitalized English subtitle between lines, neon lime green circular backdrop glow, minimalist subtle grid paper background` | 底层：网格白底<br>中层：半透明高亮正圆色块<br>顶层：极黑粗体字 |
| **02 曲线穿插** | 单行横排大字、天地副标题呼应、荧光手绘曲线穿插 | `bold clean single-line Chinese characters, small neat subtitle above, small English title below, vivid bright lime green 3D doodle stroke curving in and out through the strokes of characters, dynamic weave, layer depth` | 底层：网格白底<br>交织层：前穿后插的荧光手绘绿线条<br>顶层：黑体字 |
| **03 刚柔碰撞** | 倾斜大字组、右上小字组、底层红色飘逸手写花体 | `italic dynamic heavy sans-serif typography, left-aligned, small elegant English block in top-right, large overlapping bright red expressive cursive script calligraphy behind the black characters, contrasting textures` | 底层：网格白底<br>穿插层：鲜红花体草书英文字<br>顶层：厚重几何斜黑体 |
| **04 虚实线框** | 居中实心大字、底部拉开字距副标、巨型镂空描边字 | `bold solid black center title, widely spaced thin subtitle below, massive semi-transparent hollow wireframe outline text in light neon green spanning across the entire background, visual contrast of solid vs wireframe` | 底层：网格白底<br>中景：超大比例镂空描边英文字<br>前景：居中纯黑大字 |
| **05 东方竖排** | 等宽横排留白、右侧负空间竖排拼音/微缩英文 | `widely tracked elegant Chinese title characters with generous negative space, tiny vertical inset typography in Pinyin/English neatly aligned next to each character right edge, Japanese editorial magazine grid layout` | 单层纯粹平面：通过极佳的字距与竖向微缩排版建立网格秩序与节奏感 |
| **06 机能波点** | 波点网点纹理、荧光绿3D硬阴影、斜切黑色胶囊条标语 | `bold techwear typography, black characters with halftone dot pattern gradient texture, vibrant lime green 3D offset hard extrusion drop-shadow, slanted black parallelogram badge banner below with white inverted slogan, cyber-athletic style` | 底层：网格底<br>投影层：荧光绿 3D 偏移硬投影<br>主体层：波点渐变字<br>挂载层：斜切胶囊徽章 |
| **07 故障切片** | 完整实心大字、上下低高度线框切片向外抽离推开、顶部超宽英文 | `bold centered solid black typography fully intact and unbroken, low-height upper wireframe slice showing only top tips shifted upward, low-height lower wireframe slice showing only bottom feet shifted downward, kinetic typography displacement, ultra-wide spaced top header` | 核心层：100% 完整实心大字主体（无切线）<br>动效层：上下抽离的浅高度空心轮廓切片<br>引导层：顶部超宽字母组 |
| **08 荧光划线** | 单行粗黑大字、底部鲜黄色波浪/直线划线、右上微标对齐 | `massive bold heavy black sans-serif typography, vibrant electric yellow highlighter stroke (organic wavy squiggly underline or slanted block) accentuating key characters underneath, small minimalist directional arrow keyword tag in upper right, editorial book note aesthetic` | 底层：白色工程网格底<br>高亮层：荧光马克手绘波浪或倾斜色块<br>主体层：纯黑超粗标题字<br>注解层：右上箭头微标 |
| **09 游标刻度** | 居中厚重标题、下方精密刻度标尺、参数标签、四角L标 | `technical architectural blueprint poster, massive ultra-bold heavy black Chinese typography, precision caliper measurement scale bar with fine tick marks directly underneath the title, small minimalist dimension data box, subtle L-bracket crop marks at four corners` | 底层：四角L型十字裁切标与细网格<br>主体层：纯黑极粗主标题<br>测绘层：高精度游标刻度尺与尺寸胶囊 |

---

## 3. 字数自适应排版与视觉重心平衡矩阵 (Word-Count & Balance Matrix)

不同字数的标题如果机械套用同一种排版结构，极易出现“重心左偏”、“右侧空洞”或“呆滞拥挤”。针对常见字数，建立以下自适应动态排版规则：

### ① 4 汉字排版规范（最常见：如《极客构建》、《向内生长》、《未来已来》、《深度思考》、《架构演进》）
- **核心禁忌**：**绝不强行换成两行（2+2）左对齐**！这会导致视觉重量集中在画布左侧 1/3 区域，右侧产生巨大空洞。
- **字重与体量一致性原则 (Headline Visual Weight Consistency)**：所有 4 字单行横排风格的主标题在视觉占比上必须**完全统一**（占画布宽度的 73%~78%，高度占比 35%~50%，超粗黑体 MiSans-Heavy / Impact 级别字重），严禁出现局部风格标题字号过小或比例失调的情况。
- **最佳解法：单行水平居中 + 贯穿式穿插**：
  - **大字主体**：4 个大黑体字保持在**单行水平排列，完全居中（Centered）**；
  - **风格 03（刚柔碰撞）**：红色手写体英文置于 4 个汉字的**正中间（垂直水平居中）**，在汉字笔画间横向穿梭交叠，重心绝对平衡；
  - **风格 08（荧光划线）**：
    - **形态灵活多变**：支持**手绘波浪形笔迹（Wavy Squiggly Underline，自由灵动）**与**几何直线块状笔迹（Straight Block Highlight，规整硬朗）**；
    - **默认模式（推荐）**：荧光色块垫在**后两字（或动宾关键词）**下方，右上方搭配指向微标，产生打破对称的笔记灵动性与对角线引导；
    - **全贯穿模式**：荧光黄色条通栏横跨 4 个字底部，形成水平底座般的扎实沉稳感；
  - **风格 09（游标刻度）**：主标题字号与 02/03/08 保持完全对齐（超大字重），刻度标尺总宽度与主标题字宽紧密平齐，中间置入 `DIMENSION: 100% // V2.0` 数据胶囊，上下绝对居中对称。

### ② 5~6 汉字排版规范（如《秋日 奔赴山野》、《极客 奔赴未来》）
- **最佳解法：2+4 / 2+3 非对称阶梯错落（原视频原版技法）**：
  - **大字主体**：上行 2 字，下行 3~4 字，统一**左对齐 + 向前倾斜（Italic Slant）**；
  - **右上补空**：利用上行仅有 2 字留出的右上角矩形负空间，嵌入 2 行紧凑的全大写英文小字块，在视觉重量上与左侧拉平；
  - **层间手写**：红色连笔草书横向跨越在上行与下行大字的水平缝隙中，完美锁定核心焦点。

### ③ 2~3 汉字短标题（如《觉醒》、《极客》、《AI 浪潮》）
- **最佳解法：超大特写居中 + 夸张穿插**：
  - 单行超大字号居中，拉大字距；
  - 风格 08 自动采用**全词划线模式**，避免短词局部划线造成断裂感；
  - 辅助装饰元素（色块、巨型线框、斜切胶囊）大比例环绕，填充画面边缘。

---

## 4. 视觉品质控制红线 (Negative Prompts & Guardrails)

1. **背景干净**：默认采用 `subtle light grey grid notebook paper, clean studio white background, high-end editorial graphic design`，严禁杂乱写实摄影背景抢夺文字视觉重心。
2. **文字辨识度**：主标题字形必须厚重挺拔（Heavy/Black Weight Sans-serif），杜绝细弱笔画模糊。
3. **重心均衡**：画面几何中心即为视觉焦点，严禁无对称补偿的单边偏重。
4. **颜色克制**：整体画面严格遵循 **“黑白灰为主，点缀 1~2 种高明度对比色”**（如荧光绿 `#39FF14`、警示黄 `#FFE500`、先锋红 `#FF3333`）。
5. **负面提示词（Negative Prompts）**：`blurry, noisy, low quality, photorealistic messy cluttered background, 3d glossy bubble plastic, distorted anatomy, messy composition, low contrast, unbalanced weight, empty right side`。
