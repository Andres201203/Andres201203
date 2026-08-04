# Andrés Escobedo Lara

**AI and data analyst who builds production LLM systems** and turns messy,
multilingual data into decisions.

I built an LLM document-extraction pipeline for LATAM insurance at Lockton, and
I ship **SofIA**, a multi-agent sales assistant running in production on
WhatsApp, Instagram and web.

B.S. Business Administration, Marketing Analytics — Rockhurst University,
Kansas City · Minor in Data Analytics & Technology · Expected Dec 2026

> Most of my commits live in private client repositories, so the public repos
> here are a slice of my work. Happy to walk through the architecture of the
> private systems in detail.

---

## Selected work

### SofIA — Multi-agent LLM sales assistant *(private, in production)*

A production GenAI platform handling **~350 leads/month** across WhatsApp,
Instagram and web for Fortune 500 clients in food, banking and CPG.

- **Multi-agent orchestration** on Claude (Opus/Sonnet) and GPT-4o, so the
  assistant quotes, looks up and books autonomously instead of routing every
  conversation to a human.
- **RAG plus tool/function calling** into pricing, CRM and calendar services,
  with evaluation gates and retrieval telemetry.
- **Real-time inference services** (REST + webhooks) with idempotent queues,
  retry/backoff and dedup middleware — deployed on Railway with CI/CD and
  Vitest coverage, keeping message handling reliable under production load.
- **Raised lead capture from 60% to 95%**, and added the trust-and-safety
  controls that serving enterprise clients requires: PII handling,
  prompt-injection defenses, audit logging and cost telemetry.

*Stack:* TypeScript · Node.js · Prisma · PostgreSQL/Supabase · Railway ·
Vitest · Claude · GPT-4o

### LLM document extraction for LATAM insurance — Lockton

- Scaled a Brazil-only extraction pipeline across LATAM by enriching a
  **Pydantic** schema with multilingual few-shot examples, so one system
  extracts premiums, deductibles, commissions and clauses across Spanish,
  Portuguese and French.
- Benchmarked native-language prompting against English and found English held
  up for high-resource languages — **redirecting the team from prompt wording
  to schema and context design.**
- Ran nine iterative prompt versions, one hypothesis each, to isolate the real
  levers: explicit extraction rules, exact schema field names, commission/null
  handling, and dropping a lossy pre-translation step.

---

## Public repositories

| Project | What it is |
|---|---|
| [formula-1-prediction](https://github.com/Andres201203/formula-1-prediction) | Gradient-boosted race-winner classifier over 6,911 driver-race records (2010–2025). Walk-forward backtest retraining before every race: **59.8% top-1 accuracy vs a 55.4% pole-sitter baseline**, with drift tracking and a test that asserts no temporal leakage. |
| [nba-predictions](https://github.com/Andres201203/nba-predictions) | Calibrated XGBoost + logistic-regression ensemble blended with a Monte Carlo 7-game series simulator for NBA Finals outcomes. |
| [andresbuilds-legal](https://github.com/Andres201203/andresbuilds-legal) | Static legal pages backing OAuth app integrations. |

---

## Skills

**Languages & Data** Python (Pandas, NumPy, scikit-learn) · TypeScript/Node.js ·
SQL · Pydantic

**AI / LLM** Claude · GPT-4o · prompt & context engineering · few-shot / RAG ·
tool & function calling · evaluation

**Data & BI** Tableau · Excel (MOS Expert certified) · Google Sheets / Apps Script

**Platforms & Tools** PostgreSQL/Supabase · Prisma · Railway · HubSpot ·
Salesforce · Meta APIs · Git/CI-CD

**Languages** Spanish (native) · English (fluent) · French (conversational)

---

## How I work

- Validate before claiming. In the F1 project the first model scored *below* a
  trivial baseline — that result is in the README, along with what fixed it.
- Root-cause fixes over workarounds.
- Risky changes ship behind feature flags so they can be turned off without a
  deploy.

---

## Contact

- **Email:** andresescobedolara@gmail.com
- **LinkedIn:** [andres-escobedo-lara](https://linkedin.com/in/andres-escobedo-lara)
