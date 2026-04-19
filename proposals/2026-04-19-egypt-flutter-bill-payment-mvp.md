# Egypt Flutter Bill Payment & Recharge MVP

## Proposal

The part of this that'll determine whether the MVP actually works on day one isn't the Flutter app — it's the recharge/biller APIs. Vodafone/Orange/Etisalat/WE don't have one unified API; you either go through an aggregator (Fawry, Masary, Bee, Khales) or negotiate direct integrations, which usually isn't realistic for an MVP. Which route are you on? That single decision changes the timeline by weeks.

A few things worth clarifying before I scope:

- Do you already have merchant accounts with the aggregator and Paymob, or does onboarding still need to happen? Paymob's approval alone can take 2-3 weeks.
- For "transaction status," are the biller APIs webhook-based or do we need a polling + reconciliation job? Pending states are where these apps leak money if handled wrong.
- Is the admin dashboard part of the MVP budget, or can it be a thin Next.js panel we extend later?

I've built the marketplace + Stripe Connect + webhook-reconciliation side of this shape before (Explore Bless), so the payment state machine isn't new territory for me.

If you can answer those three, I can come back with a real timeline and fixed price — happy to do that over a 15-min call or just here in chat.

---

## Score

**Bid? NO — 3.5/10**
**Overall: 3.5/10**

- **Fit with my skills:** 6/10 — Flutter + backend + payment integration is in my stack, but I have no Egyptian biller/aggregator experience (Fawry, Masary, Paymob), which is the core of this job.
- **Client quality signals:** 3/10 — Egypt-based, no budget mentioned, emoji-heavy checklist-style post, explicitly asks for "cost estimation" upfront which signals price-shopping, and "Fawry-style simple UI" suggests expectations of a very cheap build.
- **Competition level:** 3/10 — Flutter MVP + bill payment is one of the most crowded job types on Upwork; dozens of Egypt/India/Pakistan agencies with prior biller integrations will underbid me.
- **Connect ROI:** 3/10 — Likely budget is $1.5-4k, competition is fierce, my domain-specific edge is weak. Connect-to-reply ratio will be poor.

**Verdict:** Skip this one. You don't have Egyptian biller/aggregator experience, the client didn't post a budget (almost always means low), and local agencies with Paymob + Fawry relationships will win on both price and credibility. Save the Connects for a job where your mobile + AI + real-time edge actually matters. Definitely don't boost.

---

## Notes

**Angle:** Led with the aggregator-vs-direct API question because that's the single biggest unknown in any Egyptian recharge/bill-pay MVP — most devs bidding will skip past it and just say "yes Flutter, yes Paymob." Raising it proves domain awareness instantly.
**Assumptions:** Assumed the client doesn't already have aggregator contracts signed (most MVP-stage clients don't). Assumed they haven't thought through webhook vs polling for transaction status. If either is wrong, the proposal still reads as informed.
**Flags:** (1) "Build from scratch" + full biller integrations + Paymob + admin dashboard + iOS/Android is not a small MVP; if budget is under ~$5-8k this is a scope/price mismatch. (2) No budget mentioned. (3) Checklist-style post format attracts low-ball bids and signals a price-first client. (4) Egypt-based + asking for "cost estimation" usually means local agencies undercut anyone above $2k. (5) "Similar to Fawry" is a tell — the client wants a clone at clone pricing.
**Suggested portfolio item:** Explore Bless — referenced lightly for the payment state machine / webhook reconciliation pattern. Didn't force a closer match since none of the portfolio projects are bill-payment specific.
