# Portfolio & Skills Reference (for the proposal agent)

This file is structured for the proposal generator to pattern-match job posts against real work. When writing a proposal, first scan the **Job-Type → Reference** table, then pull the matching portfolio entry and any skill notes. Only reference a project if it genuinely fits — a forced link is worse than none.

---

## 1. Positioning (one-paragraph self-summary)

Toronto-based senior engineer, 5+ years, Top Rated on Upwork (100% JSS, 1000+ hrs). Mobile-first full-stack: I own app, API, database, and deploy end-to-end so clients don't hire three freelancers for an MVP. Strongest edges: hardware-adjacent mobile (camera, GPS, scanning, offline sync, widgets, push), real-time systems under load (Socket.IO, BullMQ, Redis), and AI integration (OpenAI SDK, pgvector, Twelve Labs, ElevenLabs, n8n). Shipped apps to millions of users and driven $100k+ in client revenue.

---

## 2. Job-Type → Portfolio Reference (quick lookup)

| If the job is about... | Lead with this project | Why it fits |
|---|---|---|
| TikTok/Reels-style feed, recommendations, video ranking | **Yum AI / Bless feed engine** | Real multi-vector recommender in production (Twelve Labs + OpenAI embeddings, pgvector) |
| AI meal planning, recipe import, food apps | **Yum AI** | Built the scraping + AI normalization pipeline from scratch |
| Travel apps, itinerary builders, Expedia/Skyscanner | **Travy** | Live Expedia integration, AI tour guide, HLS video |
| Relationship / habit / streak tracking, custom iOS features | **Unfold Us** | Custom Swift modules, home-screen widgets, custom push sounds |
| Two-sided marketplace, Stripe Connect, host/provider + customer | **Explore Bless** | Dual-user architecture, Stripe Connect split payments, scheduling |
| AI voice agents, outbound calling, Twilio + ElevenLabs | **Novara AI** | Production AI outbound sales agent |
| Field ops, inspections, barcode/QR scanning, offline-first | **Clearwell** | Water tank inspections, QR scan, AI health analysis |
| Multi-location ops, geolocation activity logging, admin dashboards | **Baketracker** | Multi-tenant ops platform with geo-gated logging |
| Healthcare / practice management / legacy modernization | **Amromed therapy platform** | Laravel+jQuery → MERN migration, HIPAA-sensitive |
| Telephony, OTP voice, regional phone number provisioning | **Novara AI / Twilio work** | Twilio Available Numbers + Outgoing Caller ID APIs in prod |
| Subscriptions, IAP, credits, server-side receipt validation | **Multiple (Yum AI, Travy, Unfold Us)** | RevenueCat + Apple IAP with idempotent server validation |

---

## 3. Portfolio Projects (detailed)

Each entry is formatted so the agent can lift a single-sentence reference directly into a proposal.

### Yum AI — AI meal planning
- **One-liner:** AI meal planner with large-scale recipe scraping and an AI Recipe Import feature that normalizes messy web data into structured recipes.
- **Stack:** React Native, Node.js/Fastify, PostgreSQL, OpenAI, scraping pipeline.
- **Hard parts solved:** Data normalization from thousands of inconsistent recipe sources; personalization feed.
- **Name-drop line:** *"Built something similar for Yum AI — the tricky part was normalizing scraped recipes into a clean schema the AI could reason over."*

### Travy — AI travel planner
- **One-liner:** Instant personalized itinerary builder with Expedia API integration for flight and hotel matching, plus HLS video tour guides.
- **Stack:** React Native, Node.js, Expedia API, HLS streaming, OpenAI.
- **Hard parts solved:** Turning vague travel preferences into bookable itineraries; live third-party inventory.
- **Name-drop line:** *"Did the same shape of integration on Travy — Expedia's API has some quirks around availability caching that'll bite you if you don't handle it upfront."*

### Unfold Us — relationship tracker
- **One-liner:** Long-term relationship tracking with streaks, custom Swift modules, custom push notification sounds, and home-screen widgets.
- **Stack:** React Native + native Swift modules, Node.js backend, APNs with custom sound assets.
- **Hard parts solved:** Native iOS features React Native doesn't expose out of the box (widgets, custom push sounds).
- **Name-drop line:** *"Unfold Us needed custom Swift modules for home-screen widgets and custom notification sounds — the RN bridge for that is underdocumented; happy to share what I learned."*

### Explore Bless — two-sided marketplace
- **One-liner:** Explorer/Host marketplace with Stripe Connect for split payments and a scheduling system.
- **Stack:** React Native, Node.js, Stripe Connect, PostgreSQL.
- **Hard parts solved:** Multi-party payments with holds/refunds, role-based flows without leaking data across tenants.
- **Name-drop line:** *"Built a similar dual-role marketplace on Explore Bless — the Stripe Connect piece (destination vs. separate charges) is where most devs get it wrong the first time."*

