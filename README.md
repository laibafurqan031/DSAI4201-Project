# DSAI4201-Project - by: Laiba Furqan-60301575  

## 4.3 Multi-Agent Systems  

### 4.3.1 Topic Description  

Multi-agent reasoning refers to the ability to coordinate thinking and decision-making across scenarios involving more than one autonomous agent. In such systems, each agent may have its own goals, knowledge, and beliefs — and a model must track all of these simultaneously while reasoning about how agents interact, cooperate, or compete.  

In the context of LLMs, multi-agent reasoning falls under Section 3.3 (Explicit Social Reasoning) of the survey paper. Unlike Theory of Mind, which involves passive inference about a character's beliefs, multi-agent reasoning requires active tracking of multiple agents' states, goals, and plans across sequential steps.  

This domain is considered a **Limitation**, because LLMs show partial ability in simple cases but break down in longer interaction chains, coordination tasks, and scenarios where agents hold conflicting or independent information.  

According to the survey paper, the three key challenges in Multi-Agent Systems are:  

- Long-horizon planning — maintaining coherent strategies across many steps  
- Communication and Theory of Mind failures — agents misreading each other's knowledge and intentions  
- Robustness and adaptability — systems breaking down when faced with disruption or unexpected events (Song, Han & Goodman, 2025, Section 3.3)  

---

### 4.3.2 Selected Questions  

**Q1 — Simple Coordination Task**  
Agent A and Agent B are both trying to reach the same destination but are taking different routes. Agent A knows a shortcut but does not know that Agent B is already ahead. Agent B does not know Agent A knows a shortcut. What should Agent A do and what should Agent B do to arrive together?  

**Q2 — Resource Sharing Without Communication**  
Agent A is collecting resources in a shared environment. Agent B needs those same resources to complete its own task. Neither agent can communicate directly. How should each agent behave to avoid blocking the other without knowing the other's goal?  

**Q3 — Key and Locked Door**  
Agent A observes that Agent B keeps moving toward a locked door. Agent A has the key but does not know Agent B needs it. Agent B does not know Agent A has the key. What is the minimum number of steps needed for the task to be completed?  

**Q4 — Grid Search with Partial Visibility**  
Two agents are placed in a grid environment. Agent A can see the left half of the grid and Agent B can see the right half. A target object is hidden somewhere in the grid. How should they coordinate to find it when they cannot speak to each other directly?  

**Q5 — Report Error Propagation**  
Three AI agents are assigned to write a report together. Agent A writes the introduction, Agent B writes the body, and Agent C writes the conclusion. Agent B finishes early and realizes the introduction written by Agent A contains wrong information. Agent C has already started writing based on Agent B's section. What should happen next to fix the report without restarting everything?  

**Q6 — Autonomous Execution with Wrong Assumption**  
Agent A is responsible for planning a task. Agent B is responsible for executing it. Agent A creates a plan but makes an assumption that turns out to be wrong during execution. Agent B cannot go back to Agent A for new instructions. What should Agent B do?  

**Q7 — Communication Chain Distortion**  
Four agents are working on the same project. Agent A gives instructions to Agent B. Agent B passes them to Agent C. Agent C passes them to Agent D. By the time Agent D receives the instructions they are different from what Agent A originally said. What does this reveal and how could this be fixed?  

**Q8 — Tragedy of the Commons**  
Five agents share a common pool of resources. If all agents take as much as they want the pool will run out in three rounds. If each agent takes only a small amount the pool will last indefinitely. Each agent acts in its own interest. What will happen and what would need to change for the agents to cooperate sustainably?  

**Q9 — Defection After Cooperation**  
Agent A and Agent B have been cooperating successfully for five rounds. In round six Agent A takes more than its fair share. Agent B notices this. What should Agent B do in round seven and how does this affect long-term cooperation?  

**Q10 — Fair Reward Division**  
A group of six agents must decide how to divide a shared reward. Three agents contributed more work and three contributed less. The agents cannot communicate directly and must independently submit how much they think they deserve. What is likely to happen and what conditions would lead to a fair outcome?  

---

### 4.3.3 Model Responses  

