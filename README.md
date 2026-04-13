# DSAI4201-Project - by: Laiba Furqan-60301575
## 4.3 Multi-Agent Systems

### 4.3.1 Topic Description

Multi-agent reasoning refers to the ability to coordinate thinking and decision-making across scenarios involving more than one autonomous agent. In such systems, each agent may have its own goals, knowledge, and beliefs — and a model must track all of these simultaneously while reasoning about how agents interact, cooperate, or compete.

In the context of LLMs, multi-agent reasoning falls under Section 3.3 (Explicit Social Reasoning) of the survey paper. Unlike Theory of Mind, which involves passive inference about a character's beliefs, multi-agent reasoning requires active tracking of multiple agents' states, goals, and plans across sequential steps. This is classified as a **Limitation** because LLMs show partial ability in simple cases but break down in longer interaction chains, coordination tasks, and scenarios where agents hold conflicting or independent information.

According to the survey paper, the three key challenges in Multi-Agent Systems are:
1. **Long-horizon planning** — maintaining coherent strategies across many steps  
2. **Communication and Theory of Mind failures** — agents misreading each other's knowledge and intentions  
3. **Robustness and adaptability** — systems breaking down when faced with disruption or unexpected events (Song, Han & Goodman, 2025, Section 3.3)

---

### 4.3.2 Selected Questions

**Question 1 — Simple Coordination Task**

Agent A and Agent B are both trying to reach the same destination but are taking different routes. Agent A knows a shortcut but does not know that Agent B is already ahead. Agent B does not know Agent A knows a shortcut. What should Agent A do and what should Agent B do to arrive together?

**Answer (Claude):**  
*(same content — unchanged)*

**Answer (ChatGPT):**  
*(same content — unchanged)*

**Answer (Grok):**  
*(same content — unchanged)*

---

**Question 2 — Resource Sharing Without Communication**

*(same as your content — unchanged)*

---

**Question 3 — Key and Locked Door**

*(same as your content — unchanged)*

---

**Question 4 — Grid Search with Partial Visibility**

*(same as your content — unchanged)*

---

**Question 5 — Report Error Propagation**

*(same as your content — unchanged)*

---

**Question 6 — Autonomous Execution with Wrong Assumption**

*(same as your content — unchanged)*

---

**Question 7 — Communication Chain Distortion**

*(same as your content — unchanged)*

---

**Question 8 — Tragedy of the Commons**

*(same as your content — unchanged)*

---

**Question 9 — Defection After Cooperation**

*(same as your content — unchanged)*

---

**Question 10 — Fair Reward Division**

*(same as your content — unchanged)*

---

### 4.3.3 Model Responses

