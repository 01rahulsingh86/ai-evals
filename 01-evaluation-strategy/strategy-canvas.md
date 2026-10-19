# AI Evaluation Strategy Canvas

> Repo file `ai-evals/01-evaluation-strategy/strategy-canvas.md` (the repo is your submission).

## 1. Product Strategy, The Context

**Who it's for:** VP-level strategists and product leaders at Fortune 500 companies who pay upward of $50,000 a year for verified market intelligence.

**What they use it for:** Asking plain-language questions, like “Compare the pricing models of Stripe and Adyen,” and getting answers in seconds instead of digging through the platform.

**What's at stake:** Engagement is dropping, Q4 retention is at risk, and the CPO wants Ascend IQ live for the top 50 enterprise accounts next month. One poor answer to the wrong client can do lasting damage to the relationship.

## 2. Measurements, The Execution

**User promise.** For VP-level strategists and product leaders, Ascend IQ promises to deliver fast, accurate, and verifiable answers to market-intelligence questions in seconds, so that they can make high-stakes decisions with confidence without manually searching the platform.

**Top 3 trust metrics:**
- **Latency**, Response speed (P95 / P99). Slow kills engagement.
- **Fairness**, Quality consistency across user groups, geos, languages.
- **Robustness**, Coherence on messy, adversarial, out-of-scope inputs.

**Why these three:** Accuracy / Correctness: factual accuracy rate, comparison accuracy, numeric accuracy, contradiction rate, unsupported-claim rate.
Verifiability / Grounding: citation coverage, citation correctness, source-authority score, claim-to-source traceability, freshness of sources.
Latency: median response time, P95 latency, time-to-first-token, time-to-final-answer. A reasonable product target might be <3–5 sec median for common questions, while allowing slower responses for complex research.
Fairness / Neutrality: whether competitors are evaluated using equivalent criteria, sentiment/skew by company, asymmetric evidence standards, omission bias. For example, Stripe and Adyen should be compared on the same dimensions rather than selectively highlighting strengths for one.
Safety / Enterprise Trust: hallucination rate, confidential-data leakage, cross-account leakage, prompt-injection resistance, inappropriate source usage, and rate of answers that should have abstained but did not.
Completeness / Relevance: whether the response answers every part of the question, includes the decision-relevant dimensions, avoids unnecessary information, and correctly handles ambiguity.
Freshness: percentage of answers using information within the required freshness window, stale-fact rate, and detection of changed pricing/products.
User outcome metrics: answer acceptance rate, follow-up/rephrase rate, time saved versus traditional search, weekly active enterprise users, repeat usage, and retention among the top 50 accounts.

## 3. Strategic Trade-Offs, The Cost

### Trade-off 1 · Latency ↔ Robustness
We prioritize Robustness over Latency because Ascend IQ serves high-value enterprise clients, and a slower answer is preferable to an incorrect, unsafe, or misleading one that could damage trust.

### Trade-off 2 · Fairness ↔ Robustness
We prioritize Fairness over Latency because enterprise clients expect consistently reliable answers across markets, geographies, and user groups, even if additional checks add a small amount of response time.

---
_Generated from the AI Evaluation Strategy Canvas, M1 lab tool, AI Evals Certification._