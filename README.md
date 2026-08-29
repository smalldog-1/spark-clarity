# Spark Clarity ✨

Transform vague inspirations into clear, structured concepts with AI-guided inquiry.

[中文文档](./README_CN.md)

## Overview

Spark Clarity is a systematic idea clarification assistant that helps you organize fuzzy inspirations into clear, comprehensive product concepts through structured questioning and analysis.

Unlike traditional brainstorming or consensus tools (like "grill me"), Spark Clarity runs a **two-mode workflow**: **guided Q&A** for the parts only you know (origin, concept, the signature you want it to have) and **independent AI research** for the objective parts (competitive landscape, competitor weaknesses, root causes, solutions) — precisely because if you could already analyze the market yourself, you would not need this conversation. It guides you to:
- Explore the origin and motivation behind your idea
- Clarify the core concept (appropriate abstraction, avoiding premature details)
- Understand the competitive landscape
- Draw out the idea's signature — what you want it to stand for
- Deep-dive into competitor pain points and solutions
- Output a concise, impactful analysis document

## Workflow

```
1. Origin Exploration → Why does this idea exist?         [Q&A]
          ↓
2. Concept Clarification → What do you want to build?     [Q&A]
          ↓
3. Landscape Mapping → AI research: similar products & why [AI]
          ↓
4. Signature → What do you want it to stand for?        [Q&A]
          ↓
5. Competitive Deep-Dive → Pain points, root causes, solutions [AI]
          ↓
6. Documentation → Structured Markdown report             [AI]
```

## Getting Started

### Installing as a standard skill

This repo IS the skill directory. Clone it into a pi skill location and it is discovered automatically:

```bash
# global (user-wide)
git clone https://github.com/smalldog-1/spark-clarity.git ~/.pi/agent/skills/spark-clarity
# or project-level
cd your-project && git clone https://github.com/smalldog-1/spark-clarity.git .pi/skills/spark-clarity
```

Then start a conversation; pi loads the skill when your idea matches its description, or force it with `/skill:spark-clarity`. Works in any Agent Skills-compatible harness (Claude Code: `~/.claude/skills/`).

### Using without installing

1. Paste the contents of `SKILL.md` into a fresh conversation
2. Start a new conversation - AI will guide you through the process
3. Answer questions step by step (the Q&A phases)
4. Receive a complete analysis document

See [GETTING_STARTED.md](./GETTING_STARTED.md) for detailed instructions.

## Features

- **Two-Mode Division**: Q&A for your subjective insights; independent AI research for market facts — never mixed
- **Systematic Process**: Six clear phases, not random conversation
- **Appropriate Granularity**: Avoid premature implementation details
- **Credible Competitive Research**: AI delivers the landscape and deep-dive from its own knowledge (marked ⚡ AI-research)
- **Structured Output**: Auto-generated, ready-to-use analysis reports with provenance labels
- **Focused Interaction**: One question at a time for efficient dialogue

## Output Example

The final document includes:
- 🎯 Origin & Motivation
- 💡 Core Concept (target users, value, key scenarios)
- 🌍 Competitive Landscape
- ✨ Signature & Vision (from the user)
- 🔍 Competitive Analysis (limitations, root causes, solutions)
- 🚀 Strategic Positioning
- 📋 Key Insights

See [EXAMPLE.md](./EXAMPLE.md) for a complete conversation example.

## Use Cases

- Product managers clarifying new product ideas
- Entrepreneurs validating startup directions
- Developers planning open-source projects
- Designers defining design directions
- Anyone needing to transform vague inspirations into clear plans

## Comparison

| Tool | Purpose | Approach |
|------|---------|----------|
| Grill Me | Build consensus with AI | Through challenge and questioning |
| Spark Clarity | Structure inspiration | Through systematic guidance |
| Traditional Brainstorming | Divergent thinking | Free association |
| Spark Clarity | Convergent thinking | Structured analysis |

## Contributing

Contributions are welcome! See [CONTRIBUTING.md](./CONTRIBUTING.md).

## License

MIT License - see [LICENSE](./LICENSE) for details.

---

**Let's turn your spark into clarity.** ✨
