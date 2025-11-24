# AI-ML-Assignment-6-Prompt-Engineering

**Name:** Alex Torres  
**Task:** Structured Data Extraction from a product review into JSON  
**LLM Used:** OpenAI `gpt-4.1-mini` (via Python API)

---

## Experiment Overview

I used a single constant input (a customer review of a Logitech mouse) and tried
five prompts:

1. Baseline Prompt (no techniques)
2. Technique 1 – Role Prompting
3. Technique 2 – Output Formatting & Schema Constraints
4. Technique 3 – Chain-of-Thought Style Instructions
5. Final Optimized Prompt (combining the best elements)

---

## Summary Table

| Prompt Name                    | Accuracy (1–10) | Observation                                  |
|--------------------------------|-----------------|----------------------------------------------|
| baseline                       | 5               | Correct fields, but JSON format inconsistent (code block + wrong price and rating format).   |
| technique_1_role_prompting     | 7               | Cleaner JSON and better accuracy, but price and rating formats still incorrect.  |
| technique_2_output_formatting  | 9               | Accurate JSON with correct formatting; nearly perfect.      |
| technique_3_chain_of_thought   | 8               | Good reasoning, but extraneous text and minor field inaccuracies (“TechWorld downtown”, numeric price).  |
| final_optimized_prompt         | 10              | Accurate, clean JSON with full format adherence and no noise.      |

*(Replace scores and notes with your real results.)*

---

## Key Lesson Learned

Prompt engineering has a **huge impact** on LLM performance.  
Simply adding:
- a **role** (“Senior Data Analyst”),  
- a strict **output schema**, and  
- clear **step-by-step instructions**  

turned a vague, low-quality response into a **consistent and reliable JSON extractor**. The LLM is much more accurate when the prompt reduces ambiguity and clearly defines both the task and the expected format.
