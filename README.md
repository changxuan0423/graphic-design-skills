# Graphic Design Skills

Reusable Codex skills for graphic design workflows.

## Included Skills

### Concept Poster Designer

`concept-poster-designer` creates high-concept minimalist graphic posters, banners, key visuals, promotional images, and typography-led design prompts from a single character, word, phrase, short sentence, or letter group.

It turns text meaning into a visual metaphor instead of producing a generic illustration or a decorative word poster.

## Installation

Copy the skill folder into your Codex skills directory:

```bash
cp -R concept-poster-designer ~/.codex/skills/
```

Restart Codex or start a new thread so the skill metadata can be discovered.

## Usage

```text
Use $concept-poster-designer
核心文字/单词/词组/字母: 孤独
文字语言: 中文
可选补充语境: 艺术展海报
可选情绪倾向: 冷峻、克制、疏离
可选禁用元素: 眼泪、拥抱、心形
```

For a GitHub banner:

```text
Use $concept-poster-designer
核心文字/单词/词组/字母: EverOS
文字语言: 英文
可选补充语境: GitHub README banner
可选情绪倾向: 现代主义、极简设计、科技感、黄色品牌强调色
```

## Input Fields

```text
核心文字/单词/词组/字母:
文字语言:
可选补充语境:
可选情绪倾向:
可选禁用元素:
可选尺寸/比例:
可选品牌/场景:
```

Only the core text is required. Other fields can be inferred when omitted.
