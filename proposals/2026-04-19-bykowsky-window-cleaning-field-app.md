# Bykowsky Window Cleaning — Internal Field App V1

## Proposal

A few things worth pinning down before I quote, because they'll shape the V1 architecture more than the feature list will:

1. Offline. Techs lose signal on-site constantly — is this app expected to let them complete the checklist + capture photos with no connection and sync later? That's a different build than an always-online web form, and getting it wrong means lost data on the "opening night" jobs.
2. Photos. Raw phone shots are 3-5MB each; a property with all four sides + issue closeups is easily 30+ photos per job. Are we compressing on-device before upload, and do you want originals retained for the PDF or just the compressed versions?
3. Report output. "Branded PDF" is the V1 deliverable — do you have a design for it already, or should I mock one from the checklist structure?

I'd build this as a React Native app (iOS + Android from one codebase) with Firestore + Cloud Storage for the backend, since you already mentioned Firestore — that keeps auth, offline cache, and file uploads native to the stack. PDF generation server-side via Cloud Functions so the branding stays consistent.

Clearwell (clearwell.ai) is the closest thing I've shipped — field inspections, on-site photo capture, offline-first sync. Happy to walk you through how it handles the flaky-connection case.

Reply with answers to those three and I can give you a fixed scope + timeline for the 3-user V1 by tomorrow.

---

## Score

**Bid? YES**
**Overall: 7/10**

- **Fit with my skills:** 9/10 — field inspection app with photos, checklist, offline, PDF reports is almost exactly Clearwell.
- **Client quality signals:** 6/10 — well-written brief, clear V1 scope, thinks about scalability. No budget stated and no hire history visible in post. Worldwide posting attracts heavy competition.
- **Competition level:** 6/10 — sounds like generic "field app" work on the surface, but the offline + PDF generation piece filters out template bidders.
- **Connect ROI:** 6/10 — likely $3-6k V1 contract if the client is serious. Worth bidding without a boost unless I see it's high-competition at post time.

**Verdict:** Strong skill fit and a clear brief — the client has thought about this, which is rare. No budget is a flag but the spec is specific enough that they probably have one in mind. Bid without boosting; if they reply, the Clearwell reference should close the credibility gap fast.

---

## Notes

**Angle:** Led with the three questions a senior dev would actually ask before scoping — offline, photo handling, PDF design — because the brief is well-written but doesn't answer them, and those three decisions are where most field-app MVPs get the architecture wrong.
**Assumptions:** Assumed the client wants iOS + Android (not web-responsive only), based on "field based" + "mobile app" wording. Assumed no existing PDF design. Assumed they meant Firestore literally, not as a placeholder.
**Flags:** No budget mentioned. "Worldwide" posting = more bidders from low-cost regions on what looks like generic CRUD work. "3 or less users to start" is tiny — if they don't pay premium for the V1 process, the project economics are thin. Also: "partner portals, billing, scheduling" is flagged as future scope, which is fine, but watch for scope creep into V1.
**Suggested portfolio item:** Clearwell — matches the field-ops + photo capture + AI-adjacent pattern almost exactly. Mentioned the live link once, didn't pad.
