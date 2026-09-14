# Selong Bay School, Cambridge Lower Secondary English

Lesson resources for one-to-one online English tutoring, built against the
Cambridge Lower Secondary English curriculum framework (0861).

## House style

**No em dashes.** Anywhere, in any deliverable. Use a comma, colon, full stop
or parentheses, whichever the sentence actually needs.

All artifacts share one token set, taken from the Selong Bay School website:

| Token | Light | Source on the school site |
|---|---|---|
| `--teal` | `#007C83` | `bg-teal` button shadow |
| `--gold` (orange) | `#FEA74A` | `bg-orange` button shadow |
| `--ink` | `#46280A` | `text-[#46280a]` on orange buttons |
| `--bg` (sand) | `#FDF7EE` | `bg-sand` / `bg-cream` |

Typeface: **Nunito Sans** (body) and **Nunito** (headings), matching the school
site's `font-sans`. `IBM Plex Mono` is used for quoted pupil text and data.

Every page defines a full light palette on bare `:root`, then redefines tokens
for `prefers-color-scheme: dark` and `[data-theme="dark"]`.

## What each lesson ships

1. `lesson.html` is the 40 minute interactive lesson, walked through together on the call
2. `script.html` is the tutor-only guide: stage timings, wording, expected sticking points
3. `review.html` is the pupil's after-lesson page: video, practice, scored quiz, checklist
4. `Worksheet-N-*.docx` is the written homework, uploaded to Google Classroom

The video slot in `review.html` is a single `VIDEO_URL` constant at the top of
its script block. Paste the link there and republish. It handles YouTube, Vimeo
and Drive links, and always shows a fallback link button in case the embed is
blocked.

## Unit 1B: Autobiography and Travel Writing

| # | Lesson | Objectives |
|---|---|---|
| 1 | Getting started: the four conventions | taught |
| 2 | Reading life writing: recognising the conventions | taught |
| 3 | Claim, Order, Senses | 8Ri.03, 8Ri.05, 8Ws, 8Wv |

### Parked

`lesson-XX-editing-parked/` holds a complete editing and proofreading lesson
(Cut, Sharpen, Vary, Check, objective 8Wp.04). It is finished and published but
sits much later in the sequence than the pupil has reached. Renumber it when the
unit gets there.
