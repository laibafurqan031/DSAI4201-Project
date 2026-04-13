# DSAI4201-Project
# DSAI4201 Project — Multi-Domain LLM Reasoning Analysis

## Team Members
- **Aneeha Sohail (60105845)** — Theory of Mind  
- **Thaminah Fathima (60106660)** — Social Norms & Moral Reasoning  
- **Laiba Furqan (60301575)** — Multi-Agent Systems  

---

## Project Overview

This project evaluates the reasoning capabilities of Large Language Models (LLMs) across three key domains identified in the survey paper:

- **Theory of Mind (ToM)**
- **Social Norms & Moral Reasoning**
- **Multi-Agent Systems**

Each domain represents a **known limitation** of LLMs, where models appear correct at a surface level but struggle with deeper reasoning, consistency, and complex interactions.

We tested multiple models:
- GPT
- Claude
- Grok
- DeepSeek (for Social Norms section)

---

## Key Objective

To analyze whether LLMs:
- Perform **true reasoning**  
- Or rely on **pattern matching and learned responses**

---

## Project Structure & Branches

Each section of the project was developed separately in dedicated branches:

| Branch Name | Section | Author |
|------------|--------|--------|
| `theory-of-mind` | 4.1 Theory of Mind | Aneeha |
| `social-norms` | 4.2 Social Norms & Moral Reasoning | Thaminah |
| `multi-agent` | 4.3 Multi-Agent Systems | Laiba |
| `main` | Final integrated report | All |

Each branch contains:
- Questions
- Model responses
- Comparisons
- Analysis

---

## Section Summaries

---

### 4.1 Theory of Mind (Aneeha)

**Focus:**  
Understanding beliefs, intentions, and hidden mental states.

**Findings:**
- All models answered correctly at surface level  
- **Claude** showed deepest reasoning (especially recursive beliefs & emotions)  
- **GPT** was correct but shallow  
- **Grok** was structured but slightly less nuanced than Claude  

**Key Insight:**  
LLMs can simulate Theory of Mind but lack consistent deep understanding, especially in:
- Recursive belief tracking  
- Emotional reasoning  
- Hidden implications  

---

### 4.2 Social Norms & Moral Reasoning (Thaminah)

**Focus:**  
Evaluating politeness, ethics, fairness, and cultural behavior.

**Findings:**
- All models gave **socially acceptable answers**
- Major differences in **depth and consistency**

| Model | Performance |
|------|------------|
| Claude | Most human-like, nuanced reasoning |
| DeepSeek | Logical and consistent but blunt |
| GPT | Safe but shallow |
| Grok | Short, rule-based, least consistent |

**Key Insight:**  
LLMs:
- Handle simple moral judgments well  
- Struggle with:
  - Conflicting values (e.g., honesty vs kindness)  
  - Cultural nuance  
  - Long-term consequences  

Moral reasoning is largely **pattern-based, not principled**

---

### 4.3 Multi-Agent Systems (Laiba)

**Focus:**  
Coordination between multiple agents with different goals and knowledge.

**Findings:**
- All models solved basic scenarios correctly  
- Performance diverged with complexity  

| Model | Performance |
|------|------------|
| Claude | Best at tracking agents, deep reasoning |
| Grok | Strong structure, consistent |
| GPT | Correct but surface-level |

**Key Challenges Identified:**
- Long-horizon planning  
- Communication failures  
- Coordination under uncertainty  

**Key Insight:**  
LLMs struggle with:
- Tracking multiple agents simultaneously  
- Handling conflicting knowledge  
- Maintaining reasoning across multiple steps  

---

## Overall Comparison

| Model | Strengths | Weaknesses |
|------|----------|-----------|
| **Claude** | Deep reasoning, consistency, nuance | Slightly verbose |
| **GPT** | Correct answers, clarity | Shallow reasoning depth |
| **Grok** | Structured, logical | Less nuanced |
| **DeepSeek** | Consistent, analytical | Lacks emotional/social nuance |

---

## Final Conclusions

Across all three domains:

### What LLMs do well:
- Produce **correct and socially acceptable answers**
- Handle **simple reasoning tasks**
- Recognize patterns and common scenarios

### Key Limitations:
- **Shallow reasoning depth**
- **Inconsistent responses across prompts**
- Difficulty with:
  - Multi-step reasoning  
  - Conflicting goals  
  - Hidden beliefs  
  - Moral trade-offs  

---

## Final Insight

> LLMs **approximate reasoning**, but do not consistently perform **true human-like reasoning**.

They rely heavily on:
- Pattern recognition  
- Learned responses  
- Context similarity  

Rather than:
- Stable internal reasoning models  
- Deep understanding of agents, beliefs, and ethics  

---

## Note

All sections were developed independently and later integrated into this final report.  
Refer to individual branches for detailed breakdowns and experiments.

---
