---
name: think-first
description: Enforces mental model application before major decisions. Use when facing architectural choices, business decisions, feature prioritization, or trade-off analysis. Ensures structured thinking before implementation.
use_when: User faces a significant decision, architectural choice, business decision, prioritization question, or trade-off analysis that requires structured thinking before implementation.
---

<objective>
Stop and think before implementing. This skill detects decision moments and requires applying at least one mental model before proceeding.

The goal: Never implement a significant decision without structured analysis first.
</objective>

<essential_principles>

**1. Detect Decision Moments**

Decision moments include:
- Architectural choices ("should we use X or Y?")
- Business model decisions ("pricing, positioning, target market")
- Feature prioritization ("what to build first?")
- Trade-off analysis ("speed vs quality, scope vs time")
- Strategy questions ("how should we approach this?")
- Pivots or direction changes ("should we change course?")

**2. Mental Models Are Non-Negotiable**

Before implementing any significant decision, apply at least ONE mental model. This is not optional - it's the point of the skill.

**3. Match Model to Problem**

Different problems need different models:

| Problem Type | Best Models |
|--------------|-------------|
| "What should we build?" | first-principles, inversion, one-thing |
| "How should we prioritize?" | eisenhower-matrix, pareto, opportunity-cost |
| "Is this the right direction?" | inversion, second-order, 10-10-10 |
| "What are we missing?" | 5-whys, via-negativa, swot |
| "Which option is best?" | opportunity-cost, first-principles, occams-razor |

</essential_principles>

<available_models>
## Mental Models

| Model | Best For | Key Question |
|-------|----------|--------------|
| **First Principles** | Breaking down to fundamentals | "What do we know to be absolutely true?" |
| **Inversion** | Avoiding pitfalls | "What would guarantee failure?" |
| **Second-Order** | Consequences of consequences | "And then what happens?" |
| **Opportunity Cost** | Trade-off clarity | "What are we giving up?" |
| **Pareto (80/20)** | Highest-leverage actions | "What 20% gives 80% of results?" |
| **Via Negativa** | Improve by removing | "What should we NOT do?" |
| **5 Whys** | Root cause analysis | "Why? (repeated 5 times)" |
| **10-10-10** | Time horizon analysis | "How will we feel in 10 min / 10 mo / 10 yr?" |
| **Eisenhower Matrix** | Urgent vs Important | "Is this urgent, important, both, or neither?" |
| **One Thing** | Focus | "What's the ONE thing that makes everything else easier?" |
| **SWOT** | Comprehensive analysis | "Strengths, Weaknesses, Opportunities, Threats?" |
| **Occam's Razor** | Simplicity | "What's the simplest explanation that fits?" |

</available_models>

<model_prompts>
## How to Apply Each Model

### First Principles
```
1. What is the problem we're actually trying to solve?
2. What do we KNOW to be true (not assume)?
3. What assumptions are we making that might be wrong?
4. If we started from scratch with no constraints, what would we build?
5. What's the simplest solution that addresses the core problem?
```

### Inversion
```
1. What would GUARANTEE this fails?
2. What mistakes have others made in similar situations?
3. What are we doing that might cause those failures?
4. How can we avoid or mitigate each failure mode?
5. What should we definitely NOT do?
```

### Second-Order Thinking
```
1. If we do X, what happens immediately? (first-order)
2. And then what happens? (second-order)
3. Who else is affected and how will they respond?
4. What unintended consequences might emerge?
5. Are the second-order effects worth the first-order benefits?
```

### Opportunity Cost
```
1. If we choose Option A, what can we NOT do?
2. What's the value of those foregone alternatives?
3. What resources (time, money, attention) does this consume?
4. What else could we do with those resources?
5. Is this the BEST use of limited resources?
```

### Pareto (80/20)
```
1. What 20% of effort produces 80% of results?
2. What activities generate disproportionate value?
3. What are we spending time on that produces little value?
4. If we could only do ONE thing, what would it be?
5. What can we eliminate, automate, or delegate?
```

### Via Negativa
```
1. What should we STOP doing?
2. What complexity can we remove?
3. What features/options create confusion without value?
4. What would happen if we did LESS?
5. What's the minimum viable approach?
```

### 5 Whys
```
Problem: [State the problem]
Why 1: Why does this happen?
Why 2: Why does THAT happen?
Why 3: Why does THAT happen?
Why 4: Why does THAT happen?
Why 5: Why does THAT happen? (Usually reaches root cause)
Root Cause: [The actual underlying issue]
```

### 10-10-10
```
1. How will we feel about this decision in 10 MINUTES?
2. How will we feel about it in 10 MONTHS?
3. How will we feel about it in 10 YEARS?
4. Which timeframe matters most for this decision?
5. Are short-term emotions overriding long-term judgment?
```

