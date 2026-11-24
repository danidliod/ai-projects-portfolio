# AI-Built Projects Portfolio

Products I designed and shipped over the last year, from idea to production. AI plays two roles in them: **inside the product** (agents, classification, information extraction, content generation) and **as the engineering workflow** (Claude Code agents that build, test, deploy and fix incidents).

The source code stays in private repositories. Each page here explains the problem, how the product works, its architecture, stack, deployment and current status, with screenshots and video where available. **Code walkthroughs and live demos are available on request.**

![Tower of Mist](assets/migdal-haarafel/teaser.gif)

---

## By the numbers

| | |
|---|---|
| **Products** | 9 main + 3 smaller — most of them live or in daily use |
| **Commits** | ~3,600 |
| **Pull requests** | ~2,500 — every change on its own branch, with tests and a preview |
| **Test files** | ~1,300 (unit, component, end-to-end, evals, game-playing bots) |
| **Platforms** | Web/PWA, iOS (SwiftUI + Capacitor), Android, Apple Watch, WebXR, Telegram, WhatsApp |

---

## Main projects

| | Project | In one sentence | AI in the product | Status |
|---|---|---|---|---|
| 1 | [**Tower of Mist**](projects/01-tower-of-mist-game.md) | An adventure and learning game for kids in three languages — 2D, 3D and VR | Built with coding agents, including bots that play and test every level | 🟢 [Live on the web](https://migdal-haarafel.vercel.app) · 🟡 heading to the app stores |
| 2 | [**Chief-of-Staff AI**](projects/02-chief-of-staff-agent.md) | A personal business agent: meetings, email, calendar, CRM, receipts and tasks, via Telegram and a web console | Gemini (understanding, classification, vision, summaries) + automatic incident repair by Claude Code | 🟢 In production, used daily |
| 3 | [**Our Year (FamiSync)**](projects/03-family-year-planner.md) | The whole family year in advance, with automatic capture from WhatsApp groups | Claude extracts candidates; code decides what goes in | 🟢 Live for a first family |
| 4 | [**Growth Engine**](projects/04-growth-engine.md) | A marketing platform for organisations: campaigns, landing pages with A/B tests, social networks | An LLM writes variants, deterministic guardrails check them, Thompson sampling learns | 🟢 Live with a demo org · 🟡 before live providers |
| 5 | [**App Growth Kit**](projects/05-app-growth-kit.md) | An organic app-promotion kit run by Claude Code every hour | An agent driving a browser: reels, outreach, measurement, decision log | 🟢 [Open source](https://github.com/danidliod/app-growth-kit) |
| 6 | [**imhungry**](projects/06-imhungry.md) | "What can I eat right now?" — saves money by cutting food waste | Gemini: recipes from the pantry, receipt scanning, shelf life, shopping lists | 🟢 [Live](https://imhungry.appnest.fyi) · iOS, Android, Watch |
| 7 | [**Growing From Within**](projects/07-growing-from-within.md) | Career coaching at a professional crossroads: assessment, report, companion bot, CV, networking, interviews | A bot with 5 contexts, reports, CV tailoring, outreach drafts | 🟡 Advanced development |
| 8 | [**Mosquito Radar**](projects/08-mosquito-radar.md) | An honest iOS mosquito app: it hears the wingbeat at night and wakes you | On-device DSP only; built and calibrated with a coding agent | 🟡 TestFlight |
| 9 | [**HitDeck**](projects/09-hitdeck.md) | Scans music-game cards and plays the song on Apple Music | — (decoding a public data chain) | 🟢 [On the App Store](https://apps.apple.com/app/id6801653040) |

### Smaller projects

| Project | What it is | Technology | Status |
|---|---|---|---|
| **Shomer Sheket** ("Quiet Keeper") | Detects the dog's barking (a voice fingerprint in 24 frequency bands), plays an interrupt sound and rewards quiet, with a bark log. [Website](https://shomer-sheket.vercel.app) | PWA + a native Android background service (Java); the APK is built and signed in GitHub Actions | 🟢 Live |
| **chatdigest** | Daily summaries of WhatsApp groups, read straight from the local database on a Mac, including voice-note transcription, with phone access | Python, SQLite, whisper.cpp, Claude CLI, Tailscale, a Supabase Edge Function (encrypted text only) | 🟢 Personal use |
| **EV Electric Meter** | Managing charging meters for electric cars, plus a back office | Flutter, Firebase, Brevo | 🟡 |

---

## How I work with AI

| Stage | What AI does | What stays with me |
|---|---|---|
| Research & definition | Market and competitor scans, technical and regulatory feasibility (e.g. why "ultrasonic mosquito repellent" apps are documented fraud) | Choosing the problem, defining what success means |
| Planning | Decision records (ADRs), roadmaps, threat models, risk maps | Approving direction and priorities |
| Building | Claude Code writes code in small rounds on branches, each with a preview; dedicated agents for implementation, bug fixing, code review and releases | "Ship it" — nothing reaches production without approval |
| Testing | Unit tests, Playwright, extraction evals, bots that play the game, RLS tests on real Postgres | Deciding what to test and why |
| Operations | An incident is detected → an agent analyses, fixes, tests, deploys and reports on Telegram | Approving irreversible decisions |

**Principles that repeat across the projects**
- **Human in the loop:** AI proposes, a person approves — calendar events, marketing messages, CRM actions. Anything applied automatically is marked and can be undone in one tap.
- **The model doesn't decide:** it returns candidates, and deterministic code decides what passes.
- **Only true claims:** guardrails block any number, price or urgency that isn't in the facts.
- **Privacy by default:** on-device processing where possible, logs without content, secrets on the server only, extra protection for children's data.
- **Measure what matters:** paying users, not likes; a holdout group, not just conversions; evals, not gut feeling.
- **A bug that recurs three times gets an automated check**, not another paragraph in the docs.

## Technologies (across projects)

**AI:** Claude (Claude Code, Claude Code GitHub Action, Claude API), Google Gemini (incl. Vertex AI), Whisper · **Web:** Next.js, React 19, TypeScript, Tailwind, Vite · **Mobile:** SwiftUI, Capacitor (iOS/Android), Flutter, Java · **Games & graphics:** Phaser 4, Three.js, WebXR, Web Audio · **Data:** Supabase/Postgres + RLS, Cloudflare D1, Firebase · **Automation:** n8n · **Infrastructure:** Vercel, Cloudflare Workers, AWS EC2 + Docker Compose, GitHub Actions · **Integrations:** Telegram, WhatsApp (Meta Cloud API + linked device), Gmail/Calendar/Tasks/Drive, Resend, Twilio, StoreKit 2, MusicKit, RevenueCat · **Testing:** Vitest, Playwright, XCTest, evals

---

Contact me through my LinkedIn profile. Code access or a live demo on request.
