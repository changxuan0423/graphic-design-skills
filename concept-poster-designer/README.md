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
核心文字: 孤独
语境: 艺术展海报
气质说明: 冷峻、克制、疏离
禁用: 眼泪、拥抱、心形
目标生成模型: GPT-image
```

Only the core text is required — everything else is inferred. The full input contract, workflow, and output shape live in [SKILL.md](SKILL.md); two complete worked examples (孤独 exhibition poster, EverOS wide tech banner) live in [references/worked-examples.md](references/worked-examples.md).

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
