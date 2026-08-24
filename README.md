<div align="center">

# Md. Emamul Mursalin

**I design and ship AI products — web, mobile, and the systems behind them.**

Software Engineer at [Ayana Dev Studio](https://mursalinsdesk.com) · Rajshahi, Bangladesh
TypeScript · Next.js · NestJS · Postgres · AI integration

[![Portfolio](https://img.shields.io/badge/Portfolio-mursalinsdesk.com-2F5AA8?style=flat-square)](https://mursalinsdesk.com)
[![Email](https://img.shields.io/badge/Email-emamulmursalin47%40gmail.com-5A6673?style=flat-square)](mailto:emamulmursalin47@gmail.com)
[![Fiverr](https://img.shields.io/badge/Fiverr-Hire-16704F?style=flat-square)](https://www.fiverr.com/emamulmursalin_)

</div>

---

## What I do

I build production systems end to end: the interface, the API, the data model, and increasingly the AI layer that makes the product worth using. Most of my recent work is full-stack TypeScript — Next.js App Router on the front, NestJS and Postgres behind it — with LLM pipelines (Groq, OpenAI, LangGraph) wired in where they earn their place rather than as decoration.

What I care about is the part users never see: session handling that survives a refresh race across browser tabs, caches that invalidate on the right mutation, errors that say what actually went wrong. Shipping is the easy half; keeping a system honest as it grows is the work.

---

## Selected work

| Project | What it is | Stack |
|---|---|---|
| **[Founders](https://founders.mursalinsdesk.com)** | A reputation economy for founders — credit-metered peer feedback, AI-scored reviews, launch pledges with public show-up rates. Monorepo, 600+ tests, merge-blocking CI. | Next.js 16 · NestJS · Neon Postgres · Prisma · Groq · Vercel |
| **[BookWriter](https://bookwriter-dun.vercel.app)** | AI book writer and editor — drafts new books or brings existing ones current, researched and cited, cover to back cover. | Next.js · TypeScript · LLM pipeline |
| **[MedScribe](https://medscribe-saas-nine.vercel.app)** | A prescription pad built for doctors in Bangladesh — 25,000+ searchable local medicines, Bangla or English entry, printed on the practice's own letterhead. | Next.js · TypeScript · Postgres |
| **[CoatingPro](https://coatingpro.vercel.app)** | Industrial coating services platform — service catalogue, quote flow, lead capture. | Next.js · TypeScript · Tailwind |
| **CakeOrFake** | Chrome extension that AI-screens Upwork applicants — hours of review compressed into minutes. | Chrome Extensions API · LLM scoring |
| **Sunnah Companion** | Cross-platform mobile app for daily practice tracking. | Flutter · Dart |

More case studies, including in-progress work: **[mursalinsdesk.com](https://mursalinsdesk.com)**

---

## How I engineer

Specifics from systems currently in production, not a philosophy list:

- **Auth that survives real browsers.** First-party BFF cookie layer over a token API; a single-flight refresh promise serialized across tabs with the Web Locks API, so N concurrent 401s trigger exactly one rotation instead of tripping refresh-reuse detection and logging the user out.
- **Caches that tell the truth.** Tag-scoped invalidation in the Next.js App Router — mutations expire the tags their writes actually touch, so "changes go live immediately" is a guarantee rather than a hope, and read-your-own-writes lands in the same round trip.
- **Failure that stays honest.** Paired Suspense and error boundaries per route segment; a 404 is reserved for genuinely missing resources, never used to paper over an API outage. Failed reads never render as empty states.
- **Types as design.** Strict TypeScript with `noUncheckedIndexedAccess`, literal unions over stringly-typed fields, discriminated unions so invalid states cannot compile.
- **Tests that gate merges.** 600+ specs weighted toward integration, asserting what users observe; CI runs them merge-blocking, and the hard cases — concurrent-refresh races, cache invalidation, optimistic rollback — are covered on purpose.
- **Audits before rewrites.** I review my own systems against structured checklists (rendering, state, types, data, resilience, tests, performance, CSS, architecture) and fix by severity instead of by instinct.

---

## Open source

Agent tooling I've built and published for [Claude Code](https://claude.com/claude-code):

- **[design-craft](https://github.com/emamulmursalin47/design-craft)** — UI audit, design rationale, and stakeholder-response skill distilled from two UX books, with contrast and palette scripts.
- **[competitor-teardown](https://github.com/emamulmursalin47/competitor-teardown)** — crawls any product site and produces a full teardown: screenshots, auto-generated wireframes, UX critique, business-model and funnel analysis, packaged as a standalone HTML report.

---

## Stack

| Layer | Tools |
|---|---|
| **Languages** | TypeScript, JavaScript, Python, Dart, SQL |
| **Frontend** | Next.js (App Router, RSC), React, Tailwind CSS, shadcn/ui, Framer Motion |
| **Backend** | NestJS, Node.js, Express, REST, GraphQL, Socket.IO |
| **Data** | PostgreSQL, Neon, Prisma, MongoDB, Redis |
| **AI** | Groq, OpenAI, LangGraph, Vercel AI SDK, RAG pipelines, prompt/eval design |
| **Mobile** | Flutter, React Native |
| **Platform** | Vercel, Docker, GitHub Actions, Turborepo, pnpm workspaces |
| **Testing** | Vitest, Jest, Playwright, React Testing Library, Supertest |

---

## Currently

Building an AI-driven feedback and launch platform for founders, and writing agent tooling that makes engineering review reproducible instead of vibes-based. Open to work on AI products, platform architecture, and systems that need to stay correct under growth.

<div align="center">

<a href="https://github.com/emamulmursalin47">
<img height="150" src="https://github-readme-stats.vercel.app/api?username=emamulmursalin47&show_icons=true&hide_border=true&bg_color=00000000&title_color=2F5AA8&icon_color=2F5AA8&text_color=808891&hide=issues" alt="GitHub stats" />
</a>
<a href="https://github.com/emamulmursalin47">
<img height="150" src="https://github-readme-stats.vercel.app/api/top-langs/?username=emamulmursalin47&layout=compact&hide_border=true&bg_color=00000000&title_color=2F5AA8&text_color=808891&langs_count=8" alt="Top languages" />
</a>

</div>
