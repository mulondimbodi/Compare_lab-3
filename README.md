# CMPG 313 – Lab 3: AI The Past and the Present

## Overview
This project compares **rule-based AI (ELIZA)** with **modern generative AI (LLM)** side-by-side using a Python GUI.

## Files
| File | Description |
|------|-------------|
| `eliza.py` | Custom rule-based ELIZA chatbot (10+ rules, no NLTK dependency) |
| `LLM.py` | Modern LLM chatbot using Qwen2.5-1.5B-Instruct via HuggingFace |
| `chat_comparison.py` | Side-by-side Tkinter GUI comparing both systems |

## Setup

### 1. Install dependencies
```bash
pip install transformers torch
```

### 2. Run ELIZA only
```bash
python eliza.py
```

### 3. Run LLM only
```bash
python LLM.py
```
> Note: First run will download the Qwen2.5-1.5B model (~1 GB).

### 4. Run the comparison GUI
```bash
python chat_comparison.py
```

## ELIZA Rules Modified (Part 1)
The custom `eliza.py` includes 10 rules:
1. **Greetings** – Hello, hi, hey
2. **Name introduction** – "My name is …"
3. **Feeling statements** – "I feel …" / "I am feeling …"
4. **Stress/anxiety** – Detects stressed, anxious, overwhelmed
5. **Tiredness/sleep** – Detects tired, exhausted, need sleep
6. **Family references** – Mother, father, parents
7. **"I need …"** – Reflects needs back as questions
8. **"Because …"** – Challenges reasoning
9. **"I am …"** – Identity statements
10. **Goodbye** – Quit/bye detection
11. **Fallback** – Generic Socratic responses

## Test Prompts Used
- Hello
- My name is Mulondi
- I feel stressed
- I am tired
- Because I have exams
- My mother is strict
- I need more sleep
- quit

## Key Observations
| Aspect | ELIZA | LLM |
|--------|-------|-----|
| Technique | Pattern matching (regex) | Neural text generation |
| Context awareness | None – each reply is independent | Partial – follows topic |
| Naturalness | Formulaic, repetitive | Fluent, varied |
| Explainability | Fully transparent (readable rules) | Black-box |
| Speed | Instant | Seconds (inference) |
| Failure mode | Falls back to generic response | May hallucinate or drift |

## Screenshots
Screenshots of ELIZA, LLM and comparison GUI conversations are included in this repository.

## Author
Module: CMPG 313  
Institution: North-West University