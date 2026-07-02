# Visual Asset Reference

Use this before generating or placing images in a teaching deck.

## What To Generate

Generate images when they help students see:

- A scale jump, such as desk -> molecule -> atom -> nucleus.
- A hidden mechanism, such as fields, interactions, or detector traces.
- A scientific instrument or environment.
- A boundary between known and unknown ideas.

Do not generate images just to decorate a text slide.

## Prompt Rules

Prompts should specify:

- Subject and teaching purpose.
- Aspect ratio needed for the slide.
- Visual style, such as "cinematic educational science visualization".
- No text, no labels, no formulas, no arrows.
- Whether the image is conceptual, not literal.
- Scientific constraints that prevent misconceptions.

For atom visuals, explicitly say:

```text
no orbital rings, no tiny planets, electron probability cloud
```

For detector visuals, explicitly say:

```text
particle detector cutaway, tracks and energy traces, conceptual educational visualization, no text, no labels
```

## PPT Placement Rules

- Keep labels and explanations editable in PPT, outside the image.
- Use generated images as the visual anchor, not as the full explanation.
- Add a short caption if a concept image could be misread as a literal photo.
- Check crops after rendering. Do not trust first placement.
- Use no more generated images than the story needs.

## Image QA

Reject or revise an image if:

- It includes unreadable fake text.
- It shows a misleading scientific mechanism.
- It is too decorative to teach the slide's point.
- It has crowded detail that will vanish on a classroom projector.
- Its palette fights the deck's accent color.
