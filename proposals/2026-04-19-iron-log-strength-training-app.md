# Iron Log — Strength Training App

## Proposal

The active workout screen is the whole app — that's where Hevy, Strong, and Boostcamp either win or lose users, and it's where most devs underestimate the work. Ten set types (Myo Reps, Drop, Superset, Giant, Cluster, Iso Hold, etc.) each need slightly different input affordances, and cramming them into one screen without a modal maze is the actual design problem.

Being upfront on the $2k side: for a cross-platform build with this scope, that's MVP-scoped, not full-spec. I'd go Flutter for single-codebase iOS + Android and the animation polish a "premium dark" aesthetic needs, and I'd push to cut v1 down to: active workout + all 10 set types, routine builder, basic progress view, local-first storage with cloud sync deferred. Blocks/deload and calendar land in v1.1.

A couple things worth nailing before I commit:

- Do you already have a routine/block data model sketched, or are we designing that too? Deload logic interacts with how blocks are structured.
- Offline-first is non-negotiable for a lifting app (logging mid-set with no signal) — are you planning auth + cloud backup in v1, or local-only to start?
- Any wearable work planned (Apple Health, Watch rest timers), or pure phone for now?

Send over wireframes or a Figma if you have them and I'll come back with a concrete scoped plan. Otherwise 15 minutes on a call and I can tell you what $2k actually buys here.

---

## Score

**Bid? MAYBE**
**Overall: 4/10**

- **Fit with my skills:** 8/10 — Mobile-first full-stack MVP with a hard UX core (set-type state management) and offline sync; exactly my lane.
- **Client quality signals:** 3/10 — $2k for cross-platform iOS + Android with this feature list is a mismatch. Either the client is underpricing because they don't know, or they're fishing for low-cost-region bidders.
- **Competition level:** 3/10 — At $2k budget this post gets flooded with sub-$15/hr bidders from regions I can't compete with on price. Domain specificity won't save it.
- **Connect ROI:** 3/10 — Max contract ceiling ~$2k. Even winning it is a mediocre return, and the odds are low against the price-competitive bid pool.

**Verdict:** Lean skip, but the post is specific enough that a scope-reality proposal might stand out if the client is coachable. Only bid if Connects are plentiful. Don't boost. If they reply, the first conversation is about trimming scope to v1, not about starting work.

---

## Notes

**Angle:** Named the real hard problem (set-type UX) and led with budget honesty — $2k for this scope on two platforms is a mismatch, so pretending otherwise would set up a failed project. Scope-reality framing filters for a coachable client.
**Assumptions:** Assumed greenfield, no existing codebase, no design system yet, and that the client is a lifter (the set-type list is too specific otherwise). Also assumed the $2k budget is a ceiling they'd be willing to stretch if scoped properly — if it's truly fixed, this is not winnable at a rate I work for.
**Flags:** $2k for cross-platform iOS + Android with 10 set types, routine builder, block/deload planning, calendar, progress tracking, and dashboard is a 3-5x underquote. Either the client doesn't know the real cost (fixable in conversation) or is shopping price (not fixable). "Premium, dark, performance-focused" at $2k is especially suspect — polish is expensive. Category is saturated (Hevy, Strong, Boostcamp, Fitbod).
**Suggested portfolio item:** None — didn't fit naturally. Clearwell has offline-first mobile patterns but forcing a water-tank-inspection reference into a lifting app would hurt more than help.
