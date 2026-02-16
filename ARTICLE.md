# I Built a Multi-Agent Think Tank for Personal Productivity — Here's the Architecture

*Three AI agents analyze my life. One synthesizes their insights into actionable moves. Here's how it works.*

---

## The Problem: Planning Without Execution

I had the perfect productivity stack:

- 📚 **Obsidian vault** with 500+ notes, project ideas, and research
- 📊 **Habit tracker** logging workouts, sleep, supplements, and diet
- 📰 **Curated news feeds** for tech, markets, and industry intelligence

And yet... I felt stuck. I'd spend hours *planning* my AI/ML career transition while *executing* on business development tasks that weren't moving the needle.

The data was there. The insights weren't.

**The gap:** I needed someone (or something) to look at ALL the data and tell me what I was missing. Not summarize—synthesize. Not encourage—expose the contradictions.

---

## The Solution: Specialized Agents + Ruthless Synthesis

I built a **multi-agent orchestration system** inspired by (okay, directly using) Breaking Bad characters. Each agent has a distinct personality, domain, and reporting format. They run independently. Then a synthesis layer called "The Cook" combines their insights and delivers ONE actionable move.

```
┌─────────┐ ┌─────────┐ ┌─────────┐
│  Saul   │ │  Mike   │ │   Gus   │
│ (Vault) │ │(Habits) │ │ (Intel) │
└────┬────┘ └────┬────┘ └────┬────┘
     │           │           │
     └───────────┼───────────┘
                 │
            ┌────▼────┐
            │  Cook   │ ← One insight, one action
            └─────────┘
```

---

## The Four Agents

### 1. Saul Goodman — The Vault Fixer

**"It's all good, man. I know a guy who knows a guy."**

Saul digs through my Obsidian vault like he's looking for dirt on a client. He finds:
- **Active schemes:** What I'm actually working on
- **Cold cases:** Forgotten ideas that still have value
- **Patterns:** Recurring themes across years of notes
- **Tensions:** Where my notes don't match my actions

Saul's job isn't to organize—it's to find the angles others miss.

### 2. Mike Ehrmantraut — The Cleaner

**"No half measures."**

Mike inspects my habit logs with the precision of a crime scene investigator:
- **Discipline report:** What's locked in vs. what's slipping
- **Energy patterns:** When I run hot vs. cold
- **Trends:** The actual numbers (weight, workouts, adherence)
- **Risks:** Problems before they become crises

Mike doesn't sugarcoat. He finds the gap, reports the gap, suggests the fix.

### 3. Gustavo Fring — The Strategist

**"I hide in plain sight. I always plan 10 moves ahead."**

Gus watches the external world—markets, tech trends, industry shifts:
- **Opportunities:** Actionable openings aligned with my goals
- **Threats:** Risks to current plans
- **Learning signals:** Resources worth studying
- **Market pulse:** Real estate, investments, macro trends

Gus never moves without calculation. Every piece of intel is a potential advantage.

### 4. The Cook — The Synthesis Layer

**"I am the one who knocks."**

The Cook reads all three reports and does what I can't: find the connections. His rules:
- **Don't summarize** — that's for amateurs
- **Look BETWEEN the reports** — the gaps hide the gold
- **Tensions > Confirmations** — contradictions are where growth lives
- **One real insight beats ten obvious ones**

The Cook delivers ONE specific, actionable move. Not a list. Not options. The move.

---

## A Real Example

Here's an actual (sanitized) output from my system:

```markdown
# 🧪 The Cook's Brief — 2026-02-16

## 💡 The Connection: "Agent Orchestration as the Asset"
Gus and Saul align on a major pivot: The Think Tank system I'm building 
is more valuable than the SaaS I'm trying to sell. Market intelligence 
shows "Agent Orchestration" is the defining skill of 2026, and my vault 
shows high density here.

## ⚡ The Tensions: "Playing Business vs. Cooking Code"
The most dangerous tension is between the AI/ML career goal and daily 
activity. 
- **The Lie:** "I'm transitioning to AI/ML Engineering." 
- **The Truth:** Vault and logs show 90% focus on business development, 
  10% on technical study.
- **The Result:** Building a "business" that might fail while stalling 
  on the "skill" that guarantees the career jump.

## 🎯 The Play: "The 18:00 Pivot"
Mike identifies 18:00 as the chaos point where sleep and spiritual goals 
die. Move my evening practice to 18:00 sharp (pre-gym). This breaks the 
energy loop and ensures the goal isn't "left for last."

## 🔮 The Wild Card: "The Open-Source Signal"
Stop hiding the orchestration work. Sanitize the Think Tank logic and 
put it on GitHub. One repo of high-level agentic orchestration is worth 
100 landing pages for a niche SaaS.
```

