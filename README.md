# Music-Streaming-Dashboard
# Data Challenge

## 🎯 Your Role

Step into the role of a data analyst investigating a music streaming platform.
You've been provided with a dataset spanning multiple dimensions and time periods.
Your mission is to create an analytical report that uncovers patterns, drives insights,
and delivers actionable recommendations to stakeholders.

## 📊 The Scenario

You are the lead analyst at a mid-size music streaming service. The business has provided
four years of operational data covering listening behaviour, subscription lifecycle,
content catalogue, and user demographics across 10 markets. Leadership wants to know
what the data is telling them — where the opportunities are, where the risks are,
and what to do next.

### Dataset Overview

- **Dimensions**: 9 dimension tables tracking users, artists, tracks, genres, devices, playlists, subscription plans, countries, and a conformed date dimension
- **Bridge**: 1 bridge table linking playlists to tracks (many-to-many)
- **Facts**: 2 fact tables recording listening sessions and subscription events
- **Scope**: 2021-01-01 to 2024-12-31 (48 months)
- **Currency**: USD
- **Volume**: ~224,000 listening sessions, ~3,640 subscription events, ~961 users, ~774 tracks, ~448 artists

### Key Business Metrics Available

- Listening volume, duration, skip behaviour, new-artist discovery
- Subscription lifecycle events (signup, upgrade, downgrade, churn, retention)
- Monthly Recurring Revenue (MRR) decomposition (before / after / change per event)
- Estimated session-level revenue (ad revenue on Free tier; per-stream royalty on paid tiers)
- User segmentation (age, gender, country, subscription tier, fraud flag, family account)

## 🔍 Analysis Areas

Look for patterns and insights across these four core areas:

### Temporal Trends
- How do listening volume, revenue, and subscription events change over time?
- Are there seasonal, monthly, or weekly cycles?
- When do peaks and valleys occur, and why?
- What events or conditions trigger significant shifts?

### Entity Analysis
- Which entities (users, artists, tracks, playlists, devices, countries) drive the most activity?
- How do different segments (tier, age, country, device type) perform relative to each other?
- What characteristics distinguish high-performing entities from others?
- Are there geographic or demographic hotspots?

### Transaction Patterns
- What are the most common transaction/event types?
- How are they distributed across users, tiers, time, and geography?
- What correlations exist between listening behaviour and subscription outcomes?
- Are there anomalies or unexpected patterns (e.g. suspicious activity)?

### Cross-Dimensional Insights
- How do dimensions interact to affect outcomes? (e.g. tier × country × genre)
- Which attribute combinations over-index or under-index vs overall baselines?
- Do certain entity pairs (user–artist, device–genre, country–genre) show stronger affinity than others?
- What leading indicators predict future behaviour (upgrades, churn, lifetime value)?

## ❓ Guiding Questions

Use these to structure your analysis — they're starting points, not a checklist. Explore further where you find interesting signal.

### Revenue & Business Health
- What is total MRR, ARPU, and churn revenue over the period?
- Which tier, country, or cohort drives the most revenue? The most growth?
- How much revenue is at risk from the currently churning base?
- What's the net MRR expansion vs contraction each month?

### Customer Behaviour
- How does listening behaviour differ between tiers? Between age cohorts? Between countries?
- Do we see pre-churn warning signals in listening data? (i.e. is there a *leading indicator* for churn?)
- Do heavy free users convert to paid? What does "heavy" look like in practice?
- Which users are most and least engaged, and what do they look like?

### Content & Catalogue
- Which artists, tracks, and genres drive the most plays? The most revenue?
- How does content performance vary by country, age, or device?
- Are algorithmically recommended tracks performing differently from non-recommended tracks?
- How does playlist composition influence listening patterns?

### Fraud, Risk & Data Quality
- Are there suspicious listening patterns that suggest fraud or abuse?
- How does the `is_fraud_cluster` segment behave differently from regular users?
- What operational or quality issues surface from the data?

## 💡 Impact & Purpose

Your analysis should help stakeholders:

- Identify revenue growth and churn mitigation opportunities
- Prioritise market and segment investments
- Understand the drivers of engagement and retention
- Detect suspicious or anomalous activity
- Optimise content and marketing spend

## 📋 Deliverables

Create a professional analytical report that includes:

1. **Executive Summary**
   - 3–5 key findings with business impact stated clearly
   - Top 3 recommendations in plain language
   - Headline numbers that matter (MRR, churn rate, ARPU, engagement trends)

2. **Detailed Analysis**
   - Visualisations of key trends and patterns
   - Statistical summaries by segment
   - Answers to the guiding questions with supporting evidence

3. **Actionable Insights**
   - What you discovered and why it matters to the business
   - Recommended next steps with expected impact
   - Areas for deeper investigation or additional data

## 📁 Data Dictionary

See `DATA_DICTIONARY.md` for full table and column descriptions, including:
- Primary keys, foreign keys, and the star-schema diagram
- Revenue formulas (session-level ad/royalty revenue, MRR change logic)
- Subscription event semantics (signup, upgrade, downgrade, churn, retention)

## 🚀 Getting Started

1. **Explore the data**: Start with summary statistics, distributions, and simple aggregations
2. **Check data quality**: The data is generally clean, but keep an eye out for outliers or anomalies worth flagging
3. **Visualise relationships**: Use charts to probe temporal, geographic, and cross-dimensional patterns
4. **Test hypotheses**: Structure analysis around the guiding questions; look for both obvious patterns and subtle ones
5. **Go beyond top-N**: Raw rankings often hide the real story. Use over-indexing (share within segment ÷ share globally) and cohort comparisons to surface meaningful deviations.
6. **Synthesise insights**: Connect findings across dimensions into a coherent business story

## Scoring Hints (for your own benefit)

A strong submission will:
- Lead with business impact, not table dumps
- Quantify findings in dollars or percentage-of-base, not just row counts
- Use cohort and over-index analysis, not just top-N rankings
- Distinguish signal from noise — call out where findings are indicative vs conclusive
- Propose next actions that are specific and measurable
