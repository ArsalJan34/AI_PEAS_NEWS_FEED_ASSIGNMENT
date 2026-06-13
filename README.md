# PEAS Framework & Task Environment Analysis
### System: Personalized News Feed Recommender (Twitter/X · TikTok Algorithm)
This project applies the **PEAS framework** and **Task Environment Analysis** to a real-world AI system — a personalized news feed recommender of the kind powering Twitter/X and TikTok. It was completed as part of an AI/Intelligent Systems course assignment.
---
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

### Task 4 — Structured Data Design (JSON Representation)
The full PEAS specification and environment classification encoded as a single valid JSON object:
```json
{
  "system_name": "Personalized News Feed Recommender",

  "peas": {
    "performance_measures": [
      "engagement_rate_meaningful_interactions_only",
      "session_satisfaction_feedback_and_return_frequency",
      "content_diversity_topic_source_perspective_spread",
      "misinformation_suppression_flagged_content_downranked"
    ],
    "environment": "Global digital ecosystem with device-level context (time, network, screen size, scrolling behaviour), multilingual content streams, dynamic social signals, breaking-news events, and platform advertising/moderation constraints",
    "actuators": [
      "ranked_content_feed_renderer",
      "push_notification_dispatcher",
      "ab_test_allocation_engine",
      "content_diversity_injector",
      "feedback_signal_collector"
    ],
    "sensors": [
      "interaction_telemetry_streams_millisecond_resolution",
      "nlp_embedding_encoder_high_dimensional_semantic_space",
      "real_time_trending_signal_detector",
      "social_graph_propagation_tracker",
      "user_context_sensors_device_geo_time_language",
      "source_credibility_scorer_factcheck_verdicts"
    ]
  },

  "environment_classification": {
    "observability": {
      "choice": "Partially Observable",
      "justification": "The agent cannot access a user's cognitive state or offline context; a scroll-past may signal disinterest or prior reading — indistinguishable from behavioural trace alone."
    },
    "agents": {
      "choice": "Multi-agent",
      "justification": "Millions of creators, advertisers, and bot networks act simultaneously; a coordinated campaign by one actor distorts the signal environment for every other agent."
    },
    "determinism": {
      "choice": "Stochastic",
      "justification": "Identical content shown at different times produces different outcomes; external events add uncontrollable variance to user response."
    },
    "episode_structure": {
      "choice": "Sequential",
      "justification": "Each recommendation conditions the next; surfacing a divisive article shifts emotional state and changes subsequent content appeal."
    },
    "temporal_stability": {
      "choice": "Dynamic",
      "justification": "The content pool refreshes continuously, trending topics peak and decay in hours, and user preferences drift over weeks."
    },
    "state_space": {
      "choice": "Continuous",
      "justification": "User preference is a dense embedding vector; article relevance and engagement probability are real-valued continuous outputs."
    }
  },

  "utility_function": "U = alpha*(Engagement_Rate) - beta*(Filter_Bubble_Index) - gamma*(Misinformation_Risk)"
}
```

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
## 👤 Student Info
| | |
|---|---|
| **Name** | Arsal Jan Chandio |
| **Roll No** | 2k23/CSE/34 |
---
## 🗂️ Course Info
> **Subject:** Artificial Intelligence / Intelligent Systems
> **Topic:** Agent Design & Task Environment Analysis
> **Framework:** PEAS (Russell & Norvig)
