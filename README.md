# emotion-analysis 🎭 — Hume AI on call transcripts — 48 emotions, sentiment scoring, emotional journeys.

<p align="center">
  <img src="assets/hero.png" alt="Emotion Analysis hero" width="1100">
</p>

<p align="center">
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript">
  <img src="https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white" alt="Node.js">
  <img src="https://img.shields.io/badge/Hume_AI-FF6B6B?style=for-the-badge" alt="Hume AI">
  <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white" alt="PostgreSQL">
</p>

Processes call transcripts through Hume AI's emotion detection API to extract 48 discrete emotions per utterance. Maps emotional arcs across conversations, identifies sentiment shifts, and generates emotional journey visualizations for interview prep and relationship intelligence.

> **This is a closed-source project. The README documents the architecture and learnings.**

## What it does

- Processes call transcripts through Hume AI (48 emotion dimensions)
- Maps emotional arcs across entire conversations
- Identifies sentiment shifts and turning points
- Scores overall call quality and emotional resonance
- Generates per-speaker emotion profiles
- Feeds emotional context back into CRM for relationship intelligence

## How it works

```
Transcript ingested (Fireflies or manual upload)
  → Split into utterances
  → Each utterance sent to Hume AI API
  → 48-dimension emotion vector returned
  → Aggregate into speaker profiles
  → Plot emotional journey over time
  → Store scores in PostgreSQL
  → Surface insights in CRM contact view
```

## Tech stack

- **Runtime:** Node.js
- **AI:** Hume AI (Expression Measurement API), 48 emotion dimensions
- **Database:** PostgreSQL (RDS)
- **Processing:** Batch pipeline with rate limiting
- **Visualization:** Emotion arc charts (time-series)

## What I learned

- 48 emotions is far more nuanced than positive/negative sentiment — "interest" vs "excitement" vs "admiration" tells you different things about a conversation
- Emotional journeys across a 30-minute call reveal patterns invisible in transcripts — a dip in "confidence" at minute 12 correlates with tough questions
- The most valuable insight wasn't individual emotions but emotion *transitions* — "confusion -> understanding -> excitement" signals a great explanation
