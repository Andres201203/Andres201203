# Andres Escobedo Lara

Software engineer working on production AI systems — conversational agents,
data pipelines and the infrastructure that keeps them running.

I build and operate a multi-agent WhatsApp sales assistant that handles real
customer conversations end to end: qualifying leads, scoring them, syncing to a
CRM, and surfacing the results in an analytics dashboard. It runs in production
and I own it from schema to deploy.

> **Note on my activity graph:** most of my commits live in private client
> repositories, so the public repos below are only a slice of my work. Happy to
> walk through the architecture of the private systems in detail.

---

## What I'm building

### Sofia — AI sales agent for WhatsApp *(private, in production)*

A conversational sales agent that qualifies inbound leads over WhatsApp and
hands off to human sellers once a lead is genuinely ready.

- **Multi-agent architecture** with a runtime skill system, so agent behavior
  can be modified without redeploying.
- **Finite state machine** driving conversation state, with invariants
  enforcing that unqualified leads can never reach a seller.
- **Lead qualification and scoring**, plus routing and assignment across a
  sales team.
- **CRM integration** (HubSpot) and a financial sync layer, keeping an external
  source of truth in step with the application database.
- **Analytics dashboard** (Next.js) with funnel breakdowns by acquisition
  channel, pipeline value and conversion metrics.
- **Operational discipline:** feature-flagged rollouts, migration workflows
  against a live database, and post-deploy verification.

*Stack:* TypeScript · Node.js · Prisma · PostgreSQL/Supabase · Next.js ·
Railway · Vitest · Anthropic Claude

---

## Public repositories

| Project | What it is |
|---|---|
| [nba-predictions](https://github.com/Andres201203/nba-predictions) | Calibrated XGBoost + logistic-regression ensemble blended with a Monte Carlo 7-game series simulator to predict NBA Finals outcomes. Isotonic calibration, ~20 seasons of playoff data. |
| [formula-1-prediction](https://github.com/Andres201203/formula-1-prediction) | Predicts Grand Prix winners by regressing race pace on qualifying pace using FastF1 timing data and scikit-learn ensembles. Includes an explicit write-up of the model's limitations. |
| [andresbuilds-legal](https://github.com/Andres201203/andresbuilds-legal) | Static legal pages backing OAuth app integrations. |

---

## Stack

**Languages** TypeScript · JavaScript · Python · SQL

**Backend** Node.js · Prisma · PostgreSQL · Supabase · REST APIs

**Frontend** Next.js · React

**AI/ML** Anthropic Claude · OpenAI · multi-agent orchestration · prompt
engineering · scikit-learn · XGBoost

**Infra & tooling** Railway · Git · GitHub Actions · Vitest · feature flags

---

## How I work

- Root-cause fixes over workarounds — if a fix feels hacky, it is.
- Nothing ships unverified: tests run, behavior demonstrated, changes diffed
  against main.
- Risky changes go out behind feature flags so they can be turned off without a
  deploy.
- Small, reviewable changes with conventional commits.

---

## Contact

- **Email:** andresescobedolara@gmail.com
