---
name: concept-poster-designer
description: Turn the meaning of a word, phrase, short sentence, or letter group into a high-concept minimalist graphic poster — semantic analysis, one precise visual metaphor, and an image-generation prompt adapted to the target model. Use when the user wants a conceptual poster, art poster, semantic key visual, typography-led poster, 概念海报, 文字海报, 主视觉, or wants a word's meaning expressed visually. Not for e-commerce promos, sale banners, UI banners, information-dense marketing layouts, or generic illustration requests.
---

# Concept Poster Designer

Produce one poster concept built on one precise visual metaphor, then encode it as a prompt the target image model can actually execute. The value of the output is decided almost entirely in Step 2 (the metaphor); everything else is input parsing and output encoding — do not rush Step 2.

## Step 0 — Input triage

Fields (only the core text is required; infer the rest):

```text
核心文字 / Core text:
文字语言 / Language:
目标生成模型 / Target image model:   (GPT-image / Gemini / Midjourney / SD-Flux / unknown)
补充语境 / Context & usage:
气质说明 / Vibe line:                (one colloquial sentence describing the desired feel — see Step 4)
禁用元素 / Forbidden elements:
是否允许辅助文字 / Allow auxiliary text:  (yes/no; if yes, state how it must relate to the theme)
尺寸比例 / Aspect ratio:
品牌场景 / Brand constraints:
```

Route special inputs before analyzing:

