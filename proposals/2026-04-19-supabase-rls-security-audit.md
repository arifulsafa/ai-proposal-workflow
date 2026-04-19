# Supabase RLS + FERPA Pre-Launch Security Audit

## Proposal

RLS audits on multi-tenant Supabase are where most "pre-launch" reports miss real issues — the policies themselves pass review, but the enforcement leaks through service_role calls in Edge Functions or a `select` that silently bypasses `auth.uid()` because a JOIN pulled rows via a view owned by `postgres`. I assume that's exactly the shape of coverage you need verified across the 11 areas, not just "do the policies exist."

Answering your four:

1. **Flat fee:** $950 for the full scope.
2. **Timeline:** Written pass/fail report delivered within 5 business days of NDA execution + staging access.
3. **Supabase/RLS experience:** I've written and audited RLS for multi-tenant SaaS with role-based isolation (coordinator/supervisor/admin-style splits), including Storage bucket policies and JWT claim validation inside Edge Functions. My usual cross-tenant test harness is a second authenticated client impersonating each role and asserting row counts per policy path — catches the leaks static review misses.
4. **FERPA/HIPAA:** Familiar with both as they apply to SaaS vendors — FERPA's school-official/directory-info distinctions and contractual obligations for education records, and why a platform serving universities in a healthcare-adjacent context typically sits outside HIPAA covered-entity/BA scope absent a BAA with a provider.

Happy to sign the NDA today and start once staging is provisioned.

— Ariful

---

## Score

**Bid? YES**
**Overall: 7/10**

- **Fit with my skills:** 6/10 — Supabase RLS and multi-tenant isolation are in my stack, but I can't claim deep FERPA audit track record; the technical side is solid, the compliance angle is honest-but-thin.
- **Client quality signals:** 8/10 — NDA + IP assignment, clearly scoped 11-part deliverable, specific stack called out, staging-only access (mature operator), US client, payment-verified implied by structured post.
- **Competition level:** 7/10 — The FERPA + Supabase RLS combination filters out generic bidders; the explicit "do not apply if…" language will cut the field hard.
- **Connect ROI:** 6/10 — Flat fee is small (~$800-1500 likely range), so Connects spend matters; <5 proposals so far is good, don't boost.

**Verdict:** Bid without a boost. The client has filtered the field themselves with gatekeeping language and low applicant count — a precise proposal that answers the 4 questions cleanly is likely to make the shortlist. Small ticket but high reply-probability, and the engagement is short and bounded which is fine.

---

## Notes

**Angle:** Opened with the specific class of RLS-audit failure most reviewers miss (service_role bypass + view-owned JOINs), because that's the one line that signals "this person has actually audited Supabase in production, not just written policies."
**Assumptions:** (1) Flat fee $950 is in their expected range — they didn't post a budget; adjust up to $1200-1500 if Ariful wants more margin. (2) That the client will recognize the technical specificity of the hook; if they're non-technical the hook lands weaker but the 4 structured answers carry it.
**Flags:** Small flat-fee engagements can turn into scope creep — the "pre-completed security fixes" language suggests someone already did a first pass, so any finding that requires a fix becomes a negotiation. The 7.75-10.75 hr estimate is tight for 11 areas; if findings require re-testing after fixes, that's out of scope. Also: "healthcare-adjacent" + "not a HIPAA covered entity" is a specific legal posture the client wants agreement on, not debate — the proposal reflects their framing back rather than challenging it.
**Suggested portfolio item:** None — didn't fit naturally. Baketracker has multi-tenant isolation but it's not Supabase, and forcing it in would dilute the security-audit framing.
