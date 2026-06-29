# Launch Day — your first 60 minutes, in order

Run this top to bottom the day your store goes live. It takes you from "Gumroad
products exist" to "live, connected, and driving traffic." Check each box.

---

## Phase 0 — Pre-flight (you should already be here)

- [ ] Gumroad payout details added (Settings → Payments).
- [ ] All 3 products created and **published**:
  - [ ] The AI Job Search Toolkit — $27
  - [ ] The Recruiter Outreach Pack — $17
  - [ ] The Interview Mastery Pack — $47
- [ ] Order bump (Recruiter Pack) attached to the $27 toolkit.
- [ ] Upsell (Interview Pack) attached to the $27 toolkit.

> Copy used: `delivery/gumroad-copy.md`. Setup walkthrough: `delivery/gumroad-setup.md`.

---

## Phase 1 — Test the machine before anyone sees it (10 min)

Never send traffic to an untested checkout.

- [ ] Create a **100%-off discount code** on the $27 toolkit.
- [ ] Buy it yourself with the code, and confirm **all four**:
  - [ ] The **order bump** shows at checkout.
  - [ ] The **upsell** appears right after purchase.
  - [ ] The **files download** correctly (open one — make sure it's the real content, not an empty/wrong zip).
  - [ ] The **receipt / after-purchase email** arrives.
- [ ] Fix anything broken now. Then **delete or disable the 100%-off code** so the public can't use it.

---

## Phase 2 — Connect the link (the funnel comes together) (15 min)

You now have your product URL: `https://yourname.gumroad.com/l/xxxx`. Wire it in.

- [ ] **Sales page:** open `sales-page/index.html`, replace all **3** `BUY_URL`
      placeholders with your Gumroad link. (The deploy-ready copy at
      `.deploy/index.html` uses `#offer` — update the real `sales-page` file, then redeploy.)
- [ ] **Deploy the page** free (Netlify Drop is fastest — drag the folder), or
      skip the custom page for v1 and just use Gumroad's hosted page.
- [ ] **Email sequence:** in your MailerLite/Brevo automation, replace every
      `[LINK]` with your product URL and `[Your name]` with your name across all 5 emails.
      (Guide: `delivery/email-automation-setup.md`.)
- [ ] **Lead magnet:** confirm Email 1's `[download link]` points to the hosted
      checklist PDF, and the signup form is live.

> Decide your "money link" — the one URL you'll put everywhere. Either your
> deployed sales page **or** the Gumroad product page. Pick one and be consistent
> so you can track what works.

---

## Phase 3 — Set up tracking (5 min)

You can't improve what you can't see.

- [ ] Note your starting numbers (all zero — that's fine). Gumroad shows
      **views** and **sales** per product.
- [ ] If using the custom page, add a free analytics snippet (or just rely on
      Gumroad views for v1).
- [ ] **Use a different link per channel** where you can (Gumroad lets you add
      `?ref=pinterest`, `?ref=reddit`, etc.) so you learn which channel actually
      drives buyers — that's the data that tells you where to double down.

---

## Phase 4 — Go live with traffic (20 min)

The store is ready. Now point attention at it. This is the part that produces sales.

- [ ] Open `marketing/week-one-posts.md` → post **Day 1** everywhere you can:
  - [ ] One short-form post (X / Threads / LinkedIn / Bluesky).
  - [ ] One Pinterest pin (make the graphic free in Canva using the pin title).
- [ ] Put your **money link** (or the free lead-magnet form) in **every profile bio**.
- [ ] Find **2–3 genuine questions** on Reddit (r/jobs, r/resumes, r/careerguidance)
      or Quora and leave a real, helpful answer — link only where the sub allows it.
- [ ] Pin/bookmark `marketing/week-one-posts.md` — tomorrow you post Day 2. Same time each day.

---

## Phase 5 — Done for the day. Walk away.

- [ ] You launched. The machine is live and can take money 24/7 without you.
- [ ] Tomorrow: post Day 2. Repeat daily.
- [ ] Friday: open `automation/the-loop.md` and run the weekly review.

---

## What "success" looks like at each stage (so you don't panic)

| Timeframe | Realistic, healthy signal | What it does NOT mean |
|---|---|---|
| Day 1 | A few visitors, maybe 0 sales | That it's broken. Day 1 is almost always quiet. |
| Week 1 | First clicks, possibly first sale, list signups trickling in | That you should quit if no sale yet — keep posting. |
| Weeks 2–4 | Pinterest/SEO start compounding; sales become semi-regular | — |
| Month 2–3 | A repeatable trickle you can amplify by doubling the winning channel | — |

If after ~2 weeks of daily posting you have traffic but **no sales**, the problem
is the **page or price framing**, not the traffic — tighten the headline and
re-test. If you have **sales but tiny traffic**, the funnel works; pour energy
into the channels (Phase 4) to scale volume.

---

## The one rule for launch day

**Done beats perfect.** A live store with an untested cover image and one Day-1
post beats a "perfect" funnel that never launches. Get it live today. Improve it
with real data this week. That's the whole game.
