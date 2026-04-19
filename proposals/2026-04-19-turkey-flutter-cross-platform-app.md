# Turkey Flutter Cross-Platform App (Mobile + Web)

## Proposal

One thing worth nailing down before I quote: how do you want subscription entitlements to sync between RevenueCat (mobile) and Stripe (web) when the same user pays on one and logs in on the other? This is the part that quietly eats weeks on projects like this — RevenueCat has no web SDK, so the usual fix is a Firestore `entitlements` doc written by both a RevenueCat webhook and a Stripe webhook, with the client reading from Firestore as the single source of truth. Worth agreeing on upfront.

Stack-wise your choices are solid — BLoC + Clean Architecture + go_router scales cleanly, and Firestore fits the content/favorites/admin-panel shape. A couple of things I'd flag from experience: Flutter web has real quirks around Firebase Auth persistence and bundle size that are worth budgeting for, and Firestore security rules for the admin-panel side need to be designed before you write a line of UI or you'll repaint them later.

Happy to jump on the intro call, or reply with answers to the entitlement-sync question and the scope of the admin panel and I'll put together a concrete plan and phased estimate.

---

## Score

**Bid? MAYBE**
**Overall: 5/10**

- **Fit with my skills:** 7/10 — Flutter + Firebase + dual-payment (Stripe + RevenueCat) is squarely in my wheelhouse; I've shipped RevenueCat with server-side validation multiple times.
- **Client quality signals:** 4/10 — "Budget is flexible" on a 3-6 month build is a soft red flag; Turkey-based clients on Upwork skew toward lower rates; no prior hire info in the post.
- **Competition level:** 4/10 — Generic Flutter + Firebase jobs attract hundreds of low-cost-region bidders; not niche enough to filter.
- **Connect ROI:** 4/10 — No stated budget + high competition + long project = high Connect risk for uncertain return.

**Verdict:** Technically a good fit, but the economics are shaky. The "budget is flexible" framing on a half-year project usually means they're shopping for the cheapest bidder who can sound senior. Bid without boosting, and only if the hook gets a substantive reply — don't chase.

---

## Notes

**Angle:** Opened with the RevenueCat/Stripe cross-platform entitlement sync question because (a) it's a real engineering problem on this exact stack that 90% of bidders will miss, (b) it proves I've actually built this before, and (c) it forces a substantive reply instead of a yes/no.
**Assumptions:** Assumed a single user account spans mobile and web (standard for this kind of app). Assumed they want one subscription to unlock content across all three platforms, not separate subs per platform. Verify both.
**Flags:** "Budget is flexible" + "3 to 6 months" + no hire history visible + Turkey market = high probability of a budget far below what this scope actually costs. Also: "full project details will be shared after a brief introductory call" is a mild flag — either they have a solid spec they're gatekeeping, or they're still figuring it out and the call is exploratory.
**Suggested portfolio item:** None — didn't fit naturally. Yum AI / Travy / Unfold Us all use RevenueCat but none are Flutter-web cross-platform. Forcing one in would have weakened the hook.
