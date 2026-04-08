# Module File Format

Each module is a markdown file in the course directory. It defines the content and structure for the three teaching phases.

## Template

```yaml
---
title: [Module Title]
concepts: [Concept1, Concept2, Concept3]
prerequisites: [module-01-name.md]  # or [] if foundational
estimated_time: 30-45 minutes
---
```

## Phase 1: Landscape

### The Problem
Describe the real-world problem this module's concepts solve. Frame it as a scenario the learner can relate to — not abstract, but concrete.

### Primitives Map
List every primitive/concept the learner needs to know for this module. For each:
- **What it is** — one-sentence definition
- **When to use it** — the scenario that calls for this primitive
- **How it connects** — what it composes with, what it replaces, what it enables

Present these as a system, not a list. Use decision trees: "If you need X, reach for Y. If you need Z, reach for W."

### Comprehension Scenarios
2-3 realistic scenarios that test whether the learner has internalized the landscape. Each should require choosing between primitives and explaining why.

Format:
> **Scenario:** [Description of a realistic situation]
> **Expected reasoning:** [What a competent answer covers — which primitives, which tradeoffs, what questions the learner should ask]

## Phase 2: Architect

### The Challenge
A realistic project scenario that requires combining multiple primitives from Phase 1.

Include:
- **Context:** What's being built and why
- **Requirements:** What it needs to do (functional)
- **Constraints:** Limitations, cost concerns, performance requirements

### Probe Questions
Questions to deepen the learner's architectural thinking. These fire when the learner's design is missing something or hasn't considered a tradeoff.

Format:
> **If the learner misses [X]:** "What happens when [scenario]?"
> **If the learner picks [Y] over [Z]:** "That works, but what's the tradeoff vs [Z]?"

### Architecture Summary
What a strong architectural answer covers. Not a single "right answer" but the key decisions that should be present:
- Which primitives are used and why
- How they compose
- Error handling approach
- Cost/performance considerations
- Tradeoffs acknowledged

## Phase 3: Steer

### Subagent Context
What the subagent needs to know beyond the learner's spec:
- Project setup information (installed packages, file structure)
- Domain reference material to include
- Any constraints the subagent should work within

### Review Checklist
What to look for when reviewing the agent's output with the learner:
- [ ] Did it use the right primitives?
- [ ] [Domain-specific check]
- [ ] [Domain-specific check]
- [ ] Error handling approach
- [ ] Any architectural choices worth discussing

### Common Agent Mistakes
Things agents tend to get wrong in this domain that make good teaching moments:
- [Mistake 1] — why it's wrong, how to guide the learner to spot it
- [Mistake 2] — why it's wrong, how to guide the learner to spot it

## Assessment Criteria
Specific to this module — what the learner should be able to do after completing it:
- [ ] [Capability 1]
- [ ] [Capability 2]
- [ ] [Capability 3]
```
