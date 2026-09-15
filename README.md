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
4. `Worksheet-N-*.docx` is the written homework, for lessons whose review page
   does not yet carry the work inline

The video slot in `review.html` is a single `VIDEO_URL` constant at the top of
its script block. Paste the link there and republish.

**Do not use an `<iframe>` for video.** The artifact sandbox blocks embedded
players, and a blocked frame renders as a black box with no error, so the pupil
just sees something broken. The page uses a styled link card that opens the
video in a new tab, plus an "I have watched the video" tick that saves with the
rest of the work. Remote thumbnails are blocked too, so the card is drawn in CSS
rather than pulling an image from YouTube.

## The homework flow

Two steps, in this order:

1. **Workbook** (`review.html`): video, recap, practice, self-check quiz,
   checklist. Nothing is marked. Progress is kept in `localStorage` so the pupil
   can stop and come back. Its final section is a button to Google Classroom.
2. **Worksheet** (`Worksheet-N-*.docx`): the written work, uploaded to Google
   Classroom. This is the part the tutor marks.

The workbook deliberately does **not** collect written answers. Pupils have no
claude.ai account in the school organisation, so publish it with
`capabilities: {}`. Declaring `db` would make the artifact
organization-internal and unshareable by public link, and would only save for a
viewer signed in to the owner's organization.

The Classroom link is the `href` on `#classroomLink` near the end of
`review.html`. Point it at the specific assignment rather than the Classroom
home page when the assignment URL is known.

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
