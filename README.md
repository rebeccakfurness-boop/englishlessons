# Selong Bay School — Cambridge Lower Secondary English

Lesson resources for one-to-one online English tutoring, built against the
Cambridge Lower Secondary English curriculum framework (0861).

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

1. `lesson.html` — the 40-minute interactive lesson, walked through together on the call
2. `script.html` — tutor-only teaching guide: stage timings, wording, expected sticking points
3. `review.html` — the pupil's own after-lesson page: video, practice, scored quiz, checklist
4. `Worksheet-NN-*.docx` — the written homework, uploaded to Google Classroom

## Unit 1B — Autobiography and Travel Writing

| # | Lesson | Objective |
|---|---|---|
| 11 | Cut, Sharpen, Vary, Check | 8Wp.04 — evaluate and edit to improve accuracy and effectiveness |
