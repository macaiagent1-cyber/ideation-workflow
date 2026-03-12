# Idea Card Format

Every idea extracted from raw input gets standardized into this format. The goal is to make every idea comparable — same fields, same level of detail, regardless of how it arrived.

## Required Fields

```markdown
### ID-XXX: [Short Descriptive Title]

**Source:** [DM from @username / conversation / user-added / notes]
**Requester:** [Name or handle, if known. "Community" if from multiple people]
**Raw quote:** "[Original words, verbatim or close paraphrase]"

**Core request:** [One sentence. What does the person actually want to exist or happen?]

**Problem it solves:** [One sentence. What pain point or gap does this address?]

**Domain:** [The subject area — e.g., content production, research, education, business ops, dev tooling]

**Initial signals:**
- Complexity: [simple / moderate / complex / unclear]
- Recurrence: [one-off request / asked by multiple people / recurring need]
- Specificity: [vague wish / clear ask / detailed spec]
```

## Field Guidelines

**Short Descriptive Title** — Noun phrase, not a sentence. "Weekly report automation" not "Someone wants their weekly reports automated." Max 8 words.

**Core request** — Strip away the requester's framing and get to the functional ask. "I wish I could..." becomes "A system that does X." If the request is vague, state the clearest interpretation and flag uncertainty.

**Problem it solves** — Why does this person want this? What are they doing manually, badly, or not at all today?

**Domain** — Pick the primary domain. If it spans two, pick the one where the value lives. Tag the secondary in parentheses if genuinely split.

**Initial signals** — First-pass gut reads. These get replaced by rigorous scoring in later stages. They exist here to help pattern analysis in Stage 02.
- **Complexity**: How much work would this take to deliver? Simple = a template or prompt. Complex = multi-component system.
- **Recurrence**: Is this one person's niche need, or do multiple people want something like this?
- **Specificity**: Did the requester describe exactly what they want, or is it a vague direction?

## Handling Ambiguous Requests

If a request could mean two different things, create two separate idea cards and note: `**Ambiguity note:** This may be the same request as ID-XXX. Keeping separate until user clarifies.`

## Handling Multi-Part Requests

If one DM contains three distinct ideas, create three cards. Link them: `**Related:** ID-XXX, ID-YYY (from same requester, same conversation)`
