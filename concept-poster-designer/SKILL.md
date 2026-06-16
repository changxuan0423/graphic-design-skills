---
name: concept-poster-designer
description: Create high-concept minimalist graphic posters, banners, key visuals, promotional images, or flat-design campaign visuals from a user-provided character, word, phrase, short sentence, or letter group. Use when the user asks to turn text meaning into a conceptual poster, visual metaphor, typography-led graphic design, semantic key visual, banner, poster, publicity image, or prompt for image generation.
---

# Concept Poster Designer

## Workflow

1. Read `references/concept-poster-sop.md` before producing the final creative direction or image prompt.
2. Extract the required input:
   - Core text: character, word, phrase, short sentence, or letter group.
   - Text language.
   - Optional context, emotion, usage scene, aspect ratio, brand constraints, and forbidden elements.
3. If core text is missing, ask for it. Otherwise proceed with reasonable assumptions.
4. Analyze the text before designing:
   - Literal meaning and semantic center.
   - Emotional temperature.
   - Cultural associations, symbols, contradictions, and hidden tension.
   - Best visual logic: person relation, object relation, action, space, contrast, symbol, conflict, order, absurdity, or poetic relation.
5. Generate one focused concept, not a list of loose decorative ideas.
6. Build the poster around the core text as the dominant visual structure. Let imagery interact with the text through embedding, cutting, occlusion, scale contrast, spatial relation, or narrative tension.
7. Keep the composition minimal, readable, and poster-like. Prefer a few precise elements over many attractive elements.
8. Deliver:
   - A short semantic analysis.
   - One clear visual concept.
   - A complete image-generation prompt.
   - Negative prompt / forbidden direction.
   - Optional auxiliary copy if it strengthens the poster.

## Output Shape

Use this structure unless the user asks for another format:

```markdown
**语义判断**
[2-4 concise bullets]

**海报概念**
[one paragraph describing the core visual metaphor]

**成图提示词**
[single polished prompt ready for image generation]

**负面提示**
[concise forbidden elements and quality guards]

**辅助文案**
[optional one-liner or omit]
```

## Quality Bar

The result must feel like a designed conceptual poster, not a normal illustration, ad template, e-commerce layout, or a word enlarged on a pretty background. The viewer should immediately feel why the given text has been expressed this way.
