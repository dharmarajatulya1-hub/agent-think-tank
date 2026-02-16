# Agent Think Tank

A multi-agent orchestration system for personal productivity. Three specialized agents (Saul, Mike, Gus) analyze your vault, habits, and market intel. One synthesis layer (The Cook) turns their insights into actionable moves.

## The Problem

You have:
- 📚 Hundreds of notes, ideas, and half-finished projects
- 📊 Habit trackers, health data, and discipline logs  
- 📰 News feeds, market trends, and strategic intelligence

And yet... you still feel stuck. Why?

**Because information isn't insight. And planning isn't execution.**

## The Solution

The Think Tank uses **specialized agents with distinct personalities** to analyze different domains, then **synthesizes their insights** into a single actionable brief.

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

## The Agents

| Agent | Role | Domain | Personality |
|-------|------|--------|-------------|
| **Saul** | The Vault Fixer | Knowledge, notes, projects | Finds the angles others miss |
| **Mike** | The Cleaner | Habits, health, discipline | No half measures, no sugarcoating |
| **Gus** | The Strategist | Markets, trends, threats | Plans ten moves ahead |
| **Cook** | The Synthesis Layer | Cross-domain connections | Cooks intel into pure insight |

## Quick Start

1. **Copy the agent prompts** from `agents/` into your LLM system of choice
2. **Set up your data sources:**
   - Saul: Point at your notes/knowledge base
   - Mike: Connect your habit tracking data
   - Gus: Configure news/intelligence feeds
3. **Run the agents** (sequentially or in parallel)
4. **Feed their outputs to the Cook** for synthesis
5. **Read the brief** and execute the recommended move

See [docs/ARCHITECTURE.md](docs/ARCHITECTURE.md) for detailed implementation options.

## Example Output

After running the Think Tank, you might receive:

```markdown
# 🧪 The Cook's Brief — 2026-02-16

## 💡 The Connection
Your vault shows 20+ "learning projects" started. Your habit logs show 
4 hours/day of "research." Gus reports the market window for your target 
skill is closing. You're planning your way out of execution.

## ⚡ The Tensions
- **Said:** "I'm transitioning to AI Engineering"
- **Did:** 90% business dev, 10% technical study

## 🎯 The Play
Stop building the landing page. Ship one ML project this week. 
The portfolio piece beats the business plan.

## 🔮 The Wild Card
Your note-taking system IS the product. Sanitize it and open-source 
the orchestration pattern. That's the resume.
```

## File Structure

```
agent-think-tank/
├── agents/
│   ├── saul-goodman.md      # Vault analysis agent
│   ├── mike-ehrmantraut.md  # Habit/discipline agent
│   ├── gus-fring.md         # Market intelligence agent
│   └── synthesis-layer.md   # The Cook (synthesis)
├── docs/
│   └── ARCHITECTURE.md      # Detailed architecture guide
├── examples/
│   ├── saul-example.md      # Sample Saul output
│   ├── mike-example.md      # Sample Mike output
│   ├── gus-example.md       # Sample Gus output
│   └── synthesis-example.md # Sample Cook output
└── README.md
```

## Why This Works

1. **Specialization beats generalization.** Each agent has a narrow focus and a strong personality. No more generic advice.

2. **Tensions reveal truth.** The Cook explicitly looks for contradictions between your vault, habits, and market reality.

3. **Output constraints force clarity.** Strict report formats make synthesis possible and prevent AI rambling.

4. **One action beats ten suggestions.** The Cook delivers ONE specific move, not a list of options.

## Customization

The Breaking Bad personas are scaffolding. The pattern works with any distinct voices:
- Optimist / Pessimist / Realist
- Past / Present / Future  
- Analyst / Creative / Critic

The key is that each perspective is **distinct and consistent**.

## Advanced: The Scout

Add a fifth agent: **The Scout** explores new territories—side income ideas, learning resources, networking opportunities. The Scout doesn't report regularly, only when something genuinely new appears.

## License

MIT. Use it, fork it, improve it. If you build something cool, share it.

---

*Built with 🔥 and a healthy disrespect for "productivity systems" that don't produce.*
