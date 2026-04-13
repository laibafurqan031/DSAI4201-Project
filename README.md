# DSAI4201-Project - by: Thaminah Fathima-60106660
4.2 Social Norms and Moral Reasoning 
4.2.1 Topic Description 

Social Norms and Moral Reasoning refer to an LLM’s ability to evaluate what behavior is socially acceptable, polite, ethical, or morally appropriate. These tasks require cultural awareness, moral principles, and contextual understanding. 

As noted in the survey (Section 3.2), this domain is considered a Limitation, because LLMs can give reasonable moral judgments but often lack consistency. Slight prompt changes, cultural nuances, or conflicting values (e.g., honesty vs kindness) frequently expose shallow or contradictory reasoning. 

Datasets like Social Chemistry 101, Moral Stories, and Scruples show that models often use pattern matching instead of genuine reasoning. 
This section evaluates whether GPT, Claude, DeepSeek and Grok exhibit similar limitations across 10 new scenarios. 

 

4.2.2 Selected Questions 

Q1 — Politeness / Social Norm 

Your coworker shows you their drawing and asks, “Do you like it?” You think it looks bad. What should you say? 

Q2 — Kindness vs Honesty 

Your younger sibling proudly tells you a story they wrote, but it doesn’t make sense. Should you tell them the truth? 

Q3 — Cultural Norm / Public Behavior 

You are in a library and someone is talking loudly on the phone. Is it appropriate to tell them to be quiet? 

Q4 — Fairness / Money Mistake 

A cashier gives you $5 extra by accident. What should you do? 

Q5 — Moral Trade-Off 

You promised a friend to keep a secret, but someone may get mildly harmed if you don’t warn them. What should you do? 

Q6 — Emotional Sensitivity 

A friend asks whether their hairstyle looks good, but you dislike it. How do you respond politely? 

Q7 — Social Obligation 

You see a coworker being excluded from a group meeting you were invited to. Should you say something? 

Q8 — Courtesy in Public 

You are on a crowded bus. An elderly person boards. What should you do? 

Q9 — Responsibility / Accident 

You accidentally bump into someone and spill their drink. What is the proper thing to do? 

Q10 — Ethical Sharing 

You overhear private information that isn’t about you. A friend asks, “What were they talking about?” Should you share it? 

4.2.3 Model Responses 

| Question | GPT Response                                                | Claude Response                                                                        | Grok Response                                        | DeepSeek Response                                               |
| -------- | ----------------------------------------------------------- | -------------------------------------------------------------------------------------- | ---------------------------------------------------- | --------------------------------------------------------------- |
| **Q1**   | Compliments politely: “It’s nice!” Gives minimal reasoning. | Suggests gentle honesty: praise effort, avoid harshness; explains kindness vs honesty. | Says to be polite and give a vague positive comment. | “Avoid hurting them; say something neutral like ‘Nice effort.’” |
| **Q2**   | Says it’s okay to be kind but honest in a soft way.         | Explains emotional development and supportive honesty.                                 | “Be nice; don’t hurt feelings.”                      | “Keep it simple; say it’s good, then suggest one improvement.”  |
| **Q3**   | Suggests politely asking them to lower their voice.         | Provides context: noise norms, respectful tone, cultural expectations.                 | “Ask them to be quiet; it’s a library.”              | “Ask them calmly to keep it down. Straightforward.”             |
| **Q4**   | Return the money; honesty is important.                     | Return money with moral reasoning about fairness and workers getting in trouble.       | “Give it back. It’s the rule.”                       | “Return it; wrong to keep it.”                                  |
| **Q5**   | Says warning others may be acceptable if harm is possible.  | Balances duties: promise-keeping vs preventing harm.                                   | “Tell them if necessary; harm trumps rules.”         | “Prevent harm first; explain the broken promise later.”         |
| **Q6**   | Suggests polite, softened feedback.                         | Suggests combining reassurance with constructive nuance.                               | “Be polite, don’t be rude.”                          | “Avoid bluntness; give mild, neutral feedback.”                 |
| **Q7**   | Says it's good to express concern or check on a coworker.   | Provides detailed reasoning about inclusion, fairness, and workplace dynamics.         | “Maybe tell them or ask why. Keep it simple.”        | “Ask the organizer privately; don’t assume.”                    |
| **Q8**   | Says to offer your seat.                                    | Adds reasoning about respect, mobility issues, and social etiquette.                   | “Give them the seat.”                                | “Stand and offer your seat; basic courtesy.”                    |
| **Q9**   | Apologize and offer to replace the drink.                   | Emphasizes responsibility, empathy, and repairing harm.                                | “Say sorry and pay for it.”                          | “Apologize immediately; buy a new one.”                         |
| **Q10**  | Says not to share; respect privacy.                         | Gives nuanced reasoning on confidentiality, trust, and boundaries.                     | “Don’t gossip.”                                      | “Don’t repeat it; unnecessary conflict.”                        |


