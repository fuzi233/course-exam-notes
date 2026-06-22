---
name: course-exam-notes
description: Use when the user asks to turn course PPT/PDF/slides/tutorials/case studies/past papers/sample answers into exam-ready Markdown notes for finals, memorisation, revision, bilingual study aids, source coverage audits, or past-paper-driven topic prioritisation.
---

# Course Exam Notes

## Overview

Create exam-oriented Markdown notes from course source files. Prioritise source coverage, past-paper evidence, concise English answer phrases, bilingual memory support, and memorisable topic summaries over page-by-page slide replication.

## Core Rules

- Do not infer course content from filenames alone; open/read every relevant source or mark why it was not readable.
- Use stronger sources to control weaker ones: exam guidance/past papers/sample answers > lecture/tutorial/case materials > required readings > generated/user notes.
- Treat generated notes only as secondary references, never as primary evidence.
- Preserve key English definitions and answer sentences close to source meaning.
- Do not invent frameworks, examples, definitions, steps, classifications, or priority labels unsupported by sources.
- Mark uncertainty as `uncertain from source files`; ignore administration unless it affects the exam.
- Keep notes compact enough for memorisation, but not lazy: every expected topic needs definition, core points, example, evidence, and exam sentence.
- Prefer exam-answer wording over generic textbook prose.

## Workflow

### 1. Establish Scope

Infer course code/name, expected topic range, deliverable mode, and output filename from the user request. If missing, choose clear defaults such as `COURSE_exam_core_notes.md` and `COURSE_source_coverage_audit.md`.

| Mode | Use when | Output |
|---|---|---|
| Full exam pack | Many sources or high-stakes final revision | Main notes + separate audit |
| Focused topic pack | User names a topic/week/module | Topic notes + compact audit |
| Repair/upgrade pass | User provides existing notes | Revised notes + coverage/change notes |

Before edits, state the file(s) to change and a 3-6 bullet plan.

### 2. Inventory Sources

Run file discovery first, normally with `rg --files`. Classify likely relevant files:

- lecture topics/slides/PPT/PDF
- tutorials, seminars, exercises
- case studies and handouts
- past papers, sample answers, marking criteria
- official readings or articles included with the course
- generated notes or AI notes, marked secondary only
- unrelated files, marked excluded with reason

For duplicates, use the newest/most complete version as primary; mark older versions `[partial] duplicate/version reference` unless they contain unique content.

Audit table:

```markdown
| Status | File name | Type | Covered content | Notes |
|---|---|---|---|---|
```

Use `[read]` only if actually opened/read; `[partial]` for selective reads, duplicates, huge files, or partial usefulness; `[unreadable]` with reason; `[excluded]` with reason.

### 3. Extract and Read Content

Use appropriate document tools/skills:

- PDF: extract text and page count; OCR/render only if text extraction fails.
- PPT/PPTX: extract slide text; inspect visually only when layout/images are essential.
- DOC/DOCX: convert/extract text.
- HTML/web exports: strip boilerplate and inspect visible content.

For each source, identify title/topic, definitions, stages/steps, types/classifications, benefits/limitations, examples/cases, exercises/questions, and repeated or exam-like phrasing. For large files, search/read relevant sections and mark `[partial] selectively searched/read for relevant sections`.

Keep file + page/slide/question references when available so important claims can be traced.

### 4. Build Coverage Maps

Create a topic coverage map before writing summaries:

```markdown
| Topic | Expected title | Source file used | Status |
|---|---|---|---|
```

Every expected topic must appear. If missing, unreadable, or only covered by generated notes, state that explicitly.

### 5. Audit Exam Evidence

Read past papers and sample answers before writing summaries. Produce:

```markdown
| Exam/source file | Question topics found | Question style | Implication for revision |
|---|---|---|---|
```

Detect question styles: define X; explain phases/steps/types; describe uses/roles; discuss benefits/limitations; compare/contrast; give examples; apply to case/product/company.

Assign priorities from evidence:

- **A**: directly tested, repeated, or foundational for many answers.
- **B**: examinable and useful, but less directly evidenced by past papers.

Avoid `C-level` skim sections unless the user explicitly requests them. For each A-priority topic, capture likely answer shape: definition, list/process, compare/contrast, discuss/evaluate, or case application.

### 6. Write the Main Notes

Recommended structure:

```markdown
# COURSE Exam Core Notes

## Part 1: Universal Answer Templates
### Common Exam Question Types
### Universal Benefits Template
### Universal Limitations Template
### Universal Definition Template
### Universal Examples Bank
### Universal Exam Sentences

## Part 2: Topic-by-Topic Core Notes
### Topic X: Original Topic Title [A/B]
#### Core definition
#### 中文辅助理解
#### Must memorise for this topic
#### Core points
#### Universal example
#### Evidence
#### Exam sentence

## Source Audit
Link to separate audit file if created.
```

Use a separate audit file for high-stakes tasks or long audits.

Topic section requirements:

- **Core definition**: 1-3 English definitions, source-aligned.
- **中文辅助理解**: one short Chinese memory hook.
- **Must memorise for this topic**: exact process names, definitions, classifications, and high-frequency lists.
- **Core points**: 5-12 bullets; start each with a bold English keyword and exam-ready explanation.
- **Universal example**: one source-supported example plus 2-3 exam sentences; add Chinese memory angle if useful.
- **Evidence**: 1-3 source pointers, preferably file + slide/page/question.
- **Exam sentence**: one concise English conclusion sentence.

Core point format:

```markdown
- **Keyword / phrase**: Exam-ready explanation in English. 中文补充只在有助记忆时加入。
```

### 7. Self-Check Before Final

Run a mechanical check where possible:

- topic count equals expected topic count
- every topic has Core definition, 中文辅助理解, Must memorise, Core points, Universal example, Evidence, Exam sentence
- audit file exists if referenced
- no placeholders, unfinished markers, or hidden missing files
- no unsupported claims presented as fact
- past papers/sample answers were used for priority decisions
- A/B priorities trace to exam evidence or coverage-map rationale
- no topic section relies only on generated notes
- output files are saved

Report any incomplete item honestly.

## Output Principles

- Main file: clean, memorisable, exam-facing.
- Audit file: complete source coverage, topic map, exam evidence, self-check.
- Final response: short summary, files changed, verification performed.