**This hit hard.** The Cook spotted a contradiction I'd been avoiding: I was "playing business" (building landing pages, planning marketing) instead of "cooking code" (building ML projects, learning orchestration frameworks).

---

## Why This Architecture Works

### 1. Specialization > Generalization
Each agent has a narrow focus and a strong personality. This prevents the "generic advice" problem where AI gives balanced but useless guidance.

### 2. Parallel Processing
Saul, Mike, and Gus run independently (simultaneously if using subagents). The Cook only activates after all three reports exist. No waiting.

### 3. Output Constraints
Each agent has a strict markdown format. This makes automated synthesis possible and prevents AI rambling.

### 4. Tensions Surface Truth
The Cook's explicit job is to find contradictions. Where do my vault notes disagree with my habits? Where do my goals conflict with market reality?

### 5. One Action, Not Ten
The Cook delivers ONE specific move. When everything is a priority, nothing is. The Cook picks.

---

## Technical Implementation

The simplest version uses pure LLM prompts:

1. **Copy the agent prompts** (in the repo) into Claude, GPT-4, or your local LLM
2. **Feed each agent their context** (vault export, habit JSON, news feed)
3. **Save their outputs** as markdown files
4. **Feed all three to the Cook**
5. **Read the brief and execute**

More advanced implementations can:
- Schedule agents with cron jobs
- Use subagents for true parallelism
- Trigger agents on events (new note → run Saul)
- Store briefs in a searchable history

The full prompts and architecture docs are in the [GitHub repo](https://github.com/USERNAME/agent-think-tank).

---

## The Scout Pattern (Bonus)

I added a fifth agent: **The Scout**. The Scout doesn't report on my life—it explores new territory:
- Side income ideas that fit my skills
- Learning resources worth bookmarking
- Networking opportunities I'd miss

The Scout runs on rotation, exploring one topic per day:
1. AI/ML learning resources
2. Side income opportunities
3. Real estate investment deals
4. Family activity ideas

The Scout prevents stagnation by continuously feeding new inputs into the system.

---

## Lessons Learned

### 1. Personalities Matter
The Breaking Bad personas aren't just fun—they're functional. Saul's shadiness makes him good at finding buried ideas. Mike's coldness makes him honest about my discipline gaps. Gus's calm calculation surfaces strategic threats I'd miss.

### 2. Synthesis Is the Product
Reading Saul's + Mike's + Gus's reports is useful. Reading the Cook's brief is transformative. The magic happens in the synthesis, not the analysis.

### 3. Tensions Are the Point
The most valuable output isn't "everything is going well." It's "you say you want X but you're doing Y." The Cook's job is to be uncomfortable.

### 4. One Move Beats Ten Plans
The system only works because the Cook delivers ONE action. If I got a list of ten suggestions, I'd optimize the list instead of executing item one.

---

## Who This Is For

The Think Tank works best if you:
- Track habits, notes, or life data
- Have goals that span multiple domains (career, health, finance)
- Tend to over-plan and under-execute
- Want AI to challenge you, not just assist you

It's overkill if you just need a todo list. It's essential if you're juggling complex life systems and need something to spot the patterns you're missing.

---

## The Code

The full system—agent prompts, architecture docs, and example outputs—is open source:

**[github.com/USERNAME/agent-think-tank](https://github.com/USERNAME/agent-think-tank)**

Use it, fork it, improve it. If you build something cool, share it.

---

## What's Next

I'm experimenting with:
- **Memory layers:** Letting agents retain context across runs
- **Voice integration:** Morning briefings via TTS
- **Action loops:** The Cook recommending, me confirming, agents executing

The ultimate goal: a system that doesn't just tell me what to do—it helps me do it.

---

*If you try this, let me know what the Cook tells you. Mine just said to stop writing this post and ship the code. He's not wrong.*
