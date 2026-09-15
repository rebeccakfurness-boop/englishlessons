# Selong Bay School · Cambridge English

Lesson resources for one-to-one online English tutoring, built against the
Cambridge curriculum frameworks: **Primary English (0058)** and
**Lower Secondary English (0861)**.

## Design system

All artifacts share one token set, taken from the Selong Bay School website:

| Token | Light | Source |
|---|---|---|
| `--teal` | `#007C83` | site `bg-teal` |
| `--gold` (orange) | `#FEA74A` | site `bg-orange` |
| `--ink` | `#46280A` | site `text-[#46280a]` |
| `--bg` (sand) | `#FDF7EE` | site `bg-sand` / `bg-cream` |

Typeface: **Nunito Sans** (body) / **Nunito** (headings), matching the school
site's `font-sans`. `IBM Plex Mono` is used for quoted pupil text and data.

Every page defines a full light palette on bare `:root`, then redefines tokens
for `prefers-color-scheme: dark` and `[data-theme="dark"]`.

## Structure

Each lesson ships four pieces:

1. `lesson.html`: the 40-minute interactive lesson, walked through together on the call
2. `script.html`: tutor-only teaching guide: stage timings, wording, expected sticking points
3. `review.html`: the pupil's own after-lesson page: video, practice, scored quiz, checklist
4. `Worksheet-NN-*.docx`: the written homework, uploaded to Google Classroom

## Primary 6 · Unit 1: Different Voices, Different Times

Cambridge Primary English Stage 6 (0058), following *Primary English Learner's
Book 6* (Burt & Ridgard, 2nd ed.). Unit 1 runs across four coursebook sessions:
1.1 *What is a prologue?* · 1.2 *Delve into detail* · 1.3 *Focus on technique* ·
1.4 *Write a short prologue*.

| # | Lesson | Session | Objectives |
|---|---|---|---|
| 1 | What is a prologue? | 1.1 | Setting the scene: character, environment, time (worksheet only) |
| 2 | Read Like a Detective | 1.2 | 6Ri.14, 6Rv.04, 6Rv.02, 6Rv.01 |

Lesson 2's worksheet is the printed review: one quiz section on the
lesson's takeaways, then a writing task built on the character, scene and
time words the pupil came up with herself.

Lesson 2 texts are original, written for these lessons rather than reproduced
from the coursebook, but keep its structure: a third-person scene followed by
a first-person note in italics, with two contrasting moods.

## Lower Secondary · Unit 1B: Autobiography and Travel Writing

| # | Lesson | Objective |
|---|---|---|
| 11 | Cut, Sharpen, Vary, Check | 8Wp.04: evaluate and edit to improve accuracy and effectiveness |
