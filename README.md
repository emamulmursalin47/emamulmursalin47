<div align="center">

# Md. Emamul Mursalin

**Full-stack engineer — I design and ship AI products: web, mobile, and the systems behind them.**

Full Stack Engineer at Ayana Dev Studio · Rajshahi, Bangladesh · Open to remote
TypeScript · Next.js · NestJS · PostgreSQL · AI agents & LLM integration

[![Portfolio](https://img.shields.io/badge/Portfolio-mursalinsdesk.com-2F5AA8?style=flat-square)](https://mursalinsdesk.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-mdemamulmursalin-2F5AA8?style=flat-square)](https://linkedin.com/in/mdemamulmursalin)
[![Email](https://img.shields.io/badge/Email-emamulmursalin47%40gmail.com-5A6673?style=flat-square)](mailto:emamulmursalin47@gmail.com)
[![Fiverr](https://img.shields.io/badge/Fiverr-Hire-16704F?style=flat-square)](https://www.fiverr.com/emamulmursalin_)

</div>

---

## What I do

I build production systems end to end — interface, API, data model, and the AI layer that makes the product worth using. Recent work is full-stack TypeScript: Next.js App Router on the front, NestJS and PostgreSQL behind it, with LLM pipelines wired in where they earn their place rather than as decoration.

That AI layer is most of what I do now: agent orchestration and tool-calling, MCP servers connecting models to real systems, real-time voice pipelines (Gemini Live), rubric-scored evaluation with OpenAI and Anthropic, and Telegram-native agents that turn conversation into tracked work. I've shipped an Amazon advertising platform that automates PPC campaign management and bid optimization through a dashboard rather than a specialist, a multi-tenant voice-coaching SaaS running in multi-org production, and an AI hiring assistant on the Chrome Web Store.

What I care about is the part users never see: session handling that survives a refresh race across tabs, caches that invalidate on the right mutation, tenant isolation proven by tests rather than assumed. Shipping is the easy half — keeping a system honest as it grows is the work.

---

## Selected work

| Project | What it is | Stack |
|---|---|---|
| **[Virtual Client](https://www.virtualclient.app/)** | Multi-tenant B2B voice-AI coaching platform — teams rehearse live conversations against AI personas and get rubric-scored feedback. **~2,500 practice sessions** across orgs in production. Hardened tenancy across 8 critical collections via a two-step Firestore security-rule migration with **90+ rules-unit tests** and an emulator harness that catches misconfigurations pre-deploy. | React · Vite · TypeScript · Express · Firebase · Gemini Live · OpenAI/Anthropic SDKs · Vitest |
| **[Telova](https://telova.tech)** | AI standups for Telegram — agents run daily check-ins, parse what the team says into tracked tasks, detect blockers, log hours, and rank engagement on live leaderboards. Role-based dashboards give managers a real picture of who needs a hand. | Next.js · NestJS · PostgreSQL · Prisma · OpenClaw · OpenRouter · Telegram Bot API |
| **[CakeOrFake](https://www.cakeorfake.com/)** · [Chrome Web Store](https://chromewebstore.google.com/detail/cakeorfake/hgbmgaejaencbbhgpmomabnfnlpgmbhi) | AI hiring assistant for Upwork — analyses proposals, surfaces best-fit candidates, and runs AI deep research by aggregating public data on applicants. Hours of screening compressed into minutes. | Chrome Extension · JavaScript · Express · Firebase · Stripe · RevenueCat · LLM APIs |
| **[Iqtidah](https://www.iqtidah.com/)** | Islamic habit tracker that unlocks 50 daily sunnahs against your prayer times — Quran, hadith and dua in Bengali and English. Offline-first, ad-free. | Flutter · Dart |
| **[Founders](https://founders.mursalinsdesk.com)** | A reputation economy for founders — credit-metered peer feedback, AI-scored reviews, launch pledges with public show-up rates. Turborepo monorepo, 600+ specs, merge-blocking CI. | Next.js 16 · NestJS · Neon Postgres · Prisma · Groq · Vercel |
| **[MedScribe](https://medscribe-saas-nine.vercel.app)** | A prescription pad built for doctors in Bangladesh — 25,000+ searchable local medicines, Bangla or English entry, printed on the practice's own letterhead. | Next.js · TypeScript · PostgreSQL |
| **[BookWriter](https://bookwriter-dun.vercel.app)** | AI book writer and editor — drafts new books or brings existing ones current, researched and cited, cover to back cover. | Next.js · TypeScript · LLM pipeline |
| **Contently AI** | AI social-content SaaS with switchable multi-model generation and agent tooling for scalable output. | Next.js · TypeScript · Groq · MongoDB · Firebase · JWT |

Case studies and work in progress: **[mursalinsdesk.com](https://mursalinsdesk.com)**

---

## How I engineer

Specifics from systems currently in production, not a philosophy list:

- **Multi-tenancy proven, not assumed.** Tenant isolation across 8 Firestore collections migrated in two safe steps, backed by 90+ security-rules unit tests and an emulator-driven harness — misconfigurations fail in CI instead of leaking across orgs.
- **Auth that survives real browsers.** First-party BFF cookie layer over a token API; a single-flight refresh promise serialized across tabs with the Web Locks API, so N concurrent 401s trigger exactly one rotation instead of tripping refresh-reuse detection and signing the user out.
- **Caches that tell the truth.** Tag-scoped invalidation in the Next.js App Router — mutations expire the tags their writes actually touch, so "changes go live immediately" is a guarantee, and read-your-own-writes lands in the same round trip.
- **Failure that stays honest.** Paired Suspense and error boundaries per route segment; 404 reserved for genuinely missing resources, never used to paper over an API outage. Failed reads never render as empty states.
- **Types as design.** Strict TypeScript with `noUncheckedIndexedAccess`, literal unions over stringly-typed fields, discriminated unions so invalid states cannot compile.
- **Tests that gate merges.** Suites weighted toward integration, asserting what users observe; CI runs them merge-blocking, and the hard cases — concurrent-refresh races, cache invalidation, optimistic rollback — are covered on purpose.
- **Audits before rewrites.** I review my own systems against structured checklists (rendering, state, types, data, resilience, tests, performance, CSS, architecture) and fix by severity rather than by instinct.

---

## Open source

Agent tooling I've built and published for [Claude Code](https://claude.com/claude-code):

- **[design-craft](https://github.com/emamulmursalin47/design-craft)** — UI audit, design rationale, and stakeholder-response skill distilled from two UX books, with contrast and palette scripts.
- **[competitor-teardown](https://github.com/emamulmursalin47/competitor-teardown)** — crawls any product site and produces a full teardown: screenshots, auto-generated wireframes, UX critique, business-model and funnel analysis, packaged as a standalone HTML report.

---

## Stack

| Layer | Tools |
|---|---|
| **Languages** | TypeScript, JavaScript (ES6+), Python, Dart, SQL |
| **Frontend** | Next.js (App Router, RSC), React, React Native, Tailwind CSS, shadcn/ui, MUI, Framer Motion |
| **Backend** | NestJS, Node.js, Express, REST, GraphQL, WebSockets (Socket.IO) |
| **AI & agents** | OpenAI, Anthropic, Groq, Gemini Live, OpenRouter, OpenClaw, Hermes AI, MCP servers, agent orchestration & tool-calling, RAG, prompt & eval design |
| **Data** | PostgreSQL, Neon, Prisma, MongoDB, Firebase/Firestore, Redis |
| **State** | Redux, RTK Query, Context API, Zustand |
| **Mobile** | Flutter, React Native |
| **Platform** | Vercel, Docker, GitHub Actions, Turborepo, pnpm workspaces, Netlify, Firebase |
| **Testing** | Vitest, Jest, Playwright, React Testing Library, Supertest, Firebase emulator suite |

---

## Experience

**Ayana Dev Studio** — Full Stack Engineer · Sep 2025 – Present
Built an AI-powered Amazon advertising platform automating PPC campaign management, bid optimization and listings through a single dashboard. Shipped CakeOrFake and Telova. Architected NestJS/Prisma/PostgreSQL backends and engineered agentic features with OpenClaw, OpenRouter, MCP servers and Telegram bot integrations.

**ATCTECH Limited** — Jr. Software Engineer · Jan 2024 – Aug 2025
Cut page load times by 30% and improved SEO through Next.js SSR/SSG, code-splitting, lazy loading and image optimization. Built a reusable Tailwind UI library and shipped responsive, accessible interfaces from Figma against REST APIs.

B.Sc. in Information & Communication Engineering, Bangladesh Army University of Engineering & Technology (BAUET) · Scrum Fundamentals Certified

---

## Currently

Building an AI-driven feedback and launch platform for founders, and writing agent tooling that makes engineering review reproducible instead of vibes-based. Open to work on AI products, platform architecture, and systems that need to stay correct under growth.

<div align="center">

**[mursalinsdesk.com](https://mursalinsdesk.com)** · [emamulmursalin47@gmail.com](mailto:emamulmursalin47@gmail.com) · [LinkedIn](https://linkedin.com/in/mdemamulmursalin)

</div>
