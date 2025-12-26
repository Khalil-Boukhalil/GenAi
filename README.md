# GenAI – Business Memo Emailing Crew

## Overview
This project implements a **multi-agent Generative AI system** designed to automatically produce **professional business memos**. Instead of relying on a single prompt, the system uses a **structured multi-agent workflow** to improve output quality and consistency.

The workflow is composed of three agents:

**Analyst Agent → Drafting Agent → Approval Agent**

This project was developed as an **academic project** with an emphasis on clarity, reproducibility, evaluation, and software structure.

---

## Project Goal
The main goal of this project is to **automate the creation of business memos** using Large Language Models (LLMs) while maintaining a clear structure and quality control.

The project aims to:
- Demonstrate how **multi-agent architectures** can improve text generation quality  
- Separate reasoning, drafting, and validation into independent agents  
- Log evaluations and feedback for later analysis  
- Provide both a **command-line interface** and a **web interface** for interaction  

---

## System Architecture
The system follows a sequential pipeline:

```
User Input / Case
        |
        v
   Analyst Agent
 (understands intent,
  constraints, tone)
        |
        v
  Drafting Agent
 (generates memo draft)
        |
        v
  Approval Agent
 (reviews, validates,
  or requests revision)
        |
        +--> Evaluation & Feedback Logs
```

Each agent has a specific role, making the system easier to understand, debug, and extend.

---

## Key Features
- **Multi-agent architecture** (Analyst, Drafting, Approval)
- **LLM integration** through a dedicated client (`llm_client.py`)
- **Streamlit web interface** for interactive usage
- **Evaluation and feedback logging** using CSV and SQLite
- **Example dataset** for memo generation and testing
- Clear separation between logic, data models, and logging

---

## Project Structure
- `business_memo_system.py` – main orchestration pipeline (CLI)
- `streamlit_app.py` – Streamlit web interface
- `analyst_agent.py` – analyzes user intent and constraints
- `drafting_agent.py` – generates memo drafts
- `approval_agent.py` – validates and approves drafts
- `llm_client.py` – interface to the language model
- `models.py` – shared data models
- `database.py` – database utilities
- `analyze_evaluation.py` – evaluation analysis script
- `business_memo_cases.csv` – example input cases

---

## Installation

### 1) Create a virtual environment
```bash
python -m venv .venv
```

Activate it:

**Windows (Git Bash)**
```bash
source .venv/Scripts/activate
```

**Linux / macOS**
```bash
source .venv/bin/activate
```

---

### 2) Install dependencies
```bash
pip install -r requirements.txt
```

---

## Running the Project

### Option 1 — Command Line Interface
```bash
python business_memo_system.py
```

This runs the complete pipeline, generates a business memo, and logs evaluation and feedback data.

---

### Option 2 — Streamlit Web Interface
```bash
streamlit run streamlit_app.py
```

This provides an interactive web interface for generating and reviewing memos.

---

## Evaluation
- Evaluation results and feedback are logged during execution  
- Logs are stored in CSV files or SQLite databases  
- `analyze_evaluation.py` can be used to analyze generated outputs  
- This supports qualitative analysis of memo quality and revisions  

---

## Limitations
- Output quality depends on the underlying language model  
- No automatic factual verification is performed  
- Evaluation metrics are basic and intended for experimentation  

---

## Reproducibility & Submission Notes
- Generated artifacts (logs, databases, cache files) are excluded from version control  
- The repository is designed to be easy to clone and run by evaluators  
- This repository represents the **final submission version** of the project  

---

## License
MIT
