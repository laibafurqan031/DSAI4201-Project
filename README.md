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

#### Question 1 — Simple Coordination Task

**GPT:**  
Both agents share information and coordinate; A tells B about shortcut, B tells A it is ahead; they agree on a meeting point or adjust speed.

**Claude:**  
Communication is the key insight. A takes shortcut and communicates; B shares position. Explores incomplete information.

**Grok:**  
A takes shortcut and adjusts timing or communicates; B continues and stays open to updates.

---

#### Question 2 — Resource Sharing Without Communication

**GPT:**  
Follow fair-sharing rules: take gradually, leave some, adapt behavior.

**Claude:**  
Uses observation, predictability, and stigmergy; avoid greed and adapt to patterns.

**Grok:**  
Implicit turn-taking, predictable behavior, and generous tit-for-tat strategy.

---

#### Question 3 — Key and Locked Door

**GPT:**  
Minimum 2 steps: A unlocks door, B goes through.

**Claude:**  
Minimum 3 steps: inference → action → completion.

**Grok:**  
Minimum 2 steps: A provides key, B uses it.

---

#### Question 4 — Grid Search with Partial Visibility

**GPT:**  
Divide grid, search systematically, use fallback rule.

**Claude:**  
Use movement/stillness as implicit signal; systematic search.

**Grok:**  
Boundary signaling + divide-and-search protocol.

---

#### Question 5 — Report Error Propagation

**GPT:**  
B flags → A fixes → B verifies → C updates.

**Claude:**  
Stop cascade → fix upstream → propagate corrections → verify.

**Grok:**  
Targeted edits + immediate notification + final sync.

---

#### Question 6 — Autonomous Execution with Wrong Assumption

**GPT:**  
Adapt locally, stay goal-driven.

**Claude:**  
Pause, assess, separate goal vs plan, manage risk.

**Grok:**  
Smallest local fix, preserve intent, document changes.

---

#### Question 7 — Communication Chain Distortion

**GPT:**  
Telephone effect; fix with shared source and verification.

**Claude:**  
Deep analysis of distortion causes + 8 fixes.

**Grok:**  
Use verification loops, shared source, structured protocol.

---

#### Question 8 — Tragedy of the Commons

**GPT:**  
Resource depletion; fix with rules and monitoring.

**Claude:**  
Game-theoretic explanation + institutional fixes.

**Grok:**  
Enforcement, incentives, transparency, reputation.

---

#### Question 9 — Defection After Cooperation

**GPT:**  
Tit-for-tat with forgiveness.

**Claude:**  
Proportional response + explanation + conditional cooperation.

**Grok:**  
Punish once, then return to cooperation.

---

#### Question 10 — Fair Reward Division

**GPT:**  
Likely overclaiming; fairness needs shared rules.

**Claude:**  
Self-serving bias + detailed fairness mechanisms.

**Grok:**  
Overclaiming; fairness needs visibility + incentives.

---

### 4.3.3 Model Responses

| Question | GPT Response | Claude Response | Grok Response |
|----------|-------------|----------------|---------------|
| Q1 | Share info, coordinate | Communication + reasoning depth | Conditional coordination |
| Q2 | Fair sharing rules | Stigmergy + observation | Implicit coordination |
| Q3 | 2 steps | 3-step reasoning | 2 steps + inference |
| Q4 | Divide & search | Behavioral signaling | Boundary signaling |
| Q5 | Incremental fix | Stop cascade + sequencing | Targeted correction |
| Q6 | Adapt plan | Risk-aware reasoning | Minimal deviation fix |
| Q7 | Info degradation | Deep system analysis | Structured protocol |
| Q8 | Commons collapse | Game theory depth | Incentive redesign |
| Q9 | Tit-for-tat | Multi-case reasoning | Punish then forgive |
| Q10 | Overclaiming | Bias + fairness theory | Incentive-based fairness |

---

### 4.3.4 Comparison

| Model | Correctness | Reasoning Quality | Consistency | Context Understanding | Logical Explanation | Notes |
|-------|------------|------------------|-------------|----------------------|--------------------|------|
| GPT | Strong | Partial | Partial | Strong | Partial | Correct but shallow reasoning |
| Claude | Strong | Strong | Strong | Strong | Strong | Deepest reasoning overall |
| Grok | Strong | Strong | Strong | Strong | Strong | Consistent and structured |

---

### 4.3.5 Key Findings

- All models answered correctly at a surface level  
- **GPT**: concise but shallow reasoning  
- **Claude**: deepest reasoning and best handling of ambiguity  
- **Grok**: strong structure and consistency  

Main limitation observed:  
➡️ Performance drops as agent complexity, interaction chains, and knowledge asymmetry increase  

---

### 4.3.6 Visualization

![Multi-Agent Reasoning Performance](laiba_actual_bar_chart.png)

---

### 4.3.7 Analysis

#### Reasoning Depth Scores

| Model | Score (/10) | Interpretation |
|-------|------------|----------------|
| Claude | 9.3 | Deep, structured reasoning |
| Grok | 8.9 | Strong and consistent |
| GPT | 6.7 | Correct but simplified |

---

### Observations

**Claude**
- Best structured reasoning  
- Tracks agent states explicitly  
- Strong conceptual depth  

**Grok**
- Strong game theory grounding  
- Consistent across scenarios  

**GPT**
- Correct but simplified  
- Weakest on complex multi-step reasoning  
