# GR Company Evaluations

Claude Code skills for evaluating software companies using **Gokul Rajaram's 8 Moats Framework**, derived from his interview with Harry Stebbings on 20VC.

Gokul's thesis: every software company's defensibility can be measured across 8 distinct moats. Companies with **4 or more strong moats are "pretty damn secure."** Companies with zero are "screwed."

## The 8 Moats

Each moat has its own evaluation skill that scores a company 0-10 with detailed analysis:

| Skill | Moat | What It Measures |
|---|---|---|
| `/evaluate-data-moat` | **Data Mode** | Proprietary data assets that compound with every interaction. Does the data flywheel create something competitors can't replicate? A thin AI wrapper on GPT doesn't count. |
| `/evaluate-workflow-moat` | **Workflow Mode** | How deeply the product is embedded in daily operations. Is it a system of record or a lightweight layer? Has the company rebuilt the experience end-to-end with AI or just bolted it on? |
| `/evaluate-regulatory-moat` | **Regulatory Mode** | Regulatory barriers and compliance requirements that protect incumbents. Licenses, certifications, and legal frameworks that AI labs can't bypass. Fintech is the canonical example. |
| `/evaluate-distribution-moat` | **Distribution Mode** | Proprietary distribution channels — platform defaults, partnerships, wedge products. Being Shopify's preferred email tool or Google's default on Apple devices. Not brand — Gokul explicitly excludes brand as a moat. |
| `/evaluate-ecosystem-moat` | **Ecosystem Mode** | Third-party developer/partner ecosystems built around the platform. Apps, integrations, consulting partners, custom workflows. Salesforce's SI network is the gold standard. |
| `/evaluate-network-moat` | **Network Mode** | Network effects where more users make the product more valuable for each user. Direct (Facebook), marketplace (Faire/DoorDash), or data-driven (Google). |
| `/evaluate-physical-moat` | **Physical Infrastructure** | Real-world physical assets — data centers, logistics networks, hardware. Pure software companies score near zero here. Hyperscalers and physical-world operators own this moat. |
| `/evaluate-scale-moat` | **Scale Mode** | Cost advantages from operating at massive scale. AI has destroyed traditional software scale advantages — only physical/infrastructure scale still counts in 2026. |

## The Orchestrator

**`/evaluate-company-moats`** is the master skill. Give it a company name and it runs all 8 moat evaluations in parallel, then synthesizes:

- Scorecard table with all 8 moat scores (0-10 each, out of 80 total)
- Gokul's threshold check (4+ moats scoring 5+ = "pretty damn secure")
- Overall durability rating (Low / Medium / High / Very High)
- AI disruption risk assessment
- Key strengths and vulnerabilities
- Retention and quality indicators
- Multi-product assessment
- Access product vs. work product classification
- "Gokul's Verdict" — a direct assessment in his analytical voice, comparing to his benchmark companies (Salesforce = 3 moats, Atlassian = 3, ServiceTitan = 32 products, etc.)

## Usage

These are [Claude Code](https://docs.anthropic.com/en/docs/claude-code) slash commands. Clone this repo and run Claude Code from the repo directory:

```bash
# Evaluate a single moat
/evaluate-data-moat Adobe

# Run the full 8-moat evaluation
/evaluate-company-moats Snowflake
```

Each skill uses web search to research the company, so evaluations are grounded in current public information.

## Framework Source

Based on Gokul Rajaram's interview on [20VC with Harry Stebbings](https://www.youtube.com/watch?v=20vc), where he outlines his framework for evaluating software company defensibility in the age of AI. Key principles:

- **Brand is not a moat.** Switching costs are going to zero. Data portability is increasing. Brand alone won't save you.
- **Data + Workflow are the anchors** for pure software companies. Everything else is harder to claim.
- **Multi-product is essential.** "You cannot be a single product company." ServiceTitan has 32 products. Robinhood has 13 product lines over $100M.
- **AI is eroding moats.** "Now everybody can produce software as cheaply as anybody else." Companies must ask: where is the profit pool — in the data or the workflows?
- **Durability over margins.** Gokul cares more about retention and defensibility than current margins. "Good companies, if they're defensible, they will have the ability to increase margin."