### Novara AI — AI outbound calling agent
- **One-liner:** Web platform that makes outbound AI sales calls using ElevenLabs voices and Twilio telephony.
- **Stack:** React.js, Node.js, Twilio, ElevenLabs, realtime audio streaming.
- **Hard parts solved:** Low-latency voice pipeline, Twilio number provisioning per region, call state management.
- **Name-drop line:** *"Shipped Novara AI on the same pattern — Twilio + ElevenLabs works, but the latency budget is tighter than it looks, especially on the first audio chunk."*

### Clearwell — field inspection platform
- **One-liner:** Water tank inspection app with barcode/QR scanning and AI-driven health analysis for field techs.
- **Stack:** React Native, camera + QR libs, Node.js, AI image analysis.
- **Hard parts solved:** Offline-first scanning, image capture reliability, running inference on field-quality photos.
- **Live link:** clearwell.ai
- **Name-drop line:** *"Clearwell does almost exactly this — QR scan in the field, AI analysis on the captured image, sync when back online."*

### Baketracker — multi-location ops platform
- **One-liner:** Operational management platform with geolocation-gated activity logging across multiple sites.
- **Stack:** Next.js, Node.js, PostgreSQL, geolocation APIs.
- **Hard parts solved:** Multi-tenant data isolation, geo-fenced actions, ops admin tooling.
- **Live link:** baketracker-frontend.vercel.app
- **Name-drop line:** *"Baketracker has the same shape — multi-location, role-based, with geo-gated actions so staff can only log work from the actual site."*

### TBeauty — beauty/routine social app
- **One-liner:** Regional leaderboards and routine sharing with HLS video, OCR product scanning, and Base64 uploads.
- **Stack:** React Native, HLS video, OCR, Node.js.
- **Name-drop line:** *"TBeauty ran on a similar feed + leaderboard pattern — HLS for video, OCR for product tagging."*

### Bless AI Feed Engine (the recommender)
- **One-liner:** Production "TikTok-style" feed using multi-vector retrieval (Twelve Labs 512-dim video embeddings + OpenAI 1536-dim text embeddings) with weighted user taste vectors in pgvector.
- **Stack:** Node.js, PostgreSQL (Neon) + pgvector, Twelve Labs Marengo-3.0, OpenAI text-embedding-3-small, Prisma.
- **Perf hooks:** <5ms feed latency (IVFFlat), <2ms preference updates, <15ms topic-filtered queries.
- **Name-drop line:** *"Built this exact architecture in production — two separate vector spaces (visual and textual) blended at query time, weighted user taste vector updated on each signal, full recompute on a Sunday cron to prevent drift."*

---

## 4. Skill Map (for quick justification in proposals)

Use these as one-line technical justifications when the client asks *"why this stack?"*.

**Mobile**
- React Native, Flutter, native iOS/Android tooling, Swift modules, home-screen widgets.
- Hardware/device: camera, GPS, QR/barcode scanning, offline sync, push (APNs + FCM + OneSignal), custom notification sounds.

**Backend & Real-time**
- Node.js (Fastify, Express), Python (FastAPI), Laravel (legacy work).
- Realtime: Socket.IO, BullMQ, Redis — used under real load, not just tutorials.

**Data**
- PostgreSQL (including Neon), pgvector, Prisma, MongoDB, MySQL, Supabase, Firebase.

**AI / Automation**
- OpenAI SDK, text-embedding-3-small, Twelve Labs Marengo/Pegasus, ElevenLabs, Claude Code, n8n, CrewAI.
- Patterns: semantic search, multi-vector retrieval, agentic workflows, scraping + AI normalization pipelines.

**Infra / DevOps**
- AWS (EC2, S3, Lambda, EKS, Elastic Beanstalk), GCP (Vertex AI, VMs), DigitalOcean, Vercel, Railway, Render, Cloudflare R2, NGINX reverse proxies.
- Docker, Kubernetes, GitHub Actions CI/CD.

**Payments & Monetization**
- Stripe (Payments + Connect), RevenueCat, Apple IAP, Superwall.
- Idempotent server-side receipt validation, prepaid credit systems.

**Telephony**
- Twilio Available Phone Numbers API (regional provisioning), Outgoing Caller ID (OTP voice), programmable voice for AI agents.

**Monitoring**
- Posthog, Sentry.

---

## 5. Credibility Stats (drop into closing lines sparingly)

- Top Rated on Upwork, 100% JSS, 1000+ hours.
- 5+ years, apps shipped to millions of users.
- $100k+ client revenue driven from products I've built.
- Open source: Microsoft `autogen` (gallery component), Creative Commons (navigation bugs + "Other Opportunities" section).

Rule of thumb: use at most **one** stat per proposal, and only if it reinforces the specific technical point being made. Dropping all four reads as a resume, not a conversation.

---

## 6. Agent Usage Notes

When generating a proposal:
1. Match the job to row(s) in Section 2. If nothing matches, don't force a portfolio mention.
2. Lift the matching project's **name-drop line** as a starting point — then rewrite it in the voice of the specific hook you chose, don't paste verbatim.
3. Use Section 4 only when the client explicitly asks about stack, or when you need to justify a non-obvious tech choice.
4. Section 5 stats are decoration, not substance. Skip them if the hook and technical content are already doing the work.
