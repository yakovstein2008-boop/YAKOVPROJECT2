# 01 — Your Sitecraft Email, Deliverability & Staying Legal

Read this once before you send a single email. Getting it wrong gets you in the spam
folder (or blacklisted), which is very hard to undo. Getting it right takes about an hour.

---

## A. Setting up your Sitecraft email

I can't create an email account for you (Google requires phone + CAPTCHA verification a
human has to do), but here are your three options, ranked.

### Option 1 — Free Gmail (start here if you want to move today)
- Create something like **`sitecraft.studio.tx@gmail.com`** or **`hello.sitecraft@gmail.com`**.
- Pros: free, instant, Gmail has great default deliverability.
- Cons: less credible than a custom domain, and Gmail caps you (see limits below).
- Good enough to land your first few clients. Many freelancers start exactly here.

### Option 2 — Custom domain + Google Workspace (recommended, ~$6–7/mo)
- Buy a domain (Namecheap, Cloudflare, Porkbun) — ~$10–40/year depending on the name.
  - `.studio` is on-brand but pricier; `.com` is most trusted. Examples: `getsitecraft.com`,
    `sitecraftatx.com`, `sitecraft.studio`.
- Add **Google Workspace** (~$6.30–7/user/mo) → gives you `hello@yourdomain.com`.
- This is what makes you look like a real business and lets you set up SPF/DKIM/DMARC (below).

### Option 3 — Separate "outreach" domain (do this once you scale past ~30 emails/day)
- Pro move: send cold email from a **second** domain (e.g., `trysitecraft.com`) that forwards
  to your main inbox. If cold outreach ever hurts a domain's reputation, it's the throwaway,
  not your primary brand domain. Not necessary on day one.

> **Whatever you choose**, then update the `mailto:` links on your live site so the address on
> the site matches the address you send from. (They currently point to the placeholder
> `hello@sitecraft.studio`.)

---

## B. Authentication: SPF, DKIM, DMARC (only if you use a custom domain)

If you use plain Gmail (Option 1), this is already handled — skip to section C.

If you use a custom domain, set these three DNS records **before** sending. Gmail/Outlook now
quietly junk mail from domains that don't have them:

- **SPF** — says which servers are allowed to send for your domain.
- **DKIM** — cryptographically signs your mail so it can't be forged.
- **DMARC** — tells inboxes what to do if SPF/DKIM fail (start with `p=none`).

Google Workspace gives you copy-paste values for all three in Admin Console → Apps → Gmail →
Authenticate email. Add them at your domain registrar. Verify with a free tool like
mail-tester.com (aim for 9–10/10) before real sends.

---

## C. Warm-up & daily sending limits (the part people skip and regret)

A brand-new inbox that suddenly sends 50 cold emails looks exactly like a spammer. Ramp slowly:

| Week | Cold emails/day (per inbox) |
|------|------------------------------|
| 1–2  | 5–10 |
| 3–4  | 15–20 |
| 5–6  | 30–40 |
| 7+   | ~50 max per inbox |

Data points to hold onto:
- Gmail inboxes that stay **under ~40 cold emails/day** keep inbox-placement above ~85%.
  Push to 100+/day and placement can fall below 50% within two weeks.
- For your volume (handful of clients needed), **5–15 well-personalized emails a day is plenty**
  and keeps you safe.
- Best send windows: **Tuesday–Thursday, ~9–11 AM** local to the prospect. Wednesday 7–11 AM
  is the single best window for *replies*.

**Warm-up tip:** for the first week or two, also send/reply to normal personal emails from the
account and get a few replies — engagement teaches Gmail you're a real person.

---

## D. Deliverability checklist (do these every time)

- ✅ **Plain text, no images, no attachments** in cold emails. They look personal and dodge filters.
- ✅ **No links in the first email** if you can avoid it (or just one). Multiple links = spam signal.
  Your CTA is "want me to send the preview?" — so the link comes *after they reply.* Perfect.
- ✅ **Keep it under ~100 words.** Short = higher reply rate and fewer spam flags.
- ✅ **One clear CTA**, phrased as an easy question.
- ✅ **Avoid spam-trigger words**: "free" in the subject, "guarantee," "100%," "act now," "$$$,"
  ALL CAPS, lots of !!! . (Note: the templates use "preview," not "free," in subject lines on purpose.)
- ✅ **Verify addresses** before sending — bounce rate must stay under ~3%. A tool like
  NeverBounce/ZeroBounce, or just don't guess addresses (use ones listed on their site).
- ✅ **Keep spam complaints near zero** — one complaint per ~1,000 emails can hurt you. The
  "reply STOP and I'll never write again" line keeps people from hitting the spam button.

---

## E. Staying legal — CAN-SPAM (U.S.)

Cold B2B email **is legal** in the U.S., but it's a commercial message, so the CAN-SPAM Act
applies. It's simple — four rules:

1. **Truthful headers & subject line.** Your real name/business in "From," no misleading subjects.
2. **A physical postal address** in the email. A registered **PO box** or a private mailbox
   (UPS Store mailbox) counts — you don't have to expose your home address.
3. **A clear opt-out.** "Reply STOP and I won't email again" works for manual sending, as long
   as you actually honor it. (Tools add a one-click unsubscribe automatically.)
4. **Honor opt-outs within 10 business days** and keep honoring them for at least 30 days.

A compliant footer you can paste under any template:

```
—
{{YourName}}, Sitecraft · {{your email}} · {{your phone}}
{{Your business mailing address — PO box is fine}}
Not interested? Reply "STOP" and I won't reach out again.
```

> If you ever email people in the EU/UK, GDPR/PECR are stricter (you generally need a lawful
> basis and easy opt-out). For now, targeting U.S. local businesses keeps it simple.

---

## F. Tools (optional, for when you scale)

You do **not** need these to start — manual Gmail is fine for your first 50–100 prospects. But
when you want to automate follow-ups and track opens/replies:

- **Sending/sequencing:** Instantly, Smartlead, Lemlist, QuickMail, Saleshandy.
- **Find businesses without sites:** Google Maps by hand (free) or scrapers like Trovn,
  Targetron, Outscraper, Apify "businesses without websites."
- **Verify emails:** NeverBounce, ZeroBounce, MillionVerifier.
- **Test your spam score:** mail-tester.com (free).

---

## Sources

- [Topo — safe sending limits](https://www.topo.io/blog/safe-sending-limits-cold-email) · [Topo — Gmail spam fix](https://www.topo.io/blog/gmail-cold-email-spam)
- [MailReach — how many cold emails per day](https://www.mailreach.co/blog/how-many-cold-emails-to-send-per-day)
- [Instantly — 90%+ deliverability](https://instantly.ai/blog/how-to-achieve-90-cold-email-deliverability-in-2025/)
- [FTC — CAN-SPAM compliance guide](https://www.ftc.gov/business-guidance/resources/can-spam-act-compliance-guide-business)
- [litemail — CAN-SPAM for cold email 2026](https://litemail.ai/blog/can-spam-compliance-guide-for-cold-email-2026)
- [Belkins — subject line study](https://belkins.io/blog/b2b-cold-email-subject-line-statistics) · [Focus Digital — open rates by industry](https://focus-digital.co/b2b-cold-email-open-rates/)
