# Engaging Lesson PPT Builder

A Codex skill for creating vivid, classroom-ready lesson PowerPoint decks. It is designed for high-school science and STEM lessons, where the goal is not just to explain content, but to make students curious enough to participate.

## What It Does

- Turns a lesson topic into a narrative classroom deck, not a text-heavy slideshow.
- Builds around hooks, prediction moments, visual reveals, short practice, evidence, boundaries, and exit tickets.
- Keeps visible slide text sparse while putting teacher delivery detail in speaker notes or handouts.
- Uses supporting skills for slide generation, image generation, design polish, physics accuracy checks, and printable teacher materials.
- Includes QA expectations: rendered slide previews, overflow checks, source notes, and generated-image provenance.

## Best For

- High-school science lessons
- STEM public classes or open lessons
- Concept-heavy topics that need visual intuition
- Teachers who want a deck plus speaker notes, teacher guide, and optional student worksheet

## Included Files

- `SKILL.md`: main skill instructions and workflow.
- `agents/openai.yaml`: display metadata for the skill.
- `references/deck-workflow.md`: lesson arc, page families, and slide-system guidance.
- `references/visual-assets.md`: image-generation and placement rules for teaching visuals.
- `references/teacher-handout.md`: teacher handout and worksheet structure.

## Suggested Workflow

1. Define the teaching job: audience, duration, prior knowledge, central question, and student output.
2. Build a lesson arc: hook -> prediction -> reveal -> concept naming -> practice -> evidence -> boundary -> exit ticket.
3. Research facts and sources before writing claims.
4. Design one coherent slide system for the whole deck.
5. Generate or source images only when they help students understand scale, mechanisms, evidence, or uncertainty.
6. Build the PPTX with speaker notes.
7. Render and inspect slide previews before delivery.
8. Add teacher-facing support such as a handout, board plan, misconception guardrails, and exit-ticket answers.

## Example Prompt

```text
Use $engaging-lesson-ppt-builder to create a 45-minute high-school physics lesson deck about particle physics. Make it visually engaging, scientifically accurate, and classroom-ready, with speaker notes and a teacher handout.
```

## Design Philosophy

The deck should feel like a guided classroom experience: a strong question, a reason to care, a visual path into the concept, and enough interaction for students to test their intuition. The teacher materials should work like a backstage guide, not a transcript.

## Notes

- Generated images should not contain labels, formulas, or long text. Keep labels editable in PowerPoint.
- Conceptual science visuals should be marked as conceptual when students may mistake them for literal photographs.
- Physics lessons should avoid common misleading visuals, such as electrons shown as tiny planets on fixed rings.
- Final decks should be rendered and visually inspected before delivery.
