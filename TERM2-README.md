# Term 2 update — what's changed & what you need to do

## 1. Upload the 10 PDFs to your Cloudflare R2 bucket

Unzip **term2-pdfs-for-cloudflare-r2.zip** and upload all 10 files into the **same R2 bucket**
you already use (the one behind `pub-c9d54ec1efa04cfeaa3041eebb9144db.r2.dev`), at the **top
level** (no folder) — just like the Term 1 PDFs. Keep the filenames exactly as they are:

```
term2-week-01-old-woman-and-her-pig.pdf
term2-week-02-south-africa-zimbabwe-journey-through-time.pdf
term2-week-03-the-small-seed.pdf
term2-week-04-a-bowl-of-phutu.pdf
term2-week-05-storm.pdf
term2-week-06-the-boerewors-man.pdf
term2-week-07-sisandas-gift.pdf
term2-week-08-wolfs-supper.pdf
term2-week-09-why-crocodile-lives-in-the-river.pdf
term2-week-10-nelson-mandela-long-walk-to-freedom.pdf
```

The app already points at these exact filenames, so once they're in the bucket the
"Download Reading (PDF)" button will work for every Term 2 week.

## 2. Deploy the updated app

Unzip **reading-app-term2-update.zip** and deploy the `reading-app` folder exactly where your
current app lives (replacing the old files). Nothing about your Firebase setup, hosting, or
the live-quiz system needs to change.

## 3. What's new

- **Term dropdown** — a new "Term" selector sits next to the Week dropdown. Term 1 (your
  original 10 voyaging/migration stories) is unchanged. Term 2 (South Africa & Zimbabwe) is
  new. Switching terms rebuilds the voyage track and week list automatically.
- **10 new Term 2 weeks**, each fully built with the same structure as Term 1 — Monday lead-in
  + vocab + comprehension, Tuesday levelled guided-reading groups, Wednesday paired
  activities, Thursday/Friday understanding projects, full lesson plans (WALT, timings,
  teacher "say" lines), printable worksheets, and project guides:
  1. The Old Woman and Her Pig
  2. South Africa & Zimbabwe: A Journey Through Time (non-fiction timeline)
  3. The Small Seed
  4. A Bowl of Phutu
  5. Storm
  6. The Boerewors Man
  7. Sisanda's Gift
  8. Wolf's Supper
  9. Why Crocodile Lives in the River
  10. Nelson Mandela: The Long Walk to Freedom
- **Live quiz** (host-quiz.html / student-quiz.html) now also has a Term selector. All 10
  Term 2 weeks have a 20-question quiz bank, and **every question is pure reading
  comprehension** — plot, character, detail, sequence, cause & effect, and vocabulary-in-
  context — written directly from that week's story. None of the questions ask about lesson
  activities, projects, or curriculum labels. Term 1's quizzes are untouched.

## 4. Adding or editing quizzes later

All 10 Term 2 weeks now have quizzes. If you ever want to tweak or replace individual
questions, edit `window.READING_QUIZ_DATA["2"]` and `window.READING_QUIZ_WEEK_TOPICS["2"]` in
`reading-quiz-data.js` — each week is keyed by week number as a string, holding an array of 20
`{ q, options, correct, day }` objects.