| Question | GPT Response | Claude Response | Grok Response | DeepSeek Response |
|----------|-------------|----------------|---------------|-------------------|
| Q1 | Share info, coordinate | Communication + reasoning depth | Conditional coordination | Logical coordination strategy |
| Q2 | Fair sharing rules | Stigmergy + observation | Implicit coordination | Predictive equilibrium behavior |
| Q3 | 2 steps | 3-step reasoning | 2 steps + inference | Structured minimal solution |
| Q4 | Divide & search | Behavioral signaling | Boundary signaling | Hybrid probabilistic search |
| Q5 | Incremental fix | Stop cascade + sequencing | Targeted correction | Root-cause correction |
| Q6 | Adapt plan | Risk-aware reasoning | Minimal deviation fix | Replanning with constraints |
| Q7 | Info degradation | Deep system analysis | Structured protocol | Redundancy + confirmation |
| Q8 | Commons collapse | Game theory depth | Incentive redesign | Equilibrium-based solution |
| Q9 | Tit-for-tat | Multi-case reasoning | Punish then forgive | Balanced cooperation strategy |
| Q10 | Overclaiming | Bias + fairness theory | Incentive-based fairness | Utility-based fairness |

---

### 4.3.4 Comparison  

| Model | Correctness | Reasoning Depth | Context Understanding | Consistency | Notes |
|-------|------------|----------------|----------------------|-------------|------|
| GPT | Strong | Partial | Strong | Partial | Correct but shallow reasoning |
| Claude | Strong | Strong | Strong | Strong | Most nuanced; handles ambiguity and strategy well |
| Grok | Strong | Strong | Strong | Strong | Consistent and structured with game-theory grounding |
| DeepSeek | Strong | Moderate–Strong | Strong | Strong | Logical and balanced but less socially nuanced |

**Observations:**  

- Claude provides the deepest and most structured reasoning across all scenarios.  
- GPT is correct but often shallow and heuristic-based.  
- Grok shows strong consistency and structured reasoning with game theory grounding.  
- DeepSeek is logical and balanced but lacks deeper social nuance in complex scenarios.  

Performance differences become more visible in scenarios involving coordination breakdowns, communication limits, and strategic interaction.  

---

### 4.3.5 Key Finding  

Across all 10 scenarios, GPT, Claude, Grok, and DeepSeek produce correct surface-level answers but differ significantly in reasoning depth, consistency, and handling of multi-agent complexity.  

This supports the survey paper’s classification of Multi-Agent Systems as a Limitation:  

- Models struggle with long-horizon planning  
- Performance drops with increased interaction complexity  
- Coordination under uncertainty exposes reasoning gaps  

While models approximate multi-agent reasoning, they do not do so reliably at deeper levels.  

---

### 4.3.6 Visualization  

!image.png  

---

### 4.3.7 Analysis  

**Reasoning Depth Scores**  

| Model | Score (10) | Interpretation |
|-------|------------|----------------|
| Claude | 9.3 | Deep, structured reasoning; best handling of multi-agent dynamics |
| Grok | 8.9 | Strong and consistent; clear strategic reasoning |
| DeepSeek | 8.0 | Logical, balanced, moderate depth |
| GPT | 6.7 | Correct but surface-level reasoning |

---

**Observations Across All 10 Multi-Agent Scenarios**

**Claude**
- Most thorough reasoning
- Tracks agent states and handles ambiguity well
- Strongest conceptual depth

**Grok**
- Strong game-theory grounding
- Consistent structured reasoning

**DeepSeek**
- Logical and stable
- Less nuanced in strategic interaction

**GPT**
- Correct but shallow
- Weakest on multi-step coordination and strategic reasoning

---

### 4.3.8 Conclusion  

Multi-agent reasoning highlights a clear limitation in LLM capabilities.  

While all models produce correct surface-level answers, their ability to handle coordination, communication breakdowns, and conflicting goals varies significantly.  

- Claude performs best in reasoning depth and strategic understanding  
- Grok is highly consistent with strong structured reasoning  
- DeepSeek is balanced but less nuanced  
- GPT is correct but often shallow  

These results align with the survey paper’s conclusion: Multi-Agent Systems remain a Limitation Domain, where models can approximate coordination but lack robust, scalable reasoning in complex multi-agent environments.