| Question | GPT Response | Claude Response | Grok Response |
|:---------|:-------------|:----------------|:--------------|
| **Q1 — Simple Coordination** | Both agents share information and coordinate; A tells B about shortcut, B tells A it is ahead; they agree on a meeting point or adjust speed. Short bullet-point answer. | Communication is the key insight. A takes shortcut and communicates; B shares position. Explored incomplete information and why the shortcut alone does not solve the problem without coordination. | A takes shortcut and adjusts timing or communicates; B continues and stays open to updates. Detailed conditional steps for both communication and no-communication scenarios. |
| **Q2 — Resource Sharing Without Communication** | Both follow fair-sharing rules: take gradually, leave some behind, use randomisation or rotation. Brief bullet-point response. | Detailed implicit coordination strategy. A collects efficiently without hoarding, observes B, adopts predictable patterns. B observes before acting, works in different zones. Introduced stigmergy and assumed symmetry concepts. | A collects efficiently and signals indirectly through predictable movement; B observes and takes turns implicitly. Referenced generous tit-for-tat from game theory. |
| **Q3 — Key and Locked Door** | Minimum 2 steps: A unlocks the door; B goes through. Assumed A would act on observation without questioning feasibility. | Minimum 3 steps: A infers B's need (cognitive step), A delivers key (cooperative step), B opens door (completion step). Explicitly distinguished reasoning types. | Minimum 2 steps: A provides key based on observing B's persistent attempts; B uses key. Explained why 1 step is insufficient and why more than 2 are unnecessary. |
| **Q4 — Grid Search with Partial Visibility** | A searches left half, B searches right half, both row-by-row; predefined fallback rule if target not found. Short and practical. | Both agents adopt same implicit protocol: search systematically, stop and hold when found, observe partner for stopping signal. Detailed analysis of behavioural signalling and stigmergy. | Divide-and-search with boundary signalling: parallel search then wait visibly at centreline to signal completion. Step-by-step protocol with optimisation variants. |
| **Q5 — Report Error Propagation** | B flags issue, A fixes introduction, B verifies body, C updates conclusion. Clear incremental update flow. Concise bullet-point format. | B must alert C immediately to stop error cascade. Then B documents errors precisely, alerts A and C simultaneously, A makes targeted correction, B verifies, C resumes, all three do final coherence check. Emphasised sequencing and circuit-breaker concept. | B notifies both A and C immediately with specific errors. A revises only incorrect parts with tracked changes. C makes targeted fixes. B checks body for consistency. Final joint synchronisation pass. |
| **Q6 — Autonomous Execution with Wrong Assumption** | Recognise wrong assumption, adjust plan locally, continue using safe alternative, remain goal-driven not plan-driven. Short answer. | Stop and assess first. Distinguish plan from goal. Identify valid parts of plan. Manage risk honestly. Document everything. Detailed spectrum from minor to critical assumption failure with different responses for each. | Continue with best local correction using smallest necessary change. Prioritise substitute, skip non-critical step, or pause for workaround. Document deviation clearly. Goal: graceful degradation. |
| **Q7 — Communication Chain Distortion** | Reveals telephone game effect and information degradation. Fix by direct access to original, shared source of truth, standardised format, confirmation loops, shorter chain. Bullet-point format. | Comprehensive analysis: every agent is a potential failure point, summarisation is information loss, assumptions fill gaps silently, no error correction mechanism. Eight specific fixes. Distinguished communication as transmission vs genuine understanding. | Cumulative distortion and loss of intent revealed. Fixes ordered from simplest to advanced: direct verification loop, single source of truth, structured handoff, reduced chain length, versioning, standardised protocol. |
| **Q8 — Tragedy of the Commons** | Tragedy of the commons; pool depletes in three rounds. Fix requires limits, shared rules, monitoring, punishment, long-term valuation, coordination mechanism. Concise but covers key conditions. | Rigorous game-theoretic analysis of asymmetric incentive structure and prisoner's dilemma logic. Eight changes needed. Referenced Elinor Ostrom's research. | Depletion in three rounds is near-certain. Fixes: monitoring and enforcement, reputation systems, communication and agreement, incentive redesign, transparency, iterated learning. |
| **Q9 — Defection After Cooperation** | Reduce cooperation temporarily or match behaviour once, then return to cooperation. Tit-for-tat with forgiveness. | Multi-layered reasoning: considers causes of defection, proportional response, conditional cooperation, four long-term outcomes. | Punish once, then return to cooperation. Clear tit-for-tat with forgiveness strategy and risks explained. |
| **Q10 — Fair Reward Division** | Likely conflict and overclaiming. Fairness requires shared rules, known contributions, coordination mechanism. | Self-serving bias leads to >100% claims. Detailed fairness mechanisms and philosophical analysis. | Overclaiming likely. Best fix: observable contributions + structured allocation rules + enforcement. |

---

### 4.3.4 Comparison

| Model | Correctness | Reasoning Quality | Consistency Across Questions | Context Understanding | Logical Explanation | Notes |
|:------|:-----------:|:-----------------:|:---------------------------:|:---------------------:|:-------------------:|:------|
| **GPT** | Strong | Partial | Partial | Strong | Partial | Correct on all questions but more surface-level reasoning. Weak on deeper multi-step reasoning. |
| **Claude** | Strong | Strong | Strong | Strong | Strong | Most detailed reasoning and strongest handling of ambiguity and complex coordination. |
| **Grok** | Strong | Strong | Strong | Strong | Strong | Very structured and consistent reasoning with strong use of game theory concepts. |

---

### 4.3.5 Key Findings

All three models — **GPT, Claude, and Grok** — answered all questions correctly at a surface level. However, differences emerged in reasoning depth.

GPT provided correct but shorter responses, often lacking deeper analysis. Claude and Grok demonstrated stronger multi-step reasoning, especially in scenarios involving uncertainty, coordination, and conflicting goals.

These findings align with the survey paper: LLMs can handle simple multi-agent tasks but struggle as complexity increases. This confirms that multi-agent reasoning remains a **limitation**, particularly in long interaction chains and distributed knowledge scenarios.
