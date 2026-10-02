# ANSELM Patterns and Anti-Patterns

> **Version:** 1.0  
> **License:** CC BY-SA 4.0

---

## Part 1: Patterns (Do This)

### Pattern 1: Questions Before Answers

**Context:** Starting analysis of new material

**Problem:** Tendency to jump to conclusions or diagrams immediately

**Solution:**

```text
Before proposing any solutions, answer:
1. Who are the stakeholders?
2. What are the constraints?
3. What is unclear or ambiguous?
4. What questions would you ask the client?
```

**Consequences:**

- ✅ Builds understanding before committing
- ✅ Surfaces assumptions early
- ⚠️ May feel slow initially

---

### Pattern 2: Three Alternatives Minimum

**Context:** Making architectural or design decisions

**Problem:** First idea gets adopted without exploring alternatives

**Solution:**

```text
Always propose at least 3 alternatives:
1. Conservative (safe, proven)
2. Innovative (risky, high potential)
3. Hybrid (balanced trade-offs)
```

**Consequences:**

- ✅ Expands solution space
- ✅ Makes trade-offs explicit
- ⚠️ Takes more time

---

### Pattern 3: Devil's Advocate Pass

**Context:** Validating a preferred solution

**Problem:** Confirmation bias — we defend what we've created

**Solution:**

```text
Once you have a solution, explicitly attack it:
"Find 5 reasons why this will fail"
"What would a skeptical reviewer say?"
"How could this go wrong in production?"
```

**Consequences:**

- ✅ Finds weaknesses before stakeholders do
- ✅ Strengthens final design
- ⚠️ May feel negative/uncomfortable

---

### Pattern 4: Progressive Disclosure

**Context:** Communicating complex systems

**Problem:** Overwhelming stakeholders with detail

**Solution:**

Create views at different abstraction levels:

1. **Level 0:** One-sentence summary
2. **Level 1:** Context diagram (5 boxes)
3. **Level 2:** Component diagram
4. **Level 3:** Detailed specifications

Let audience choose their depth.

**Consequences:**

- ✅ Respects audience's time
- ✅ Enables self-service exploration
- ⚠️ Requires discipline to maintain all levels

---

### Pattern 5: Capture-on-Decision

**Context:** During reasoning sessions

**Problem:** Decisions made but not recorded, later forgotten

**Solution:**

```text
Every time you make a decision, immediately create a record:
- What was decided
- Why (alternatives considered)
- Who decided
- What would make us revisit
```

**Consequences:**

- ✅ Builds audit trail automatically
- ✅ Enables later justification
- ⚠️ Adds overhead to session

---

### Pattern 6: Day-Zero Agreement Layer

**Context:** Starting an engagement with a messy knowledge base — synonyms,
homonyms, and the same term meaning different things in different silos

**Problem:** The ecosystem is noisy, but building a full domain ontology up
front freezes distinctions made at the moment of maximum ignorance — and rots

**Solution:**

```text
On day zero, co-create with AI the smallest agreement layer:
1. Controlled terms with aliases (one table, one afternoon)
2. Cell types (need, function, component, decision, constraint, interface)
3. Commitment relation types + the deterministic oracle that checks them

Found the CONTRACT, not the MODEL. Everything descriptive (cells,
relations, domain semantics) is derived from conversation, curated,
and verified — never authored up front.
```

**Consumer test:** every founding element must name the act that uses it
(alias checking, schema validation, the seam gate). "Sanitization" counts as
a consumer only for elements sanitization actually consumes.

**Throw-away test:** any founding element must be small enough to discard in
an afternoon.

**Consequences:**

- ✅ Cheap, corrigible, high leverage for AI coherence
- ✅ Sanitization becomes a continuous byproduct of use, not a phase
- ⚠️ Will not satisfy anyone expecting an "enterprise ontology" deliverable — by design

---

## Part 2: Anti-Patterns (Avoid This)

### Anti-Pattern 1: Diagram-First

**Symptom:** Starting with boxes and arrows before understanding the problem

**Why it's bad:**

- Commits to structure prematurely
- Hard to change once drawn
- Diagrams become "truth" instead of views

**What to do instead:**

