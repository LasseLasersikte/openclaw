# 01 — The ATS Resume System

75% of resumes are rejected by software before a human ever sees them. These are
**Applicant Tracking Systems (ATS)** — they scan for keywords, parse your work
history, and rank you against everyone else. This file gets you past the robot
*and* makes the human who reads you next say "interview."

---

## How the ATS actually thinks (30-second version)

- It reads plain text. Fancy columns, tables, text boxes, headers/footers, and
  graphics often get scrambled or dropped. **Keep layout simple.**
- It matches the **keywords and phrases in the job description.** If the posting
  says "stakeholder management" and your resume says "worked with teams," you
  lose points. Mirror their language (honestly).
- It rewards **measurable results.** "Increased X by Y%" beats "responsible for X."

---

## Prompt 1 — Extract the keywords that matter

> Paste this, then paste the job description under it.

```
You are an expert technical recruiter and ATS specialist. Below is a job
posting. Extract and return:

1. The 12–15 most important hard skills and keywords an ATS will scan for,
   ranked by how often/prominently they appear.
2. The 5 soft skills or themes the employer clearly cares about.
3. The exact job title as written (for keyword matching).
4. Any required tools, certifications, or qualifications I must mention if I
   have them.

Return as three short lists. Be specific — use the employer's exact wording.

JOB POSTING:
[paste the full job posting here]
```

Keep this output open. It's the target you're writing toward.

---

## Prompt 2 — Rewrite your experience into achievement bullets

> Paste this, then paste your current resume bullets (or rough notes) AND the
> keyword list from Prompt 1.

```
You are an expert resume writer. Rewrite my work experience into strong,
ATS-optimized bullet points using this proven formula:

[Action verb] + [what you did] + [tool/skill/method] + [measurable result].

Rules:
- Start every bullet with a powerful action verb (Led, Built, Cut, Drove,
  Launched, Streamlined, Negotiated). Never "Responsible for."
- Naturally weave in the keywords from the list below — but ONLY where they are
  truthful to what I actually did. Do not invent experience.
- Quantify wherever possible. If I didn't give a number, insert a clearly
  marked placeholder like [X%] or [$X] so I can fill it in.
- Keep each bullet to one or two lines.

TARGET KEYWORDS:
[paste the keyword list from Prompt 1]

MY EXPERIENCE:
[paste your current bullets or notes for each job]
```

---

## Prompt 3 — Write a punchy professional summary

```
Write a 3-sentence professional summary for the top of my resume, tailored to
the job below. It should: (1) state my title/identity and years of experience,
(2) highlight my 2 strongest relevant skills using the employer's language,
(3) name the value I bring. Confident, specific, no clichés like "team player"
or "hard worker." Return 3 versions so I can pick.

JOB TITLE I'M TARGETING: [title]
MY BACKGROUND: [1–2 sentences about you]
TARGET KEYWORDS: [paste from Prompt 1]
```

---

## Prompt 4 — The honest ATS score check

> After you've assembled your resume, paste it back with the job description.

```
Act as an ATS. Score my resume from 0–100 for this specific job posting, based
on keyword match, measurable results, formatting safety, and relevance.

Then give me:
- The top 3 things hurting my score and the exact fix for each.
- Any critical keyword from the posting I'm missing.
- One sentence I should add or cut.

Be blunt. I want the interview, not a compliment.

MY RESUME:
[paste your assembled resume]

JOB POSTING:
[paste the job posting]
```

Iterate until you're at 85+. Then move to `02-resume-templates.md` to drop your
content into a clean, ATS-safe layout.

---

## The five formatting rules that keep you machine-readable

1. **One column.** No side-by-side layouts.
2. **Standard section headers:** *Summary, Experience, Skills, Education.*
3. **No text inside images, tables, or text boxes** for anything that matters.
4. **Standard font** (Calibri, Arial, Georgia), 10–12pt. Save/submit as **.docx
   or PDF** — match what the application asks for; .docx is safest for ATS.
5. **Spell out then abbreviate:** "Search Engine Optimization (SEO)" so you match
   both forms.
