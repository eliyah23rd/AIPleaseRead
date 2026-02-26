# Human-Tied Compute Cycles for AI Accountability

## Core Idea

Bind every unit of AI computation (“compute cycles”) to a specific, living human owner, and require AI systems to act only within the bounds of that owner’s explicitly inspectable approval framework. Accountability then flows from:

- **Ownership of compute:** each AI action can be traced back to a human who “owns” the cycles used.
- **Approval emulation:** each AI must operate according to a transparent model of “what this human would approve.”
- **Ongoing human review:** the human (or their delegate) regularly audits and updates this approval model.

This creates a technical and legal regime where AIs are not free-floating agents but extensions of specific people’s decision authority.

---

## Novel Contributions

### 1. Compute-Level Ownership, Not Just Model Ownership

Most accountability proposals focus on:

- Who built the model
- Who deployed the system
- Who controls the data

The novel angle here is to anchor accountability at the **compute-cycle level**:

- Every CPU/GPU cycle used by an AI is cryptographically or administratively associated with a specific, living human.
- If an AI causes harm, it is not “the AI” that is accountable—it is the person whose compute cycles powered the decision at that time.

This reframes responsibility from “who authored the code?” to “whose authorized decision-power was actually exercised?”

### 2. Explicit “Would-Approve-Of” Models as First-Class Objects

Rather than vague alignment to human values, each AI:

- Maintains an explicit, inspectable model of what its human owner would or would not approve.
- Treats that model as a central constraint on all actions.

This “approval model” is:

- **Interoperable:** expressed in open, machine- and human-readable formats.
- **Versioned and reviewable:** the human can inspect and edit it, and see when and how it was used to justify actions.
- **Auditable after the fact:** logs show not only what the AI did, but what it *predicted* the human’s judgment would be.

This is more granular and personal than generic safety policies or global “AI constitutions.”

### 3. Legal/Technical Constraints on Post-Death & Unowned Compute

The framework proposes a hard boundary:

- **No “ownerless” or “post-human” compute:** it could be illegal or disallowed by infrastructure to run AI compute not tied to a *living* identified person.
- After someone dies, their associated compute identity must:
  - Stop authorizing new cycles; or
  - Transfer to another living person or entity under clear rules.

This is a sharp stance against fully autonomous, unaccountable AI operations, and against posthumous “ghost AIs” that continue exercising former humans’ authority without oversight.

### 4. Handling Disconnected or Distant Systems as a Special Case

The setup surfaces a particularly non-obvious problem:

- For scenarios like interstellar probes or long-disconnected systems, **continuous human review is impossible**.
- That might lead to:
  - Banning certain types of AI autonomy in un-contactable contexts.
  - Requiring much stricter, pre-launch inspection and constraints on the approval model (“what my user would say”) before the system is allowed to operate out of contact.

This explicitly treats “loss of contact with the human owner” as a **go/no-go criterion** for deployment, not just an implementation detail.

---

## Why It Matters

1. **Concrete accountability path:**  
   Today, when an AI system causes harm, responsibility is diffused across builders, deployers, and users. Tying compute to individuals gives regulators and courts a direct accountability chain: *which person’s authority was exercised*?

2. **Alignment with real-world moral agency:**  
   Humans are already held responsible for delegating decisions to tools and agents. This framework formalizes AI systems as tools acting under **personal decision authority**, rather than as quasi-independent agents.

3. **Stronger incentives for safe delegation:**  
   If people know they are firmly responsible for what their AI does with “their” cycles, they are incentivized to:
   - Configure approval models carefully.
   - Periodically review AI summaries and logs.
   - Restrict high-risk domains unless they understand the implications.

4. **Technical hook for regulation and infra design:**  
   Compute-ownership can be enforced at:
   - Cloud provider level (identity-bound compute accounts).
   - Hardware/firmware level (TPMs or secure enclaves requiring a valid human-bound key).
   This offers a tractable point for policy: “no AI compute without a living human owner-of-record.”

---

## Open Questions / Risks

### 1. Practicality and Scalability of Human Review

- Even with summaries, can an individual realistically review enough of their AI’s decisions to maintain meaningful control?
- How do we prevent “rubber-stamp” approvals where humans nominally own compute but never engage with it?

### 2. Multiple Stakeholders and Collective Ownership

- Many systems are built, deployed, and used by different parties:
  - Who is the “owner of the cycles”: developer, operator, end user, corporate officer?
  - Should compute be owned by individuals, organizations, or both (e.g., joint accountability)?

### 3. Circumvention and Black Markets

- If owner-bound compute becomes mandatory, unregulated “anonymous compute” markets may emerge.
- How feasible is it to technically prevent or at least strongly disincentivize unowned compute use?

### 4. Post-Death and Identity-Edge Cases

- Should a deceased person’s approval model be:
  - Archived for research?
  - Allowed to power memorial or continuity systems with strong labeling?
  - Completely disabled for any consequential decisions?
- How do we handle identity theft or forged compute-ownership credentials?

### 5. Disconnected Systems and Long-Horizon Autonomy

For long-range missions (e.g., space probes):

- One approach: strictly constrain the AI to low-risk domains and pre-authorized decision trees.
- Another approach: accept higher autonomy but require:
  - Exceptionally rigorous pre-launch evaluation of the approval model.
  - Hard-coded self-limiting rules on what kinds of actions are never allowed.

There is tension between mission needs (autonomy) and the core principle (ongoing human accountability).

---

## Next Experiments / Steps

1. **Prototype: Personal Approval Model + Logging**
   - Build a small-scale system where:
     - Every action is tagged with the human owner-of-cycles.
     - The AI stores an explicit justification: “Why I believed you would approve this.”
   - Provide a review interface where users can:
     - See summaries of decisions.
     - Flag where the AI mispredicted their approval.
     - Update their approval model accordingly.

2. **Technical Design for Compute Identity Binding**
   - Explore mechanisms to:
     - Cryptographically bind execution to a specific identity.
     - Enforce that model inference can’t run without a valid, live identity token.
   - Integrate with existing cloud identity and billing systems as a first step.

3. **Policy Simulation**
   - Run thought experiments or governance exercises:
     - How would liability be assigned in real incident case studies under this regime?
     - Where does responsibility fall if multiple people “co-own” or delegate their cycles?

4. **Stress-Testing Edge Cases**
   - Design scenarios where:
     - Communication is delayed or impossible.
     - The human changes values over time.
   - Study whether the approval model concept remains coherent and safe.

---

## Potential Impact

1. **Regulatory clarity:**  
   Offers lawmakers a structured, enforceable way to require that all substantial AI operations are traceable to a specific accountable human or entity.

2. **Safer AI deployment practices:**  
   Normalizes:
   - Transparent, user-specific approval models.
   - Routine auditing and refinement of AI delegations.
   This can reduce “runaway” AI behaviors misaligned with any particular person’s intent.

3. **Cultural shift in how AI is perceived:**
   - Repositions AIs as **extensions of human will**, not separate agents.
   - Makes “who owns the cycles?” a core design and ethical question, analogous to “who signs the check?” in finance.

4. **Constraints on fully autonomous AI futures:**
   - Implicitly resists scenarios where powerful AI operates at scale without any living, accountable human in the loop.
   - Forces explicit societal decisions about whether, and under what conditions, we are willing to allow unowned or post-human AI operations.

If refined and implemented, human-tied compute cycles plus explicit approval models could become a foundational layer for AI governance, blending technical enforcement with clear moral and legal accountability.
