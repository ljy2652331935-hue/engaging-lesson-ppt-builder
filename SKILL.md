---
name: engaging-lesson-ppt-builder
description: Create vivid classroom lesson PowerPoint decks for students, especially high-school science/STEM lessons in Chinese or English. Use when the user asks to make, redesign, improve, or systematize a teaching PPT/PowerPoint/课件/公开课/lesson deck that must be engaging, visually coherent, scientifically accurate, and classroom-ready, including optional teacher handouts, student worksheets, speaker notes, image-generation prompts, and rendered QA.
---

# Engaging Lesson PPT Builder

## Purpose

Build classroom decks that feel like a teachable experience, not a text dump. Optimize for student attention, teacher usability, factual accuracy, and visual consistency.

Core idea: make the deck first screen-ready, then make the teacher materials backstage-ready.

## Use The Right Supporting Skills

Load these skills as needed before acting:

- `presentations`: always use for PPTX creation/editing, previews, layout inspection, and overflow checks.
- `imagegen`: use when visual assets can improve curiosity, scale, or explanation. Generate bitmap images with no embedded text.
- `design-taste-frontend`: use when the user wants UI/design polish, visual redesign, stronger style, or "not template-like" pages.
- `physics-education-reviewer`: use for physics lessons or physics-adjacent claims, visuals, analogies, and misconception checks.
- `agent-reach`: use for internet research, current examples, source collection, or "全网搜/调研/查".
- `documents` and `pdf`: use when creating teacher handouts, student task sheets, rubrics, or printable guides.

## Default Deliverables

For a full lesson request, produce:

1. A final `.pptx` in `outputs/`.
2. Rendered slide previews and a montage for visual QA.
3. Speaker notes inside the PPTX for teacher delivery.
4. A source/provenance note for claims and generated visuals.
5. If requested or clearly useful: teacher handout `.docx` and student worksheet `.pdf`.

If the user only asks for a quick deck, keep handouts optional but still add speaker notes.

## Workflow

1. Define the teaching job.
   - Audience level, prior knowledge, class duration, central question, and desired student output.
   - Express the job as: "By the end, students should understand X because Y."

2. Build the narrative arc.
   - Prefer: hook question -> prediction -> visual reveal -> concept naming -> practice -> evidence -> boundary -> exit ticket.
   - Avoid agenda-like decks and encyclopedia slides.

3. Research and source.
   - Use primary or reliable educational sources for factual claims.
   - Keep a source note. Do not invent scientific facts, dates, discoveries, metrics, or examples.

4. Design the slide system.
   - Choose one visual language for the whole deck.
   - For high-school science, a strong default is "science museum / cinematic classroom": large visuals, restrained text, one accent color, clear interaction pages.
   - Read `references/deck-workflow.md` when planning or redesigning a deck.

5. Plan visuals.
   - Decide which slides need generated or sourced images.
   - Keep scientific structure editable in PPT when precision matters.
   - Read `references/visual-assets.md` before generating images.

6. Build the PPTX.
   - Use `@oai/artifact-tool` via the `presentations` skill.
   - Put final decks in `outputs/`.
   - Render every slide to PNG, create a montage, and run `slides_test.py`.

7. Review for teaching accuracy.
   - Check misconceptions, over-literal analogies, false mechanisms, and passive decoration.
   - Add prediction, short practice, feedback, and reflection moments.

8. Produce teacher support.
   - Speaker notes should be short and practical.
   - Teacher handouts should be a director's script, not a transcript.
   - Read `references/teacher-handout.md` when creating handouts or worksheets.

## Slide Design Rules

- One slide, one job.
- Use takeaway-style titles a teacher could say aloud.
- Keep visible copy sparse. Put delivery detail in notes or handouts.
- Use images for curiosity and intuition; use editable PPT text for definitions, questions, and claims.
- Do not put labels, equations, or long text inside generated images.
- Do not repeat the same layout for every slide. Mix hook, image sequence, concept board, practice, evidence, and synthesis layouts.
- Use one accent color consistently.
- Avoid generic three-card rows unless the content truly calls for comparison.
- Do not make decorative science visuals that imply false precision.

## Teaching Accuracy Rules

- Mark concept images as conceptual when they could be mistaken for literal photographs.
- Avoid misleading classics:
  - Electrons are not tiny planets on fixed orbits.
  - Particle detectors usually record tracks, energy deposits, and decay products, not "the invisible particle itself".
  - Higgs is not a magic explanation for all mass.
  - A successful model can still have known limits.
- Prefer the pattern: question -> student prediction -> visual/concrete evidence -> concept name -> memory sentence.

## Final QA

Before delivery:

- Render all slides and inspect the montage.
- Run overflow detection.
- Check title wrapping, footer consistency, image crops, and text contrast.
- Re-read visible copy for grammar, teacher voice, and student clarity.
- Confirm sources and generated-asset provenance are recorded.
- Mention any limitations or skipped checks in the final response.
