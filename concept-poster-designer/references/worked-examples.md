# Worked Examples

Two complete runs of the skill, showing the quality bar. Read these when calibrating what "specific enough" and "cliché" mean in practice — not as templates to copy.

---

## Example 1 — 「孤独」 · art exhibition poster · GPT-image · 2:3 portrait

**Input**: 核心文字: 孤独 · 可选补充语境: 艺术展海报 · 可选情绪倾向: 冷峻、克制、疏离 · 可选禁用元素: 眼泪、拥抱、心形 · 是否允许辅助文字: yes（关系说明: 深化孤独主题）· 可选目标生成模型: GPT-image

**Step 2 trace** (this is the part that decides everything):

- Ban list: 空椅子、雨夜窗前独影、人群中蜷缩的背影 — the three highest-probability 孤独 posters in existence.
- Candidates: spatial (one lit phone booth in an unlit crowd), scale (a vast auditorium, one occupied seat — dies: it's the banned empty-chair family inverted, still the same move), order (a crowd printed in perfect silkscreen registration, one identical figure printed out of register), poetic (a dinner table set for one with two chairs — banned family), symbolic (a phone screen as the only light source — safe but reusable for 失眠/成瘾, fails the specificity test).
- Winner: **order relation** — the misregistered figure. Loneliness is not the absence of people; it is being present and out of sync. The metaphor is carried by the print medium itself (套印错位), so text, image, and material speak the same language. Rejected runner-up worth keeping: the lit phone booth (spatial) — strong, but transplantable to "isolation" generally.
- CJK check: 2 characters — safe to render in-image on GPT-image; keep the characters large, clean, untouched.

**Delivered output:**

**语义判断**
- 孤独的现代形态不是缺席，而是"在场却错位"——人在群体中，节奏不在。
- 情绪温度：冷、克制，不需要悲伤符号。
- 选用视觉逻辑：秩序关系（整齐套印中的一处错版）。弃案：黑暗人群中唯一亮灯的电话亭（空间关系）——成立，但换成"隔绝"一词也能用，绑定不够专属。

**海报概念**
一张丝网版画质感的海报：画面下半部是一排排完全相同的扁平人形，墨色套印精准整齐；其中一个人形与其他毫无差别，唯独套印错位——青色与洋红色版偏移出重影，像信号不同步的人。标题「孤独」以大号宋体黑墨居上，笔画完整清晰，不参与任何变形。孤独在这里不是一个人，而是那个和所有人一样、却始终对不上版的人。

**成图提示词**（GPT-image）

> A silkscreen print poster, portrait format. The exact Chinese title "孤独", spelled precisely, letter for letter, set large in a classic serif typeface in dense black ink across the upper third, characters clean and fully intact. Below, orderly rows of identical flat human silhouettes printed in dark ink with crisp registration on warm off-white paper. One single figure among them, identical in shape, is printed out of register: its cyan and magenta layers offset a few millimeters, creating a subtle ghosted double image, while every other figure stays perfectly aligned. Single focal deviation, generous margins, flat matte ink, subtle paper grain, limited palette of black, off-white, cyan and magenta offsets. Minimalist conceptual exhibition poster, stable grid composition, strong typographic hierarchy. Tiny caption line at the bottom edge in small type: "在场，未对齐。"

**参数与负面提示**
Size: `1024x1536`（GPT-image API `size` 参数）。GPT-image 无 negative prompt 字段，排除意图已用正向表述覆盖。

**辅助文案**
在场，未对齐。

---

## Example 2 — 「EverOS」 · GitHub README banner · target model unknown · ~3:1 wide

**Input**: 核心文字: EverOS · 可选补充语境: GitHub README banner · 可选情绪倾向: 现代、极简、科技感 · 可选品牌/场景: 品牌黄强调色

**Step 0 triage — this input reroutes twice:**

- Proper noun: "EverOS" has no dictionary meaning. Reading it as ever = 永恒 → ∞ 符号 would be free-association kitsch. Instead anchor on what the product is — assume here: a personal AI memory OS ("记住你的系统"). If positioning were unguessable, ask the user for one line before designing.
- Wide banner (>2:1): horizontal composition logic, quality bar = legible at thumbnail height. The "exhibition poster / print grain" default register is wrong for a tech brand → Swiss-modernist vector branch, no paper aging.

**Step 2 trace:**

- Ban list (tech-brand defaults): 电路板线路、发光大脑、无限符号、环绕轨道线。
- Winner: **symbolic + order** — memory as a line that returns. One continuous yellow line runs the full banner width like a timeline; behind the wordmark it makes a single clean loop, then continues on. What passed through the system comes back. Safe-tier interaction only: the line passes *behind* the letterforms (occlusion), no glyph surgery.
- Text check: short Latin word, safe on all major models. Model unknown → default natural-language emission.

**Delivered output:**

**语义判断**
- 专名分流：不读字面，读产品——"记住的系统"，核心动作是"回来"。
- 视觉逻辑：符号 + 秩序关系（一条会折返的时间线）。弃案：以 "O" 为镜头光圈的记忆之眼（符号关系）——瞳孔/镜头意象在科技品牌里已近俗套。
- 风格分支：品牌语境覆盖版画默认 → 瑞士现代主义矢量，无纸纹做旧。

**海报概念**
深灰近黑的横幅上，"EverOS" 以厚重 grotesk 字体居左偏中排布。一条 2px 的品牌黄直线从画面最左端出发，水平穿过整个横幅——在字标背后干净地绕出一个环，再继续向右延伸出画。直线是时间，一次折返是记忆：经过这个系统的东西会回来。构图在缩略图尺寸下仍然只有两个元素：字标与线。

**成图提示词**（default natural-language；适用 GPT-image / Gemini）

> A minimalist Swiss-modernist tech banner, extreme wide format. The exact word "EverOS", spelled precisely, letter for letter, set in a heavy grotesque sans-serif in off-white, positioned left-of-center on a near-black charcoal background. A single thin bright-yellow horizontal line enters from the far left edge, runs level across the entire banner, passes behind the letterforms where it forms one clean circular loop, then continues straight to the right edge. Flat vector graphic, sharp edges, no texture, no gradient, two colors plus background: off-white type, yellow line, charcoal field. Vast negative space above and below the line, composition legible at thumbnail size.

**参数与负面提示**
目标比例 ~3:1。GPT-image 最宽支持 `1536x1024`（3:2）——生成后按中心水平带裁切至 3:1；Midjourney 用户可直接 `--ar 3:1 --no texture, gradient, glow`。

**辅助文案**
（省略——banner 上不加第二行文字，缩略图可读性优先。）

---

## Why these two

Example 1 shows the diverge-then-kill step doing real work: three candidates died on or near the ban list, and the winner is bound to the word through the print medium itself. Example 2 shows the two triage branches (proper noun, wide format) overriding the defaults — the print-texture register that Example 1 depends on would have been a mistake here.
