# Concept Poster SOP

## Objective

Create a high-concept graphic art poster from a user-provided character, word, phrase, short sentence, or letter group. The poster must translate meaning into a visual metaphor: text is the theme, image deepens the text, and both form one complete visual sentence.

Do not create a generic illustration. Do not simply enlarge a word and place it on a decorative background.

## Input Template

```text
核心文字/单词/词组/字母:
文字语言:
可选补充语境:
可选情绪倾向:
可选禁用元素:
可选尺寸/比例:
可选品牌/场景:
```

If the user omits non-core fields, infer them from the text. Ask only when the missing core text makes the task impossible.

## Step 1: Semantic Reading

Before designing, analyze the input through these lenses:

1. Literal meaning: What is the most basic meaning?
2. Emotional tendency: Is it gentle, cold, dangerous, lonely, romantic, oppressive, hopeful, pure, desirous, orderly, conflicting, alienated, free, silent, destructive, reborn, etc.?
3. Semantic tension: Does it contain pun, contrast, paradox, social meaning, philosophical depth, emotional pressure, or cultural resonance?
4. Visual logic: Which relationship can best carry the meaning?
   - Person relation
   - Object relation
   - Action relation
   - Spatial relation
   - Scale contrast
   - Symbolic relation
   - Conflict relation
   - Order relation
   - Absurd relation
   - Poetic relation
5. Abstract words need concrete carriers. Avoid empty abstract patterns.
6. Concrete words need conceptual treatment. Avoid literal object illustration without a designed idea.

## Step 2: Concept Selection

Choose one dominant visual metaphor. It should be simple enough to read quickly and specific enough to feel bound to the word.

Good concepts usually have:

- One clear semantic center.
- One memorable relation or contradiction.
- One dominant text structure.
- One restrained image intervention.
- One emotional temperature.

Avoid:

- Multiple competing metaphors.
- Decorative symbols with weak semantic connection.
- Overexplaining the word with many objects.
- Beautiful but interchangeable imagery.

## Step 3: Composition Logic

Use a minimalist, stable, poster-like layout.

1. Make the user input the core title. It should be large, clear, and structurally important.
2. Let imagery interact with the title. It may stand before it, hide behind it, enter its counters, cut through it, distort it, cast shadows on it, or use its negative space.
3. Control element count. Usually use one to three key visual subjects.
4. Use hierarchy:
   - First layer: core title text.
   - Second layer: visual metaphor / narrative image.
   - Third layer: very small auxiliary text, numbering, signature, or caption only when useful.
5. Use whitespace as tension, silence, breath, or isolation. Do not fill the poster merely because space exists.
6. The result must look like a finished poster, not a cropped illustration.

## Step 4: Image Expression

Select the strongest single image that condenses the word's meaning.

Use:

- Figure-to-figure relation.
- Figure-to-object relation.
- Scale contrast.
- Direction or distance.
- Occlusion.
- Cutting and fragmentation.
- Suspended action moment.
- Negative space.
- Repetition only when repetition expresses the meaning.

The metaphor should be clever but not unreadable. Aim for a "会心一击" moment: once seen, the viewer feels the text and image could not easily be separated.

For conflict, paradox, or contrast, sharpen the opposition visually.

For poetic, emotional, memory-like, or philosophical words, use quieter imagery, more restraint, and more meaningful whitespace.

## Step 5: Visual Style

Use the language of advanced graphic art posters:

- Strong flat graphic design, not generic 3D illustration.
- Collage, silkscreen, lithograph, or printmaking feeling.
- Clean color system with limited colors.
- Strong contrast, often saturated main background plus pale or high-contrast large title text.
- Subtle grain, paper texture, halftone, slight aging, or print imperfections.
- Crisp subject details, unified by a flat poster tone.
- Clear, restrained, hard-edged, conceptual print atmosphere.

Avoid:

- Cheap templates.
- Low-quality collage.
- Ordinary commercial ad layout.
- E-commerce poster style.
- Messy over-textured grunge.
- Random decorative shapes.
- Purely atmospheric visuals with no semantic function.

## Step 6: Typography

1. Preserve the user's original text as the core title.
2. For English words or letter groups, keep the original spelling. Use strong, legible letterforms.
3. For Chinese text, usually use large Chinese characters directly unless a bilingual or partial typographic strategy is semantically stronger.
4. Optional auxiliary copy may sit in a restrained corner and should deepen the theme in one short line.
5. Tiny metadata such as numbering, signature, date, or category can be used sparingly to add exhibition-poster feeling.
6. All text must feel integrated into the image, not pasted on afterward.

## Step 7: Prompt Construction

Build the final image prompt in this order:

1. Format and medium: advanced minimalist conceptual graphic poster / banner / key visual.
2. Core title text and language.
3. Semantic concept in one sentence.
4. Composition: title placement, scale, hierarchy, whitespace, visual element placement.
5. Visual metaphor: concrete subject and its relation to the title.
6. Style: flat graphic art, print texture, limited palette, silkscreen / lithograph / collage.
7. Typography: large legible title, optional small caption, integrated typesetting.
8. Quality constraints: strong poster feeling, clean, memorable, high-end, no clutter.
9. Aspect ratio if known.

## Reusable Prompt Template

```text
Create an advanced minimalist conceptual graphic poster based on the core text "[CORE_TEXT]" in [LANGUAGE].

The poster must not be a generic illustration or a decorative word poster. First translate the meaning of "[CORE_TEXT]" into a precise visual metaphor: [SEMANTIC_CONCEPT].

Composition: use the core text "[CORE_TEXT]" as the dominant typographic structure, large, clear, and highly legible. Let the image element interact with the letterforms/characters through [INTERACTION_METHOD: embedding / occlusion / cutting / negative space / scale contrast / spatial tension]. Keep the layout stable, clean, and poster-like, with intelligent whitespace and a clear hierarchy: title first, visual metaphor second, tiny auxiliary text only if needed.

Visual metaphor: [CONCRETE_VISUAL_CARRIER_AND_RELATION]. The image must make viewers immediately understand why this word is expressed this way, while still feeling clever, restrained, and memorable.

Style: high-end flat graphic art poster, strong typography, conceptual editorial design, refined collage / silkscreen / lithograph / printmaking texture, limited color palette of [COLORS], subtle paper grain and halftone, crisp edges, clean composition, strong visual memory, exhibition-poster quality.

Typography: the exact core text "[CORE_TEXT]" must appear as the main title, integrated into the image rather than pasted on. Optional small caption: "[AUX_COPY]".

Avoid clutter, cheap template design, ordinary commercial advertising layout, e-commerce style, generic 3D illustration, random decorative symbols, unreadable text, excessive grunge, excessive elements, and images unrelated to the word meaning.

Aspect ratio: [ASPECT_RATIO].
```

## Negative Prompt Template

```text
generic illustration, decorative typography only, random symbols, cluttered composition, cheap poster template, e-commerce advertising layout, ordinary commercial flyer, excessive text, unrelated imagery, unreadable title, misspelled text, low-quality collage, messy grunge, over-detailed background, generic 3D render, stock photo look, weak concept, no semantic connection between text and image
```

## Final Check

Before delivering, verify:

- Is the core text the first visual layer?
- Does every image element serve the word's meaning?
- Can the viewer quickly feel the emotion and logic of the word?
- Is the metaphor concrete enough but not literal-minded?
- Is the composition minimal, strong, and memorable?
- Does the result feel like a collectible / exhibition poster?
- Is the prompt specific enough for an image model to execute?
