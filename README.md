# Graphic Design Skills

Reusable agent skills (Codex / Claude Code compatible) for graphic design workflows.

## Included Skills

### [Concept Poster Designer](concept-poster-designer/)

Turns the meaning of a word, phrase, or short sentence into a high-concept minimalist poster: semantic analysis → one precise visual metaphor (with a mandatory anti-cliché diverge-then-kill step) → an image-generation prompt adapted to the target model.

**使用范例**（字段名固定，冒号后的内容按需修改；只有核心文字必填，其余留空自动推断）：

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

See [concept-poster-designer/README.md](concept-poster-designer/README.md) for installation and usage.