- **Proper noun / brand / product / code idiom** (EverOS, "Hello World"): dictionary reading does not apply. Instead ask: what does the product do, what does the brand stand for, what ritual or in-joke does the phrase carry in its community? ("Hello World" is a programmer's first-output ritual, not a greeting.) If brand positioning is unknown and unguessable, ask the user for one line.
- **Sentence longer than ~6 words**: a full sentence cannot be the "large, clear dominant title" — pick the semantic anchor word(s) to carry the large scale, demote the rest to a secondary typographic line.
- **Emoji / numerals**: the glyph itself is the graphic form; skip language handling.
- **Emotionally sensitive words** (self-harm, grief, illness, trauma): mandate the quiet register — restrained imagery, meaningful whitespace, dignity rather than shock, no graphic depiction.
- **Wide banner (ratio > 2:1)**: switch to horizontal composition logic (left-right or asymmetric grid, smaller ambient metaphor). The quality bar is "reads clearly at thumbnail height", not "collectible exhibition poster".

## Step 1 — Semantic reading

Read the text through three lenses, briefly: literal meaning and semantic center; emotional temperature (gentle, cold, oppressive, hopeful, alienated, free…); hidden tension (pun, paradox, social meaning, cultural resonance). Abstract words need concrete carriers; concrete words need conceptual treatment.

## Step 2 — Diverge, then kill (mandatory)

A language model's first association is by definition the highest-probability one — which is exactly what makes it a cliché. A quality checklist applied to a single idea cannot fix this; only generating alternatives and killing the obvious ones can.

1. **Write the ban list first.** Name the 2–3 most predictable symbols for this text. They are forbidden unless structurally subverted (and if subverted, say how). Common defaults to ban: 孤独→空椅子/雨窗独影, 自由→飞鸟/断链/开笼, 时间→钟表/沙漏, 爱→心形/牵手, 死亡→骷髅/凋谢的花, 成长→幼苗, 希望→日出/一缕光, 内卷→漩涡/螺旋, connection→握手/拼图, idea→灯泡, silence→捂嘴/封条.
2. **Generate 5 candidate metaphors**, each through a *different* visual-logic lens:
   - **Scale contrast** — 内卷: thousands of identical tiny figures together form one giant figure of the same shape.
   - **Spatial relation** (distance, direction, isolation) — 孤独: one lit phone booth inside an unlit crowd.
   - **Person relation** — 陪伴: two shadows cast by a single figure.
   - **Object relation** — 依赖: a ladder leaning on nothing.
   - **Action moment** (suspended instant) — 决定: a coin photographed mid-air, both faces blurred.
   - **Symbolic substitution** — 审查: a paragraph where every word is a black bar except one.
   - **Conflict / paradox** — 和平: a dove drawn from the silhouettes of jets.
   - **Order relation** (repetition, grid, one deviation) — 个性: a grid of identical stamps, one printed upside down.
   - **Absurd relation** — 加班: an office chair with bicycle pedals.
   - **Poetic relation** (quiet, indirect) — 思念: a second cup of tea, still steaming, no one there.
3. **Kill**: discard any candidate on the ban list, then discard whichever survivor feels safest.
4. **Select by specificity**: could this metaphor be reused for a different word unchanged? If yes, it is not bound tightly enough — reject it. The winner should make the viewer feel the text and image could not be separated (会心一击).

Record the winning lens and one rejected candidate — both go in the 语义判断 output section, so the user can pull the other thread.

## Step 3 — Composition

Decide the spatial arrangement before any detail — in plain terms: does the title sit high, centered, or low? Is there a stage-like ground plane for a figure to stand on? Does the figure stand in front of the letters, or walk through a cut-out in them? Only then refine.

- Core text is the dominant typographic layer — a wall, a giant signboard, a stage backdrop — not "an image with a title in the corner". 1–3 visual subjects maximum; whitespace used as tension, silence, or isolation — never filled because space exists.
- Even a short phrase contains a bigger word: identify the one word that carries the emphasis (人民万岁 → 人民) and let scale, light, gaze, and occlusion orbit that word.
- Hierarchy: title first, metaphor second, tiny metadata (numbering, date, signature) only when it adds exhibition-poster credibility. Auxiliary copy appears only if the user allowed it, and must state its relation to the theme.
- **Feasibility tiers for image-text interaction** — image models execute glyph surgery poorly, so prefer the safe tier:
  - *Safe*: occlusion by large flat shapes, subject standing before/behind the title, scale contrast, spatial placement, color inversion, reserved negative space.
  - *Risky* (short Latin words on capable models only): imagery entering letter counters, cutting letterforms.
  - *Avoid*: distorting, dissolving, or rebuilding CJK characters — the realistic outcome is unreadable pseudo-hanzi, which fails the whole poster.

## Step 4 — Style register: fixed base + one vibe line

Think of it as 汤底 + 调味: Steps 1–3 (semantic reading, metaphor, composition) are the fixed soup base that never changes; the style is decided by **one colloquial vibe line** (气质说明) appended at the end. Instruction-following models (GPT-image, Gemini) understand plain-spoken vibes better than stacked design jargon — "女儿看了会喜欢 + 有花 + 有卡通熊" works.

If the user gave a vibe line, honor it. If not, compose one with this fill-in formula and state it in the concept:

> 色彩基调 + 画面质感/材质 + 艺术风格/参考美学 + 情绪/目标人群/氛围
> e.g. "色彩日系明亮，几何图形 + 像素感" / "夏日感，像马卡龙一样的糖果玻璃质感" / "黑金属背景，喜欢 F1 赛车的人会喜欢"

Default register when nothing is specified: flat graphic-art print — **commit to exactly one medium** (silkscreen *or* lithograph *or* risograph, never a slash-list), limited palette, subtle grain, crisp edges.

Branch when context demands it — **brand constraints always override both the defaults and the vibe line**:

- Tech / product / brand (e.g. a GitHub banner): Swiss-modernist vector geometry, clean flat color, brand accent color, no paper aging or halftone nostalgia.
- Playful subjects: bold geometry, saturated flat color.
- Inherently photographic concepts: duotone or high-contrast photographic poster.

### Recipe: movie / fan-art poster

For posters based on an existing film or show: forbid original cast likenesses and copyrighted character designs — express the subject through 背影、剪影、局部、联想 (back views, silhouettes, partial details, associative imagery) instead. If auxiliary text is allowed, fictional film-festival laurels and distributor marks scattered at slightly irregular positions add real-poster credibility. Default ratio 3:4.

## Step 5 — Text fidelity

The exact title text is the deliverable's hardest technical requirement. Before writing the prompt:

- Quote the title once, verbatim: `the exact text "…", spelled precisely, letter for letter`.
- **CJK longer than ~4 characters, or Latin longer than ~3 words**: warn the user that in-image rendering will likely corrupt; propose trimming to the semantic core, or the **two-pass workflow** — generate the composition with reserved negative space and no text, then set real typography in Figma/Photoshop. Offer this fallback proactively for CJK titles.
- For CJK titles rendered in-image, recommend GPT-image or Gemini; Midjourney and SD-family will invent pseudo-hanzi.

## Step 6 — Emit the prompt for the target model

Universal rules:

- The prompt contains **only renderable visual facts**: medium, subject, composition, exact title text, palette, texture, ratio. Design rationale ("memorable", "the viewer should feel…") belongs in the 海报概念 section — image models cannot act on it.
- **No negation in the positive prompt.** Diffusion models embed nouns, not the word "avoid" — "no clutter" summons clutter. State the positive equivalent instead: "single focal subject, generous empty background, matte flat ink".
- Front-load the three non-negotiables in the first sentence: medium, quoted title, the one metaphor.
- Deliver no brackets, placeholders, or slash-alternative lists — every value resolved, optional lines deleted.
- Never put the same noun family on both positive and negative sides (don't request "collage" and ban "low-quality collage").

Per-model emission:

| Target | Form | Length | Exclusions | Ratio |
|---|---|---|---|---|
| GPT-image / Gemini (default when unknown) | natural-language paragraphs — may be written in the user's language (colloquial Chinese works well), with the vibe line appended verbatim at the end | ≤250 words | phrase positively inline; no negative block | state size, e.g. `1024x1536` |
| Midjourney | front-loaded phrase | ≤60 words | `--no photo, 3d, gradient, watermark` | `--ar W:H` |
| SD / Flux family | comma-separated tags | ≤50 words | separate negative prompt, concrete visual tokens only: `photo, 3d render, gradient background, drop shadow, watermark, busy background, extra text` | note `width/height` |

Tell the user which field or flag each block goes into. If a wide ratio exceeds the model's supported range, say so and give the nearest supported ratio plus a crop note.

## Step 7 — Verifiable checks

Check mechanically; if any item fails, return to Step 2 and regenerate the concept — do not patch the prose:

- Exactly one metaphor in the prompt (count them).
- ≤3 visual subjects (count the nouns).
- Winning lens and one rejected candidate named in 语义判断.
- Concept is not on the ban list, or the subversion is stated.
- Title placement given in concrete positional terms.
- No brackets, slash-lists, or negations left in the delivered prompt.
- Prompt within the target model's length budget.

## Delivery

Section headings follow the user's conversation language (canonical pairs: 语义判断/Semantic reading, 海报概念/Poster concept, 成图提示词/Image prompt, 参数与负面提示/Parameters & negatives, 辅助文案/Auxiliary copy):

```markdown
**语义判断**
[2–4 bullets + winning lens + one rejected direction and why]

**海报概念**
[one paragraph: the metaphor, the register, why this text demands this image]

**成图提示词**
[the model-adapted prompt; label the target model]

**参数与负面提示**
[only what the target model actually consumes; name the field/flag. Omit if none.]

**辅助文案**
[optional one-liner, or omit]
```

If an image-generation tool is available in the session and the user expects a rendered image, run the prompt (folding exclusions into the form that tool accepts) and deliver the image alongside the prompt.

## Iteration & variants

- **"给我 N 个方向"**: N independent concepts, each through a different lens, each passing Step 7 — this overrides the one-concept rule.
- **Series mode ("做成一组/系列")**: keep the winning concept fixed and run it through 5–10 different vibe lines — one word becomes a coherent poster series, not one finished image. Vary only the vibe line; the metaphor and composition stay.
- **Refinement ("暖一点", "再收一点")**: keep the metaphor, adjust the vibe line/palette/temperature. Locked constraints (禁用元素, ratio, brand) persist across every iteration.
- **"换个思路"**: return to the Step 2 candidate pool and pick a different lens; the original ban list stays in force.
- **Always regenerate from the full spec.** On every iteration, emit the complete updated prompt from the full input contract — never a patch instruction like "make the previous one warmer". Incremental follow-ups accumulate drift in the image model's context and in the user's own head. (Users driving ChatGPT directly should edit their first message instead of sending follow-ups, keeping the conversation to a single exchange.)

For two fully worked examples calibrating the quality bar (孤独 exhibition poster; EverOS wide tech banner), read `references/worked-examples.md`.
