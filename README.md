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

## How pupil work comes back

Pupils do not have claude.ai accounts in the school organisation, so the review
page does **not** use the `db` capability. Publish it with `capabilities: {}`.

Declaring `db` would make the artifact organization-internal and unshareable by
public link, and would only save for a viewer signed in to the owner's
organization. Neither holds here.

Instead the review page carries the whole worksheet inline and:

- keeps answers in `localStorage` as the pupil types, so they can stop and come
  back in the same browser
- shows a counter of how many parts are done
- has a **Show my answers to copy** button that renders every answer, the quiz
  score and the checklist into one plain-text block, name and date at the top,
  auto-selected, for pasting into the Google Classroom answer box

The limitation to warn pupils about: the work lives in that browser only until
they copy it out. A private window, a shared computer, or clearing history
loses it.

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
