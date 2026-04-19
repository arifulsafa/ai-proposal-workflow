# Field Media SFTP Upload App (iOS + Android)

## Proposal

SFTP from mobile is the part most devs underestimate on jobs like this — iOS and Android don't have native SFTP clients, so the library choice matters, and sessions get killed when the app backgrounds mid-upload unless you wire it into a background task. Worth flagging because field users are usually on spotty cell signal, and "upload failed, start the whole batch over" is the #1 reason these apps get abandoned.

I'd build it in React Native — one codebase for both platforms, solid SFTP + background-upload libraries, and it keeps your long-term maintenance cheap. Each upload writes to `username_YYYYMMDD_HHMMSS/` with the media files plus `description.txt`, exactly as you spec'd. Progress UI with per-file status, human-readable errors on failure (host unreachable, auth failed, path not writable, etc.) so your users can actually pass something useful to support.

Clearwell (clearwell.ai) is the closest thing I've built — field techs capturing photos, app handling flaky connections and syncing when back online.

**Fixed price: $550. Timeline: 8–10 days from SFTP credentials in hand to TestFlight + Android internal track builds you can install privately before store submission.**

Two quick questions before I start: (1) any max file size or video length I should design the progress UI around? (2) is Play Store submission in scope, or just TestFlight/APK for private testing?

---

## Score

**Bid? YES**
**Overall: 6/10**

- **Fit with my skills:** 8/10 — field mobile + media capture + flaky-network handling is squarely in my lane (Clearwell pattern).
- **Client quality signals:** 5/10 — post is well-written and specific, but mixed hourly/fixed-bid signals and no budget anchor. Worldwide client, no history visible in the post.
- **Competition level:** 5/10 — "simple app" posts pull 50+ bids; the SFTP-from-mobile angle filters the copy-paste crowd but scope is small enough for cheap bidders to undercut.
- **Connect ROI:** 5/10 — $550 contract is small but the work is 1.5–2 weeks part-time; reasonable return for 6–10 Connects, not worth boosting.

**Verdict:** Clean technical fit, concrete price, specific hook. Bid without boost. If the client replies engaged, this is a quick, clean job that closes well — Top Rated + a real portfolio match should carry it against the race-to-bottom bids.

---

## Notes

**Angle:** Led with the one technical detail (mobile SFTP + backgrounding + flaky networks) that the 50 copy-paste bidders will miss. Then locked in the fixed price upfront so the client doesn't have to guess.
**Assumptions:** $550 ≈ 27 hrs × $20 — assumes resumable/chunked uploads are out of scope (retry-batch-on-failure is acceptable). If they want resumable for video over LTE, price goes up ~$150. Also assumed iOS + Android both needed.
**Flags:** (1) Post tagged "Hourly" in metadata but body says fixed bid — minor. (2) No SFTP host specifics (key-only auth? non-standard port? jailed user?) — shouldn't blow up scope but worth confirming in the first reply. (3) "Less than 30 hrs/week" on a ~27-hour job is fine.
**Suggested portfolio item:** Clearwell — field-techs-in-unreliable-conditions shape matches almost exactly.