- Build mental model first (Questions Before Answers)
- Generate diagrams as outputs, not inputs

---

### Anti-Pattern 2: Blind Trust

**Symptom:** Accepting AI output without verification

**Why it's bad:**

- AI can hallucinate facts
- AI may misunderstand context
- Errors compound over time

**What to do instead:**

- Verify key facts independently
- Challenge AI: "What's your source?"
- Use domain experts for validation

---

### Anti-Pattern 3: Infinite Session

**Symptom:** 8-hour sessions without saving progress

**Why it's bad:**

- Context window overflow
- Risk of losing work
- Diminishing returns after ~2 hours

**What to do instead:**

- Session checkpoints every 60-90 minutes
- Save Knowledge Cells continuously
- Know when to start fresh

---

### Anti-Pattern 4: Perfect Draft Syndrome

**Symptom:** Refusing to share until "it's ready"

**Why it's bad:**

- Delays feedback
- Wasted effort if direction is wrong
- Contradicts "disposable views" principle

**What to do instead:**

- Share early, label as "draft"
- Use iterations for refinement
- "Good enough" beats "perfect later"

---

### Anti-Pattern 5: Solo Knowledge

**Symptom:** All knowledge lives in one person's chat history

**Why it's bad:**

- Single point of failure
- No knowledge transfer
- Lost when person leaves

**What to do instead:**

- Extract to Knowledge Cells
- Store in shared repository (Git)
- Use Context Transfer template

---

### Anti-Pattern 6: Founding Ontology

**Symptom:** Before any design reasoning, the team (or consultant) builds a
domain ontology — classes, hierarchy, is-a/part-of — as a precondition for
starting

**Why it's bad:**

- Authored at maximum ignorance; freezes wrong distinctions
- The most expensive formalism with the fewest known consumers
- Becomes an entry ticket and a gate review in new clothes
- Rots fastest of all artifacts, because nothing at day zero is grounded in the work

**What to do instead:**

- Day-Zero Agreement Layer (contract, not model)
- Derive structure from conversations; commit only what has a consumer
- Let the oracle + steward sanitize continuously

---

## Part 3: Smells (Warning Signs)

### Smell 1: Diagram Obsession

**Symptom:** Spending more time on diagram layout than content

**Indicates:** Treating diagrams as artifacts, not views

**Action:** Remind: "Diagrams are disposable. What knowledge do they represent?"

---

### Smell 2: AI Monologue

**Symptom:** AI generates pages of text without prompting

**Indicates:** Lack of user guidance, AI filling silence

**Action:** Interrupt with specific questions. Guide the conversation.

---

### Smell 3: Context Drift

**Symptom:** AI answers start to contradict earlier decisions

**Indicates:** Context window pressure, lost coherence

**Action:** Summarize, save, start new session with Context Transfer.

---

### Smell 4: Decision Amnesia

**Symptom:** "Didn't we decide this already?"

**Indicates:** No decision records, relying on memory

**Action:** Implement Capture-on-Decision pattern immediately.

---

### Smell 5: Specification Without Validation

**Symptom:** Detailed specs that no stakeholder has seen

**Indicates:** Analysis in isolation

**Action:** Stop. Get stakeholder feedback before continuing.

---

## Summary Matrix

| Category | Item | Key Principle |
| -------- | ---- | ------------- |
| **Pattern** | Questions Before Answers | Knowledge-First |
| **Pattern** | Three Alternatives | Explore solution space |
| **Pattern** | Devil's Advocate | Challenge assumptions |
| **Pattern** | Progressive Disclosure | Respect audience |
| **Pattern** | Capture-on-Decision | Continuous coherence |
| **Pattern** | Day-Zero Agreement Layer | Contract over model |
| **Anti-Pattern** | Diagram-First | Disposable views |
| **Anti-Pattern** | Blind Trust | AI as co-pilot |
| **Anti-Pattern** | Infinite Session | Context management |
| **Anti-Pattern** | Perfect Draft | Iterative process |
| **Anti-Pattern** | Solo Knowledge | Open ecosystem |
| **Anti-Pattern** | Founding Ontology | Derive, don't found |

---

*Complexity seeking clarity.*
