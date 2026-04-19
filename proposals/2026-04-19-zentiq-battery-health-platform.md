# Zentiq Battery Health Platform

## Proposal

One thing your spec doesn't pin down: how does the technician actually get the battery data into the app? Manual entry from a handheld BMS reader, OBD-II/CAN over Bluetooth, or pulling from a branded diagnostic tool? That decision drives most of the mobile build — manual entry is a week, Bluetooth OBD/CAN parsing is three or four, and it changes what "offline-first in a workshop" looks like.

The config-driven requirement is the right call — I'd put scoring weights, grading thresholds, AI prompts, pricing, and certificate layout blocks into a settings collection the admin edits, not in code. Same for the multi-currency display (GBP stored, FX on render).

Closest thing I've shipped is Clearwell (clearwell.ai) — field techs scanning tanks, AI analysis on the captured data, branded PDF out the other end. Similar shape to what you're describing.

Two things worth a quick call before I scope properly: the data-capture method above, and whether the 8-week MVP includes all EU languages + Arabic RTL + Urdu or if that's phase two. Reply with those and I'll send a concrete plan.

---

## Score

**Bid? MAYBE**
**Overall: 5/10**

- **Fit with my skills:** 8/10 — Flutter + Node + AI + payments + field-tech UX is dead-center for me; Clearwell is a near match.
- **Client quality signals:** 3/10 — "FINAL ULTIMATE v5," emoji headers everywhere, "developer must accept ongoing changes," scope inflation with no discipline. Classic red flags.
- **Competition level:** 6/10 — scope is large and specialized enough that cheap generic bidders will struggle, but UK client + £ budget will attract a lot of bids.
- **Connect ROI:** 4/10 — $5k for this scope is underpriced by 3-4x; even if won, it's a scope-creep trap unless re-scoped hard.

**Verdict:** The work is a real fit and I'd enjoy it, but the spec screams scope creep and the budget is maybe a third of what this actually costs to build properly. Only bid if I can reframe the conversation toward a phased MVP (mobile + certificate + payments first, AI/SaaS/multi-language phase two). Don't boost. If the client won't re-scope on a call, walk.

---

## Notes

**Angle:** Led with the single biggest technical ambiguity in the spec — data capture method — because it's the question that separates bidders who actually read the post from ones who skimmed it. Most will just say "yes I'll build all 23 sections."
**Assumptions:** Assumed client is a non-technical founder (the writing style and "v5 CONTRACT READY" framing suggest it). Assumed they're open to phasing if challenged thoughtfully.
**Flags:** Budget vs. scope is a 3-4x mismatch. "Developer must accept ongoing changes" is a fixed-price scope-creep trap. Spec jumps between UI polish and architectural mandates with no prioritization — a sign the client hasn't made the hard cuts yet. If the discovery call reveals they actually have £5k and want all of this, decline.
**Suggested portfolio item:** Clearwell — it's the same shape (field tech, structured capture, AI analysis, branded PDF certificate). The fit is real, not forced.
