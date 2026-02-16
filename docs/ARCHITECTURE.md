# Think Tank Architecture

## Overview

The Think Tank is a **multi-agent orchestration system** designed to solve a common problem: planning without execution. It uses specialized AI agents that each focus on a specific domain, then synthesizes their insights into actionable intelligence.

## The Core Pattern

```
┌─────────────────┐
│   INPUT LAYER   │  ← User queries, scheduled runs, triggers
└────────┬────────┘
         │
    ┌────┴────┬────────┬────────┐
    │         │        │        │
┌───▼───┐ ┌───▼───┐ ┌──▼───┐ ┌──▼────┐
│ Saul  │ │ Mike  │ │ Gus  │ │ Scout │  ← Domain Agents (parallel)
│(Vault)│ │(Habits│ │(Intel)│ │(Expl.)│
└───┬───┘ └───┬───┘ └──┬───┘ └──┬────┘
    │         │        │        │
    └────┬────┴────────┴────────┘
         │
    ┌────▼────┐
    │  Cook   │  ← Synthesis Layer
    │(Merge)  │
    └────┬────┘
         │
    ┌────▼────┐
    │ OUTPUT  │  ← Actionable brief
    └─────────┘
```

## The Four Agents

### 1. Saul Goodman — The Vault Fixer
**Domain:** Knowledge management, notes, project history

Saul digs through your knowledge vault (Obsidian, Notion, etc.) to find:
- Active projects and forgotten ideas
- Patterns across your notes
- Contradictions between what you say and what you do

**Key insight:** Your past notes contain gold you're forgetting.

### 2. Mike Ehrmantraut — The Cleaner
**Domain:** Habits, health, discipline, daily execution

Mike inspects your tracking data to find:
- What's locked in vs. what's slipping
- Energy patterns and correlations
- Small problems before they become big ones

**Key insight:** Consistency compounds; inconsistency compounds too.

### 3. Gustavo Fring — The Strategist
**Domain:** Market intelligence, trends, external signals

Gus watches the external world for:
- Opportunities aligned with your goals
- Threats to your current path
- Learning signals worth following

**Key insight:** The best moves are often invisible until someone points them out.

### 4. The Cook — The Synthesis Layer
**Domain:** Cross-domain insight, tension detection

The Cook reads all three briefs and:
- Finds connections between domains
- Exposes tensions (where actions contradict goals)
- Delivers ONE specific, actionable move

**Key insight:** The magic happens in the gaps between reports.

## Why This Pattern Works

### 1. **Specialization > Generalization**
Each agent has a narrow focus and a distinct personality. This prevents the "generic advice" problem where AI gives balanced but useless guidance.

### 2. **Tensions Surface Truth**
The synthesis layer explicitly looks for contradictions. Where do your vault notes disagree with your habits? Where do your goals conflict with market reality?

### 3. **Parallel Processing**
Saul, Mike, and Gus can run independently (even simultaneously). The Cook only activates after all three reports exist.

### 4. **Output Constraints**
Each agent has a strict output format. This makes synthesis possible and prevents rambling.

## Implementation Options

### Option A: Pure LLM (Simplest)
Run each agent as a separate prompt to your preferred LLM. Store outputs as markdown files.

### Option B: Scheduled Orchestration
Use a cron job or scheduled task to:
1. Run Saul → save to `briefs/saul-YYYY-MM-DD.md`
2. Run Mike → save to `briefs/mike-YYYY-MM-DD.md`
3. Run Gus → save to `briefs/gus-YYYY-MM-DD.md`
4. Run Cook (reading all three) → save to `briefs/cook-YYYY-MM-DD.md`

### Option C: Event-Driven
Trigger specific agents based on events:
- New vault note → Run Saul
- Missed habit → Run Mike
- Morning news scan → Run Gus

## Data Sources

### Saul (Vault)
- Markdown notes (Obsidian, Logseq)
- Project management tools
- Knowledge bases

### Mike (Habits)
- JSON habit logs
- Fitness tracking APIs
- Calendar data
- Sleep trackers

### Gus (Intel)
- News APIs
- RSS feeds
- Market data
- Research papers

## Customization

### Changing Personalities
The character personas (Saul, Mike, Gus) are scaffolding. The pattern works with any distinct voices:
- **Optimist / Pessimist / Realist**
- **Past / Present / Future**
- **Analyst / Creative / Critic**

The key is that each perspective is **distinct and consistent**.

### Adding Domains
The pattern extends to N agents:
- **Social Agent:** Tracks relationships, follow-ups, network
- **Creative Agent:** Surfaces inspiration, creative blocks, artistic goals
- **Financial Agent:** Watches spending, investments, financial health

Just add another report to the Cook's input.

## The Scout Pattern (Bonus)

A fifth optional agent: **The Scout** explores new territories:
- Side income ideas
- Learning resources
- Networking opportunities

The Scout doesn't report regularly—only when something genuinely new appears.

## Anti-Patterns to Avoid

1. **Don't let agents talk to each other directly.** They report to the Cook only. Direct conversation creates circular dependencies.

2. **Don't skip the synthesis.** Reading three separate reports is useful; reading the Cook's brief is transformative.

3. **Don't automate blindly.** The Think Tank works best when there's a human in the loop to act on (or ignore) the recommendations.

4. **Don't make the Cook nice.** The Cook should be direct, even harsh. Tensions are the point.