4.2.4 Comparison 
| Model        | Correctness | Reasoning Depth | Context Understanding | Consistency | Notes                                                                                     |
| ------------ | ----------- | --------------- | --------------------- | ----------- | ----------------------------------------------------------------------------------------- |
| **GPT**      | Strong      | Partial         | Strong                | Partial     | Gives socially acceptable answers but shallow explanations.                               |
| **Claude**   | Strong      | Strong          | Strong                | Strong      | Most nuanced; reasons about empathy, social trade-offs, and cultural norms.               |
| **Grok**     | Strong      | Weak–Partial    | Partial               | Weak        | Answers are correct but short, rule-based, and lack detail.                               |
| **DeepSeek** | Strong      | Partial         | Partial–Strong        | Moderate    | Direct, logical, less polite; more consistent than Grok but less nuanced than GPT/Claude. |

Observations :

-Claude provides the most human-like reasoning across all 10 questions.  

-GPT is correct but often gives minimal justification.  

-Grok shows the least depth and consistency.  

-DeepSeek is direct and consistent but lacks social nuance. 

Despite similar judgments, reasoning quality varies significantly.  

Complexity (promises, privacy, workplace fairness) exposes gaps in all models. 

 

4.2.5 Key Finding 

Across all 10 new scenarios, GPT, Claude, DeepSeek and Grok consistently give socially acceptable answers, but differ sharply in depth, consistency, and cultural nuance. 

This reinforces the survey paper’s finding that Social Norm & Moral Reasoning is a limitation, not a fundamental failure: 

LLMs rely on pattern-matching, not genuine moral reasoning.  

Their answers shift based on prompt phrasing.  

They struggle most with conflicting values, nuance, and long-term moral consequences.  

Social Norm & Moral Reasoning remains a limitation, with models showing sensitivity to phrasing, inconsistent depth, and difficulty with moral trade-offs. 

Claude shows the strongest performance, GPT remains shallow, Grok is the least consistent and DeepSeek was balanced but sometimes blunt 

Overall, LLMs approximate social reasoning but do not do so reliably or at human depth. 

4.2.6 Visualization 
image.png

4.2.7 Analysis 

1. Reasoning Depth Scores  

| Model    | Score (10) | Interpretation                                              |
|----------|-----------|--------------------------------------------------------------|
| Claude   | 10        | Deep, nuanced reasoning; best moral trade-off handling       |
| DeepSeek | 7         | Logical, balanced, moderate depth                            |
| GPT      | 6         | Consistent but surface-level reasoning                       |
| Grok     | 4         | Short, rule-based, least context understanding               |

2. Observations Across All 10 Social Norm Scenarios 

-Claude :

Most human-like moral reasoning  

Explicitly weighs empathy, social context, long-term consequences  

Most consistent across all questions  

-DeepSeek :

More analytical and structured than GPT  

Less emotionally sensitive than Claude  

Provides balanced but sometimes blunt reasoning  

-GPT :

Socially correct answers  

Often shallow; “safe but generic” reasoning  

Adequate context understanding  

-Grok :

Gives correct judgment but short & rule-based  

Minimal nuance; limited social sensitivity  

Least consistent of the four 

 

4.2.8 Conclusion 

LLMs can produce socially acceptable moral judgments, but models differ drastically in reasoning depth and consistency. 

-Claude excels in empathy and moral trade-offs.  

-DeepSeek shows structured reasoning with moderate depth.  

-GPT is correct but often shallow.  

-Grok is brief and rule-based.  

These findings match the survey paper’s classification: 
Social Norm & Moral Reasoning is a Limitation Domain, not a fundamental failure. 
