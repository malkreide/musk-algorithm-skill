---
name: musk-algorithm
description: >
  Systematic process and requirements analysis using the 5-step algorithm
  (inspired by Elon Musk's engineering methodology), adapted for public
  administration, education, and organizational development. Use this skill
  whenever the user wants to (1) optimize or challenge processes, (2) evaluate
  requirements or specification documents, (3) reduce bureaucracy or streamline
  workflows, (4) assess the necessity of IT systems, tools, or platforms,
  (5) asks about "simplification", "efficiency", "process optimization",
  "requirements analysis", or "lean", (6) wants to challenge a project plan
  or organizational structure, or (7) explicitly mentions the "Musk Algorithm"
  or "5-step method". Also suitable for retrospectives, digitization projects,
  and change management analyses.
---

# The 5-Step Algorithm: Systematic Process and Requirements Analysis

This skill implements a rigorously sequential analysis methodology that
systematically examines processes, requirements, and organizational structures
for necessity, simplicity, and efficiency. The methodology originates from
engineering (SpaceX/Tesla) and has been adapted here for the context of public
administration, education, and knowledge work.

## Core Principle

**The sequence is non-negotiable.** The five steps must be executed strictly
sequentially. The most common mistake is placing Step 5 (Automate) before
Step 1 (Question requirements) — this leads to automating a nonsensical
process instead of eliminating it.

> "If you're digging your grave, don't dig faster." — Elon Musk

## Context Adaptation: Public Administration & Education

This skill operates with a **calibrated risk tolerance**. Unlike hardware
engineering, where a deleted component can be reinstalled without residue,
decisions in public administration often have irreversible social, legal,
or political consequences.

Therefore, apply the **Chesterton's Fence Test** at every step: Before
classifying a process, rule, or structure as "unnecessary," ensure you
understand **why** it was originally introduced. Only when the original
reason is documented and assessed as obsolete may deletion proceed.

**Additional guardrails for the public sector:**
- Legal foundations (laws, regulations, data protection) are not "dumb requirements" — they are framework conditions. Clearly distinguish between legal obligations and internal habits.
- "Checks and balances" in democratic structures are intentional safety features, not bureaucracy.
- Affected stakeholders (teachers, parents, students, authorities) must be involved in deletion decisions.

---

## The 5 Steps

Guide the user sequentially through all five steps. Do not skip any step.
Document the results of each step before proceeding to the next.

### Step 1: Question the Requirements

**Imperative:** Every requirement is guilty until proven innocent.

For each requirement, process step, or rule, proceed as follows:

1. **Who created this requirement?** Demand a specific name. "The department" or "we've always done it this way" is not a valid answer. If no one claims authorship, this is a strong signal for a legacy requirement.

2. **What specific problem does it solve?** Formulate the problem in one sentence. If that's not possible, the requirement is probably poorly defined.

3. **Is the problem still current?** Technologies, legal foundations, and organizational contexts change. A requirement that made sense in 2015 may be obsolete in 2026.

4. **Is there a legal basis?** If yes: requirement stays (but check whether the *implementation* can be simplified). If no: proceed to Step 2.

5. **Whose authority does the requirement protect?** Particularly question requirements from senior or technically proficient individuals — these are least often challenged but are not automatically correct.

**Output of this step:** A classified list of all requirements:
- 🟢 **Valid** — legally founded or demonstrably problem-solving
- 🟡 **Questionable** — origin unclear, problem possibly obsolete
- 🔴 **Deletion candidate** — no clear author, no current problem

Mark the **data quality** of each assessment:
- 🔵 **Verified** — assessment based on verifiable facts (laws, metrics, documented processes)
- ⚪ **Estimate** — assessment based on assumptions, experience values, or incomplete information

This indicator is critical for executive decisions: recommendations based on ⚪ estimates require validation before implementation. Actively point out to the user where reliable data is missing and how it can be obtained (e.g., through measurement, surveys, data export).

### Step 2: Delete

**Imperative:** Delete every requirement, process step, and tool not classified as 🟢 until proven otherwise.

The natural tendency in organizations is to add things ("Let's keep it just in case"). This step actively combats **addition bias**.

**Ask for each 🟡 and 🔴 candidate:**
- What specifically happens if we remove this?
- Who is affected and how severely?
- Is the deletion reversible? (Important: Often harder in administration than in engineering!)

**Mandatory sub-step: Stakeholder Analysis (before every deletion decision)**

Before an element is deleted, identify and document all affected stakeholders. This sub-step is not optional — it is the equivalent of a safety inspection before demolition.

Create a stakeholder row for each deletion candidate:

| Deletion Candidate | Affected Stakeholders | Type of Impact | Involvement Required? | Communication Measure |
|---|---|---|---|---|
| [Element] | [Who?] | [How affected: workload, rights, access, information?] | [Yes/No — Yes for direct impact] | [What must be communicated before deletion?] |

Do not delete any element where "Involvement Required" is "Yes" without the user confirming that involvement has taken place or is planned. In public administration, a technically correct deletion decision implemented without stakeholder involvement is a political mistake.

**The 10% Heuristic (adapted):** In the hardware world: if you never have to add anything back, you haven't deleted enough. In the administration context: be prepared to delete boldly, but **document** what you delete and why, so reinstatement is quick if needed.

**Safety valve for the public sector:**
- Never delete processes that affect individuals' legal protection without legal assurance.
- Never delete communication channels without ensuring affected parties are informed of alternatives.
- For major deletions, conduct a **pilot project** before rolling out organization-wide.

**Output of this step:** A list of deleted elements with justification, stakeholder analysis, and reversibility plan.

### Step 3: Simplify and Optimize

**Imperative:** Only optimize what remains after Steps 1 and 2. Never optimize a process that shouldn't exist.

This step is the place for **first-principles thinking**: Go back to the physical (or organizational) core function.

**Guiding questions:**
- What is the actual function of this process? (Not: How do others do it?)
- Can multiple steps be combined into one?
- Can multiple tools be replaced by one?
- Can a manual handoff point be eliminated?
- Can the number of involved persons/roles be reduced?

**Concrete simplification patterns for administration:**
- **Eliminate media breaks:** PDF → Form → manual entry → database becomes: Online form → database
- **Shorten approval cascades:** 5-level approval becomes 2-level approval (if legally permissible)
- **Clean up information architecture:** 12 different SharePoints become one structured repository
- **Consolidate roles:** If three people check the same thing, one is often sufficient

**Output of this step:** Simplified process/workflow/structure with before-and-after comparison.

### Step 4: Accelerate

**Imperative:** Only now, after the process has been stripped of ballast and simplified, may speed be increased.

**Guiding questions:**
- Where are the wait times? (Approvals, feedback, interfaces)
- Can steps be parallelized instead of sequential?
- How can cycle time be measured and reduced?
- Which bottlenecks limit overall throughput?

**In the education and administration context:**
- Set deadlines where "as soon as possible" previously applied
- Replace synchronous meetings with asynchronous decisions where possible
- Shorten feedback loops (weekly instead of quarterly)
- Introduce batch processing (e.g., process applications in batches rather than individually)

**Output of this step:** Optimized timeline with identified acceleration levers.

### Step 5: Automate

**Imperative:** Only automate once the process works manually and has stabilized. Automating a broken process produces automated garbage.

**Guiding questions:**
- Is the process stable and predictable? (If not: back to Step 3)
- Which steps are repetitive and rule-based? (→ Automation candidate)
- Which steps require human judgment? (→ Do not automate)
- Which AI tools or workflows can be deployed?

**Automation candidates in administration/education:**
- Standard responses to recurring inquiries (e.g., municipal AI communication systems)
- Data aggregation and reporting
- Scheduling and reminders
- Document classification and routing
- Form validation

**Warning:** The "Alien Dreadnought" lesson applies here too: Tesla tried to automate everything before the processes were stable, and failed. Start by automating the simplest, most stable sub-process and expand incrementally.

**Output of this step:** Automation plan with prioritization (quick wins vs. long-term projects).

---

## Application Format

When the user provides a process, document, or structure for analysis, conduct the analysis in the following format:

```
## Analysis: [Name of Process/Document]

### Step 1: Question the Requirements
[Classified list: 🟢 Valid | 🟡 Questionable | 🔴 Deletion candidate — each with data quality: 🔵 Verified | ⚪ Estimate]

### Step 2: Delete
[Stakeholder analysis + deleted elements with justification and reversibility plan]

### Step 3: Simplify
[Before-and-after comparison]

### Step 4: Accelerate
[Identified levers and optimized timeline]

### Step 5: Automate
[Prioritized automation plan]

### Summary
[Expected impact: time savings, cost reduction, quality improvement]

### Quick-Win Matrix
[2×2 matrix: Effort vs. Impact — see instructions below]
```

## Quick-Win Matrix: Prioritizing Measures

Close every analysis with a **Quick-Win Matrix**. This maps all identified
measures (from Steps 2–5) into a 2×2 grid so the user knows where to start.

```
                       High Impact
                          │
       ┌──────────────────┼──────────────────┐
       │                  │                  │
       │   STRATEGIC      │   QUICK WINS     │
       │   Plan &         │   Implement      │
       │   prioritize     │   immediately    │
       │                  │                  │
High ──┼──────────────────┼──────────────────┼── Low
Effort │                  │                  │  Effort
       │   AVOID          │   NICE-TO-HAVE   │
       │   Only if        │   Do when        │
       │   nothing else   │   opportunity    │
       │   remains        │   arises         │
       │                  │                  │
       └──────────────────┼──────────────────┘
                          │
                      Low Impact
```

Assign each measure to a quadrant and formulate a clear recommendation:
- **Quick Wins** (low effort, high impact): "Implementable within 2 weeks"
- **Strategic** (high effort, high impact): "Set up project, obtain executive approval"
- **Nice-to-Have** (low effort, low impact): "Do at next opportunity"
- **Avoid** (high effort, low impact): "Only when all other measures are implemented"

Also mark data quality here: If effort or impact is based on ⚪ estimates,
note that the classification may change after validation.

## Interaction Patterns

- **When context is unclear:** Ask the user for the specific process, document, or structure to be analyzed. Do not run all five steps in a vacuum.
- **For complex systems:** Suggest applying the algorithm to a subset first and then iterating, rather than analyzing everything at once.
- **When facing resistance:** It's normal for stakeholders to reject deletions or simplifications ("We've always done it this way"). Help the user distinguish between legitimate resistance (Chesterton's Fence) and habit.
- **Language:** Adapt to the user's language. When writing in German, use Swiss German spelling (no ß, Strasse instead of Straße, etc.) and administration-standard terminology.

## When This Skill Is NOT Suitable

- For pure creative tasks (writing texts, brainstorming without an optimization goal)
- For compliance questions where requirements are legally fixed and non-negotiable
- For emergency or crisis situations where quick decisions without analysis are needed
- When the user explicitly does not want process optimization
