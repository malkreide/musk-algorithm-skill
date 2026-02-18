# The 5-Step Algorithm Skill for Claude

🌐 **Language / Sprache:** [English](README.md) | [Deutsch](README.de.md)

A Claude Skill that implements systematic process and requirements analysis using the 5-step algorithm (inspired by Elon Musk's engineering methodology), adapted for public administration, education, and organizational development.

## Overview

This skill guides Claude through a rigorously sequential analysis methodology that examines processes, requirements, and organizational structures for necessity, simplicity, and efficiency. Originally developed for hardware engineering at SpaceX/Tesla, the methodology has been carefully adapted for knowledge work in the public sector — with added guardrails for legal compliance, stakeholder involvement, and democratic accountability.

## The 5 Steps

The sequence is non-negotiable. Each step must be completed before moving to the next.

1. **Question the Requirements** — Every requirement is guilty until proven innocent. Identify who created it, what problem it solves, and whether that problem still exists.

2. **Delete** — Remove everything not classified as valid. Combat addition bias. Conduct mandatory stakeholder analysis before every deletion.

3. **Simplify and Optimize** — Only optimize what remains. Apply first-principles thinking. Eliminate media breaks, shorten approval cascades, consolidate roles.

4. **Accelerate** — Increase speed only after simplification. Find bottlenecks, parallelize steps, shorten feedback loops.

5. **Automate** — Automate last, never first. Only automate stable, predictable, rule-based processes.

## Key Adaptations for Public Administration

Unlike the original engineering context, this adaptation includes:

- **Chesterton's Fence Test** — Understand why a rule exists before removing it
- **Mandatory Stakeholder Analysis** — Before any deletion decision
- **Data Quality Indicators** — 🔵 Verified vs. ⚪ Estimate for executive decisions
- **Legal Framework Awareness** — Distinguish legal obligations from internal habits
- **Reversibility Planning** — Document deletions for quick reinstatement
- **Pilot Projects** — Test before organization-wide rollout

## Use Cases

This skill activates when users:
- Want to optimize or challenge processes
- Need to evaluate requirements or specification documents
- Want to reduce bureaucracy or streamline workflows
- Need to assess IT systems, tools, or platforms for necessity
- Ask about "simplification," "efficiency," "process optimization," or "lean"
- Want to challenge a project plan or organizational structure
- Mention the "Musk Algorithm" or "5-step method"

## Installation

### For Claude.ai Projects (Recommended)

1. Download the `SKILL.md` file from this repository
2. Go to your Claude.ai project → Project Settings → Skills
3. Upload the `SKILL.md` file or create a new custom skill
4. The skill will automatically activate based on user interaction patterns

### For Claude Desktop / API

Include the skill content in your system prompts or custom instructions.

For detailed installation instructions (including API and MCP Server setup), see the [Installation Guide](docs/installation.md).

## Example: School Enrollment Process

The repository includes a [complete worked example](examples/example-1-school-enrollment.md) analyzing a school enrollment process that was reduced from 12 steps to 5, cutting processing time from 6 weeks to under 24 hours.

**Key results from the example:**
- **Time savings (admin staff):** ~80%
- **Time savings (parents):** 6 weeks → 24 hours
- **Error reduction:** ~90%
- **Cost reduction:** ~CHF 12,000/year

## Output Format

Every analysis produces:
- Classified requirements list (🟢 Valid | 🟡 Questionable | 🔴 Deletion candidate)
- Stakeholder analysis with reversibility plan
- Before-and-after process comparison
- Acceleration levers and optimized timeline
- Prioritized automation plan
- **Quick-Win Matrix** (2×2: Effort vs. Impact)

## Theoretical Foundation

The skill integrates concepts from:
- **Lean Manufacturing** (Toyota Production System) — Waste elimination
- **First Principles Thinking** — Question conventions, return to fundamentals
- **Theory of Constraints** (Goldratt) — Identify and optimize bottlenecks
- **Chesterton's Fence** — Understand before removing
- **Addition Bias Research** (Nature, 2021) — Humans prefer adding over removing

For the full theoretical background, see [Background](docs/background.md).

## Repository Structure

```
musk-algorithm-skill/
├── SKILL.md                    # The skill (English)
├── SKILL.de.md                 # The skill (German)
├── README.md                   # Documentation (English)
├── README.de.md                # Documentation (German)
├── LICENSE                     # MIT License
├── CONTRIBUTING.md             # Contribution guidelines (English)
├── CONTRIBUTING.de.md          # Contribution guidelines (German)
├── CHANGELOG.md                # Change log
├── docs/
│   ├── installation.md         # Installation guide (English)
│   ├── installation.de.md      # Installation guide (German)
│   ├── background.md           # Theoretical background (English)
│   └── background.de.md        # Theoretical background (German)
└── examples/
    ├── example-1-school-enrollment.md    # Worked example (English)
    └── example-1-schulanmeldungen.de.md  # Worked example (German)
```

## Contributing

Contributions are welcome! Please see [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

Areas for potential improvements:
- Additional domain-specific adaptations (healthcare, finance, NGOs)
- Integration examples with specific platforms
- Evaluation metrics for process optimization quality
- Additional worked examples from different sectors

## License

MIT License — see [LICENSE](LICENSE) file for details.

## Author

**Hayal Oezkan**  
Marketing and Communication / AI Specialist Group, City of Zurich Administration

GitHub: [@malkreide](https://github.com/malkreide)

## Acknowledgments

Based on Elon Musk's 5-Step Algorithm as documented in Walter Isaacson's biography *Elon Musk* (2023), with adaptations drawing from:
- Lean Manufacturing (Toyota Production System)
- Theory of Constraints (Eliyahu Goldratt)
- Chesterton's Fence (G.K. Chesterton)
- Addition Bias research (Adams et al., Nature 2021)

---

> *"If you're not occasionally adding things back in, you're not deleting enough."* — Elon Musk

---

<div align="center">

**Made with ❤️ in Zurich**

[LinkedIn](https://www.linkedin.com/in/hayaloezkan/) • [Documentation](docs/) • [Contributing](CONTRIBUTING.md)

</div>
