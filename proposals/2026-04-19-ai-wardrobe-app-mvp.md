# AI Wardrobe App MVP

## Proposal

Before I quote — how are you planning to represent each uploaded outfit to the AI? Most wardrobe MVPs fork here: either you run CV attribute extraction on the user's photo (color, category, pattern, sleeve length, etc.) and reason over structured tags, or you embed the images directly and do vector similarity for "what goes with this." The first is cheaper and more controllable; the second generalizes better but is harder to debug when suggestions feel off.

For $2k scope I'd push toward the tagged-attribute approach — GPT-4 vision on upload to extract a structured schema, store it in Postgres, then suggestion prompts work off tags rather than raw embeddings. Keeps cost per user low and makes the "why did it suggest this" explainable.

Stack I'd reach for: React Native (iOS + Android from one codebase), Node/Fastify backend, Postgres, S3 for image storage, OpenAI for the vision + suggestion calls. Built the multi-vector recommender for a production social app recently, so if you do want the embedding route I've done both.

A few things I'd want to pin down before scoping properly: which platforms (iOS only or both), what counts as a "suggestion" (occasion-based, weather-based, just similar items?), and whether users upload individual garments or full outfit photos. Reply with those and I can send a concrete breakdown tomorrow.

---

## Score

**Bid? MAYBE**
**Overall: 5/10**

- **Fit with my skills:** 8/10 — Mobile + AI vision + recommendations is squarely in my lane; recent Bless feed work is directly relevant.
- **Client quality signals:** 3/10 — Vague post, generic "fashion tech" framing, no specifics on stack, users, or monetization. "Expert" tier + "willing to pay higher" is boilerplate.
- **Competition level:** 4/10 — AI wardrobe apps are a popular MVP category; every generalist bidder will throw their hat in.
- **Connect ROI:** 4/10 — $2k fixed is underpriced for a real MVP with AI, auth, storage, and two platforms. Likely to either balloon in scope or get won by someone underbidding.

**Verdict:** Skill fit is strong but the economics are weak. $2k fixed for a mobile app + backend + AI integration is about half what this should cost, and the post gives no signal that the client understands the scope. Only worth a bid if you have spare Connects — do not boost. The hook is strong enough that if they're savvy, they'll reply; if they ghost, you've lost little.

---

## Notes

**Angle:** Lead with the single real architectural fork in any wardrobe app (CV-tagged attributes vs. raw image embeddings) — it immediately separates me from everyone writing "I'll build your AI wardrobe app!"
**Assumptions:** That the client hasn't thought through the AI representation problem yet, and that "outfit suggestions" means combining wardrobe items rather than shopping recommendations. Verify both.
**Flags:** Budget is light for scope. "Complex project" tag + $2k fixed + two platforms + AI = scope creep risk or dropout risk. No mention of existing designs, auth system, or what "seamless user flow" means concretely.
**Suggested portfolio item:** Bless feed engine (multi-vector recommender) — referenced generically as "production social app" since the client probably doesn't need the full Twelve Labs detail. Yum AI would also fit if they lean into the scraping/normalization angle, but wardrobe is user-uploaded so that's less relevant.
