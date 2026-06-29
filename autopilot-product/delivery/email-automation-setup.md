# Email Automation Setup — wire the list in ~30 minutes (free)

This connects three pieces you already have into a hands-off machine: the **free
lead magnet** (the 1-Page Resume Checklist) → a **signup form** → the **5-email
welcome sequence** that sells the $27 toolkit on a timer. Once it's on, every
download becomes an automatic path to a sale.

Use **MailerLite** or **Brevo** — both have genuinely free tiers (MailerLite:
up to 1,000 subscribers + automations free; Brevo: unlimited contacts, daily
send cap). Steps below are written for MailerLite; Brevo is nearly identical
(noted where it differs).

---

## Before you start — have these ready

- [ ] The lead magnet as a **PDF** (`marketing/lead-magnet-resume-checklist.md`
      → print/export to PDF).
- [ ] The 5 emails from `marketing/email-welcome-sequence.md`.
- [ ] Your sales-page / Gumroad URL (to paste into the emails as `[LINK]`).

---

## Step 1 — Create the account (5 min)

1. Sign up free at **mailerlite.com** (or **brevo.com**).
2. Fill in basic sender details. Use a real **from-name** (your name) and a
   from-email you control.
3. *(Optional but improves delivery)* verify your sending domain later — not
   required to launch.

---

## Step 2 — Upload the lead magnet so it auto-delivers (5 min)

**MailerLite:** the cleanest pattern is to host the PDF and deliver the link in
Email 1.
1. Put the PDF somewhere with a public link (Google Drive "anyone with link,"
   Dropbox, or MailerLite's own file manager / a "file download" content block).
2. Copy that link — it becomes the `[download link]` in **Email 1**.

*(Brevo: same idea — host the PDF, link it in the welcome email.)*

---

## Step 3 — Build the signup form (5 min)

1. **Forms → Create form** → choose an **embedded form** (and/or a
   landing-page form if you don't have the sales page up yet).
2. Fields: **email** only. (Asking for less = more signups. Name is optional.)
3. Headline + button copy that converts:
   - Headline: *"Free: The 1-Page Resume Checklist"*
   - Sub: *"Fix the 12 things that get resumes auto-rejected."*
   - Button: *"Send me the checklist"*
4. Save. You'll get an **embed snippet** (for the sales page) and a **hosted form
   URL** (for Pinterest pins, your bio, Reddit profile, post CTAs).

**Put the hosted form link in:** your social bios, the bottom of value posts, and
a Pinterest pin titled like the lead magnet. That's how cold traffic becomes
subscribers you own.

---

## Step 4 — Create the automation (10 min)

1. **Automations → Create new automation.**
2. **Trigger:** "When a subscriber joins a group" → create/select a group called
   `Resume Checklist`. (Set your form from Step 3 to add subscribers to this
   group.)
3. Build the steps exactly in this order (this matches the sequence file):

   | Step | Action | Delay before it |
   |---|---|---|
   | 1 | Send **Email 1** (deliver checklist + quick win) | none — immediate |
   | 2 | Wait | 1 day |
   | 3 | Send **Email 2** (keyword trick) | — |
   | 4 | Wait | 2 days |
   | 5 | Send **Email 3** (cover letters + soft offer) | — |
   | 6 | Wait | 2 days |
   | 7 | Send **Email 4** (interview/salary stakes) | — |
   | 8 | Wait | 2 days |
   | 9 | Send **Email 5** (direct offer + guarantee) | — |

4. For each email: paste the **subject** and **body** from
   `email-welcome-sequence.md`, and replace every `[LINK]` with your Gumroad/
   sales URL and `[Your name]`.
5. **Turn the automation ON.**

*(Brevo: Automations → Welcome/Custom → trigger on "contact added to list" →
add Email + Wait steps the same way.)*

---

## Step 5 — Test it end to end (5 min)

1. Subscribe yourself through the real form with a spare email.
2. Confirm **Email 1 arrives within a minute** and the checklist link works.
3. In the automation editor you can usually "send test" for emails 2–5 to eyeball
   them without waiting days.
4. Check one renders fine on **mobile** (most opens are on phones).

If Email 1 doesn't arrive: check spam, confirm the automation is ON, and confirm
the form adds people to the `Resume Checklist` group that triggers it.

---

## You now own a renewable traffic source

Cold visitor → grabs the free checklist → enters the automation → gets real help
→ buys the $27 toolkit (and later the bump/upsell) — all without you touching it.

Two upgrades once it's running:
- **Broadcasts:** every week or two, send your list one genuinely useful tip plus
  a soft link. Free repeat sales from people who already trust you.
- **Re-offer the upsells:** after someone buys, tag them and pitch the $17 and
  $47 products in a short follow-up automation.

This list is the closest thing to free, compounding, *owned* traffic you'll ever
have — and over time it can become the biggest single driver toward the income
target in the README.
