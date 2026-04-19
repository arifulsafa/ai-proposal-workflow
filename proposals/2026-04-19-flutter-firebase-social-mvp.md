# Flutter + Firebase Social App MVP

## Proposal

On the duplicate-vote question — the right answer in Firestore isn't a `votes` array on the post doc, it's a subcollection `posts/{postId}/votes/{userId}` where the doc ID *is* the voter's UID. That makes duplicate voting structurally impossible (a second vote overwrites, it can't stack), keeps security rules trivial (`request.auth.uid == userId`), and lets you maintain `upvoteCount`/`downvoteCount` on the post via a Cloud Function trigger so the feed stays fast without reading every vote doc.

On scope: auth + post create (text+image) + feed + voting + profile is realistically 3–4 weeks of focused work if the UI stays clean-simple as you described. The parts that usually blow timelines aren't in your list — image compression/resizing before Storage upload, feed pagination once there's real data, and offline behavior. Worth agreeing early whether those are MVP or v1.1.

Flutter + Firebase is most of what I ship on the mobile side. Happy to take the test task — a post-create screen wired to Firestore + Storage with working upload/retrieve is a half-day job and a fair way for you to check code quality before committing further.

What image sizes are you expecting on posts, and is the feed chronological or ranked by votes?

---

## Score

**Bid? YES**
**Overall: 7/10**

- **Fit with my skills:** 8/10 — Flutter + Firebase + social feed is squarely in scope; voting dedup is a small architecture question I've answered many times.
- **Client quality signals:** 7/10 — clear scope, milestone structure, specific questions, stated budget. Slight minus for "paid test task" framing which can skew low-paying.
- **Competition level:** 4/10 — Flutter + Firebase + social MVP is one of the most crowded job categories on Upwork; will attract 50+ bidders from low-cost regions.
- **Connect ROI:** 6/10 — $3k ceiling split into milestones is decent but not huge; the test-task gate means Connects spent before real contract.

**Verdict:** Bid without boosting. The hook (exact Firestore schema for vote dedup) directly answers their filter question in the first line, which is how you beat 50 generic bidders here. Don't inflate the timeline — this client has thought about scope and will spot padding.

---

## Notes

**Angle:** Led with the exact Firestore schema answer to their #2 question. That's the technical filter they're using to weed out tutorial-level bidders, so answering it concretely in sentence one does more than any credential.
**Assumptions:** That they want a real, defensible technical answer over marketing. Also that "small paid test task" means actually paid (not "free to prove yourself") — if it turns out to be unpaid, I'd pass.
**Flags:** $3k for full MVP (auth + posts + images + feed + voting + profile) is tight — workable if UI stays genuinely simple, but image handling and pagination often balloon. Also: "work-for-hire, I retain full ownership" is fine but worth confirming in the contract, not just the post. High competition category.
**Suggested portfolio item:** None — didn't fit naturally. TBeauty is the closest shape (feed + social) but it's React Native, not Flutter, so referencing it would weaken rather than strengthen the pitch.
