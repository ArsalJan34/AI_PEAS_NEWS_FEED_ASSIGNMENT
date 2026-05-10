# PEAS Framework & Task Environment Analysis
### System: Personalized News Feed Recommender (Twitter/X · TikTok Algorithm)

This project applies the **PEAS framework** and **Task Environment Analysis** to a real-world AI system — a personalized news feed recommender of the kind powering Twitter/X and TikTok. It was completed as part of an AI/Intelligent Systems course assignment.

---

## 📋 Contents

| File | Description |
|------|-------------|
| `PEAS_News_Feed_Assignment_condensed.pdf` | Condensed 2-page report (PDF) |
| `PEAS_News_Feed_Assignment_condensed.docx` | Editable Word version |

---

## 🧠 What is the PEAS Framework?

PEAS stands for **Performance Measure, Environment, Actuators, and Sensors** — a structured method from Russell & Norvig's *Artificial Intelligence: A Modern Approach* for specifying the task environment of an intelligent agent.

---

## 📌 Assignment Overview

### Task 1 — PEAS Specification

Defines the four components of the recommender agent:

- **Performance Measure** — Engagement rate, session satisfaction score, content diversity index, and misinformation suppression rate.
- **Environment** — Global, heterogeneous digital ecosystem spanning user devices, content pools, social graphs, and platform constraints.
- **Actuators** — Ranked feed renderer, push notification dispatcher, A/B test engine, content diversity injectors, and feedback signal collector.
- **Sensors** — Interaction telemetry streams, NLP embeddings, trending signal detector, social graph trackers, user context sensors, and source credibility scorer.

### Task 2 — Environment Classification

The environment is classified across six dimensions:

| Dimension | Classification |
|-----------|---------------|
| Observability | Partially Observable |
| Agent Count | Multi-agent |
| Determinism | Stochastic |
| Episode Structure | Sequential |
| Temporal Stability | Dynamic |
| State Space | Continuous |

### Task 3 — Critical Analysis

- **Most Challenging Property:** Dynamism — the environment changes faster than any static model can track, forcing simultaneous optimization across conflicting time horizons (long-range preference learning vs. real-time trend adaptation).
- **Utility Function:**

```
U = α · (Engagement Rate) − β · (Filter Bubble Index) − γ · (Misinformation Risk)
```

Over-weighting any single term (e.g., maximizing α) leads to second-order harms such as filter bubble collapse and misinformation re-amplification — highlighting why all three terms must be balanced.

---

## 🔑 Key Takeaways

- Raw engagement metrics (click-through rate) are insufficient and can actively incentivize harmful content — a well-designed utility function must penalize filter bubbles and misinformation.
- The dynamic, stochastic, and multi-agent nature of the environment means no static model remains valid for long; continuous retraining and real-time adaptation are architectural requirements, not optimizations.
- PEAS analysis forces every design decision — from sensor architecture to ranking logic — to be evaluated against the full environment picture simultaneously.

---

## 📚 References

- Russell, S., & Norvig, P. (2020). *Artificial Intelligence: A Modern Approach* (4th ed.). Pearson.
- Twitter/X and TikTok recommendation system public documentation and research papers.

---

## 🗂️ Course Info

> **Subject:** Artificial Intelligence / Intelligent Systems
> **Topic:** Agent Design & Task Environment Analysis
> **Framework:** PEAS (Russell & Norvig)
