# Delivery Setup — instant, automated fulfillment (free)

This is the "autopilot" back half: a buyer pays, and within seconds they get the
product — no human involved, 24/7. We use **Gumroad** because it's free to start
(it takes a small per-sale fee instead of a monthly cost), handles checkout,
payment, taxes/VAT, file hosting, and the delivery email for you.

> Alternatives if you prefer: **Payhip** (similar, free tier), **Lemon Squeezy**
> (acts as merchant of record, great for global tax), or **Stripe Payment Links**
> + a delivery tool. Gumroad is the fastest to launch. The steps below map
> cleanly onto any of them.

---

## Step 1 — Prepare the product file (10 min)

The product lives in `../product/` as Markdown + a CSV. Buyers prefer one tidy
download. Do one of these:

- **Easiest:** Zip the entire `product/` folder → `AI-Job-Search-Toolkit.zip`.
- **More polished:** Convert each `.md` to PDF first (use any free Markdown-to-PDF
  tool, VS Code's "Markdown PDF" extension, or just open in a browser and
  Print → Save as PDF), then zip the PDFs + the CSV.

Either way you end up with **one file to upload.** Keep the `00-START-HERE`
document as the first thing they see.

---

## Step 2 — Create the Gumroad product (10 min)

1. Sign up free at gumroad.com and complete payout details (so you actually get
   paid). This is the one step that needs your real info.
2. **New Product → Digital Product.**
3. **Name:** `The AI Job Search Toolkit`
4. **Price:** `27`
5. **Upload** your zip/PDF bundle as the content.
6. **Cover image:** make a simple one free in Canva (a bold title on a clean
   background — no photo of you needed). 600×600 or 1280×720.
7. **Description:** paste the short version below.

```
Beat the resume robots, write tailored cover letters in 2 minutes, optimize your
LinkedIn to attract recruiters, walk into interviews already knowing the
questions, and negotiate a higher salary — all with free AI you already have.

Includes 7 modules: the ATS Resume System, ATS-safe templates, a Cover Letter
Prompt Pack, the LinkedIn Optimizer, the Interview Prep Pack, Salary Negotiation
Scripts, and an Application Tracker. Every prompt is copy-paste. Works with free
ChatGPT, Claude, Gemini, or Copilot.

Instant download. 30-day money-back guarantee.
```

---

## Step 3 — Turn on the automated welcome email (5 min)

In your product settings, find **"Content" → receipt/email** (Gumroad calls it
the product's post-purchase email or "Updates"). Paste the message from
[welcome-email.md](welcome-email.md). This sends automatically on every sale —
this is your fulfillment running itself.

---

## Step 4 — Add the order bump (5 min, optional but high-ROI)

Gumroad lets you offer a second product at checkout ("bump") or after
("upsell"). Even a simple `$17` add-on attaches to a meaningful share of orders
and raises your revenue per visitor with zero extra traffic. See
[upsell-ladder.md](upsell-ladder.md) for what to offer.

---

## Step 5 — Connect it to your sales page (2 min)

1. Copy your Gumroad product URL (looks like `https://yourname.gumroad.com/l/xxxx`).
2. Open `../sales-page/index.html`, find both `BUY_URL` placeholders, and replace
   them with that link.
3. Deploy `index.html` free (drag the folder into Netlify Drop, or push to
   Vercel/Cloudflare Pages/GitHub Pages).

> You can also skip the custom page entirely and send traffic straight to the
> Gumroad page — it's hosted and converts fine. The custom page is for when you
> want more control and a cleaner brand.

---

## You now have a complete money machine

A stranger can find your page, read it, click buy, pay, and receive the product
— while you sleep. The only thing left is pointing people at the page. That's
[../marketing/traffic-playbook.md](../marketing/traffic-playbook.md).

### Test it once before you promote it
Use Gumroad's preview / make a $0 test or buy it yourself with a discount code,
and confirm: checkout works → file downloads → welcome email arrives. Fix any
gap now, not after you've sent 500 people.