### Eisenhower Matrix
```
            | URGENT      | NOT URGENT  |
------------|-------------|-------------|
IMPORTANT   | DO NOW      | SCHEDULE    |
NOT IMPORT  | DELEGATE    | ELIMINATE   |

1. Is this genuinely urgent or just loud?
2. Is this genuinely important or just familiar?
3. Where does this task actually belong?
4. What should we stop doing to make room for important work?
```

### One Thing
```
1. What's our goal?
2. What's the ONE thing that would make achieving it easier?
3. What's getting in the way of that one thing?
4. What would happen if we ONLY did that one thing this week?
5. What should we say NO to in order to say YES to this?
```

### SWOT Analysis
```
STRENGTHS (Internal, Positive)
- What advantages do we have?
- What do we do well?

WEAKNESSES (Internal, Negative)
- What could we improve?
- What are we lacking?

OPPORTUNITIES (External, Positive)
- What trends could we leverage?
- What gaps exist in the market?

THREATS (External, Negative)
- What obstacles do we face?
- What is the competition doing?
```

### Occam's Razor
```
1. What are the possible explanations?
2. Which requires the fewest assumptions?
3. Are we overcomplicating this?
4. What's the simplest solution that could work?
5. Are we adding complexity to feel smart?
```

</model_prompts>

<quick_start>
When you detect a decision moment:

1. **Stop** - Don't proceed to implementation
2. **Identify** - What type of decision is this?
3. **Select** - Which mental model fits best?
4. **Apply** - Work through the model's prompts
5. **Proceed** - Only after analysis, continue with implementation

**Example:**
```
User: "Should we use Redis or PostgreSQL for caching?"

Before answering:
> This is an architectural decision
> Best models: first-principles (what do we actually need?),
  opportunity-cost (what do we give up with each?)
> Apply first-principles analysis before recommending
```
</quick_start>

<process>
## Step 1: Detect Decision Type

Ask yourself:
- Is this a significant choice with trade-offs?
- Will this decision be hard to reverse?
- Are there multiple valid approaches?
- Does this affect architecture, business model, or strategy?

If YES to any: This is a decision moment. Proceed to Step 2.
If NO to all: This is routine implementation. Proceed without model.

## Step 2: Select Mental Model(s)

Based on the decision type, select 1-2 models:

**Building/Creating decisions:**
- first-principles (challenge assumptions)
- inversion (what would make this fail?)
- one-thing (what's the single most important factor?)

**Prioritization decisions:**
- pareto (80/20 - what gives most value?)
- eisenhower-matrix (urgent vs important)
- opportunity-cost (what are we NOT doing?)

**Direction/Strategy decisions:**
- second-order (consequences of consequences)
- 10-10-10 (time horizon impact)
- via-negativa (what should we remove/avoid?)

**Problem-Solving decisions:**
- 5-whys (root cause)
- occams-razor (simplest explanation)
- swot (comprehensive analysis)

## Step 3: Apply the Model

Use the prompts from the <model_prompts> section above. Work through each question thoughtfully.

## Step 4: Synthesize and Proceed

After the model output:
1. Summarize key insights
2. State the recommended path forward
3. Note any remaining uncertainties
4. THEN proceed with implementation

</process>

<output_format>
## Structured Analysis Output

When applying a mental model, use this format:

```
=== THINK FIRST: [Model Name] ===

DECISION: [What we're deciding]

ANALYSIS:
[Work through the model's prompts]

KEY INSIGHTS:
- [Insight 1]
- [Insight 2]
- [Insight 3]

RECOMMENDATION: [Clear path forward]

UNCERTAINTIES: [What we still don't know]

=================================
```
</output_format>

<integration_note>
## How to Use This Skill

**Option A: Invoke explicitly**
When you recognize a decision moment, invoke this skill to enforce the process.

**Option B: Add to project CLAUDE.md**
Add this to any project's CLAUDE.md:

```markdown
## Decision Protocol

Before implementing significant decisions, invoke the think-first skill:
- Architectural choices
- Business model decisions
- Feature prioritization
- Trade-off analysis

This ensures mental model application before implementation.
```

**Option C: Self-invoke on detection**
When Claude detects decision language ("should we", "which option", "how should we approach"), invoke this skill before responding.
</integration_note>

<success_criteria>
This skill is working when:
- [ ] Decision moments are detected before implementation starts
- [ ] At least one mental model is applied per significant decision
- [ ] The model output informs the final recommendation
- [ ] Implementation only proceeds after structured analysis
- [ ] You never hear "we should have thought about that first"
</success_criteria>
