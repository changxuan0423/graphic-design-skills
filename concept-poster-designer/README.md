# Concept Poster Designer

`concept-poster-designer` turns the meaning of a character, word, phrase, short sentence, or letter group into a high-concept minimalist graphic poster: semantic analysis → one precise visual metaphor → an image-generation prompt adapted to the target model (GPT-image / Gemini / Midjourney / SD-Flux).

It is a *method*, not just a style guide: a mandatory diverge-then-kill step bans first-association clichés (孤独≠空椅子, freedom≠flying bird), a feasibility tier keeps image-text interactions within what image models can actually render (especially CJK titles), and style branches by context (exhibition print / Swiss tech / photographic) instead of forcing one aesthetic.

Not for e-commerce promos, sale banners, or information-dense marketing layouts.

## Installation

```bash
# Codex
cp -R concept-poster-designer ~/.codex/skills/

# Claude Code
cp -R concept-poster-designer ~/.claude/skills/
```

Restart or start a new session so the skill metadata is discovered. The skill can also trigger implicitly on matching requests (e.g. "把'自由'做成一张概念海报").

## Usage

```text
Use $concept-poster-designer

## 用户输入内容:
核心文字 / 单词 / 词组 / 字母: "好奇心和执行力"
文字语言: 中英文结合
可选补充语境: 海报，专辑封面，无人
可选情绪倾向: 现代风格，线条主义
可选禁用元素:
是否允许辅助文字: yes
辅助文字如允许，必须与主题的关系说明: 向外探索世界，向内落地结果
可选尺寸/比例: 3:4
可选目标生成模型: GPT-image
可选品牌/场景:
```

字段名固定，冒号后的内容按需修改；只有核心文字必填，其余留空则自动推断。可选情绪倾向就是一句口语化的「气质说明」，决定整张海报的风格（如 "色彩日系明亮，几何图形 + 像素感"）。 The full input contract, workflow, and output shape live in [SKILL.md](SKILL.md); two complete worked examples (孤独 exhibition poster, EverOS wide tech banner) live in [references/worked-examples.md](references/worked-examples.md).

## Credits

方法论源自 X [@xiaoxiaodong01](https://x.com/xiaoxiaodong01) 的提示词框架，经小红书 @阿元《使用GPT Image2制作高级感海报的思路整理》整理扩展，本 skill 在其基础上加入反俗套发散机制、可行性分层与按模型出稿。

## Files

```text
concept-poster-designer/
├── SKILL.md                      # the full method
├── README.md
├── agents/openai.yaml            # Codex interface metadata
└── references/worked-examples.md # calibration examples (loaded on demand)
```
