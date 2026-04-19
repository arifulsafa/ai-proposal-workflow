# UAE Family Tree App — RN/Flutter + OTP + Graph Backend

## Proposal

Two things in your spec are worth nailing down before anyone quotes this properly.

First, the data shape. A family tree is a graph, not a document tree — Firestore will work for the first few thousand users, but "show me everyone within 3 hops of user X" gets expensive fast. For something meant to scale, I'd lean toward Postgres with a proper relationships table (or Neo4j if the tree queries get really deep) and a Node/Fastify API, rather than Firebase as the primary store. Happy to do Firebase if you'd rather — just want you to see the tradeoff.

Second, the placeholder-user problem. When User A adds "my uncle" as an inactive node, and later User B independently adds the same person, how do you dedupe on signup? Phone number match is the obvious answer, but you'll want a merge/claim flow or you'll end up with duplicate branches. This is the part most devs skip in the quote and then surprise you with later.

On OTP — WhatsApp OTP via Twilio or Meta's Cloud API is doable; SMS is simpler and cheaper. I'd default to SMS and add WhatsApp as a fallback.

Stack I'd recommend: React Native, Node.js/Postgres, interactive tree rendered with react-native-skia or a d3-force layout (lazy-loaded per subtree).

If you reply with rough user-count target and whether you already have a backend preference, I can come back with a concrete scope and timeline.

---

## Score

**Bid? YES**
**Overall: 7/10**

- **Fit with my skills:** 8/10 — Mobile + backend MVP with a real architectural question (graph data at scale). Sweet spot.
- **Client quality signals:** 5/10 — UAE, "Budget: TBD", no prior hire info visible, post is clear but generic. Could go either way.
- **Competition level:** 7/10 — "Family tree app" attracts generic bidders, but the graph-scale + dedupe nuance is where I can differentiate.
- **Connect ROI:** 6/10 — No stated budget is the main risk. If they respond, the scope is meaty enough to be worthwhile.

**Verdict:** Bid, don't boost. The hook (graph vs. Firebase + placeholder dedupe) is specific enough to stand out from template proposals, and this is genuinely in my stack. Skip boost until the budget question gets answered — "TBD" from a UAE first-time poster is too risky to double-spend Connects on.

---

## Notes

**Angle:** Led with the graph-data-at-scale question because the client explicitly called out scalability as critical, and Firebase-for-graphs is the #1 thing that bites these projects at ~10k+ nodes. The placeholder-dedupe flag is the second-most-senior observation I can make on this post — it proves I actually thought about the user flow, not just the tech.

**Assumptions:** (1) Client will care about the tradeoff rather than being locked into Firebase — if they're already Firebase-committed I'd adjust. (2) They haven't thought about the dedupe-on-signup problem yet. (3) SMS is acceptable as primary OTP given UAE market — WhatsApp is nice-to-have, not must.

**Flags:** Budget "TBD" is the main concern. UAE clients can be excellent or chronic lowballers; no way to tell from the post alone. "Build me a full app for Android & iOS with backend" with no budget is a flag worth verifying before sinking real scoping time in.

**Suggested portfolio item:** None — didn't fit naturally. Nothing in my portfolio is a graph/social-relationship app specifically; forcing Clearwell or Baketracker here would have been a stretch. Better to earn credibility with the technical observations and fall back to portfolio in the reply.
