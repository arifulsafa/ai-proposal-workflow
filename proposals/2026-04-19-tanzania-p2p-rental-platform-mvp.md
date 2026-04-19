# Tanzania P2P Rental Platform MVP

## Proposal

Two things worth sorting out before I give you a firm number, because they change the scope meaningfully:

1. For the map — Google Maps looks best but the pay-per-load bill grows fast once you have real traffic in Tanzania. Leaflet + OpenStreetMap gives you the same Airbnb-style experience for free and scales without a cost ceiling. For an MVP targeting East Africa I'd default to Leaflet and only swap in Google if you need Places autocomplete later.
2. Booking flow — is this request-to-book (owner approves each one) or instant-book? That decision shapes the entire calendar/availability model and is painful to change later.

Stack I'd use: Next.js + Postgres with PostGIS for the geo queries (finding listings inside a map viewport), Cloudflare R2 or S3 for photos/videos. Boring in a good way — cheap to host, clean path to M-Pesa escrow in phase 2, and the same backend cleanly powers a mobile app later without a rewrite.

Ballpark for phase 1 as described: ~120-160 hours at $13/hr, 5-7 weeks part-time or 3-4 weeks if I go full-time. I've shipped a similar two-sided marketplace before (Explore Bless — hosts, customers, bookings, split payments) so the shape is familiar. Answer the two questions above and I can tighten that into a real phased plan tomorrow.

---

## Score

**Bid? YES**
**Overall: 7/10**

- **Fit with my skills:** 8/10 — Two-sided marketplace with bookings + map is squarely in my wheelhouse; Explore Bless is a direct analogue.
- **Client quality signals:** 7/10 — Canadian client (Western rate expectations), clear vision, phased thinking, realistic about starting simple and scaling. $20 top of band is in line with what I quote.
- **Competition level:** 7/10 — MVP marketplace posts attract bulk bidders, but PostGIS + map UX + M-Pesa future phase filters out the template-bid crowd.
- **Connect ROI:** 7/10 — 1-3 months at 30+ hrs/wk at the top of the band is solid. Worth bidding; boost if Connects are available.

**Verdict:** Bid. Canadian client changes the calculus from the Tanzania-pricing worry — $13/hr is well inside their posted range and reads as fair rather than cheap, which is actually good positioning here (cheaper than their $20 ceiling, backed by Top Rated + 1000 hours). Consider boosting if you have Connects — the combination of strong fit, long duration, and a thoughtful client is worth the extra visibility.

---

## Notes

**Angle:** Led with two real scoping questions (map provider + booking model) because both are genuinely ambiguous in the post and getting them wrong costs weeks. The $13/hr quote lands mid-range — below the $20 ceiling, comfortably above the $8 floor — which positions you as a sensible pick rather than either a discount or a premium.
**Assumptions:** That the client hasn't thought about Google Maps cost scaling (likely true for a non-technical founder targeting East Africa). That "booking system" is underspecified. That a 120-160 hour ballpark for phase 1 is defensible — if they confirm instant-book + richer filters + payment rails in phase 1, that number creeps up.
**Flags:** "Competition website:" line was left empty, which is mildly sloppy. M-Pesa escrow in phase 2 is realistic but non-trivial — flag it explicitly as its own scoped project later, not an afterthought bolted on. Hourly contracts with non-technical founders can drift; fixed phase milestones keep scope honest.
**Suggested portfolio item:** Explore Bless — direct two-sided marketplace with bookings and split payments. Natural fit, didn't force it.
