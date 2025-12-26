# GenAI – Business Memo Emailing Crew

This project implements a **multi-agent Generative AI system** for producing professional business memos.
The system follows a structured workflow:

**Analyst Agent → Drafting Agent → Approval Agent**

It was developed as an academic project and focuses on clarity, reproducibility, and evaluation.

---

## Project Objective
- Automate the creation of business memos using LLM-based agents
- Improve quality through an approval and revision step
- Log evaluations and feedback for analysis
- Provide a simple interface using Streamlit

---

## Key Features
- Multi-agent architecture (Analyst, Drafting, Approval)
- LLM integration via `llm_client.py`
- Streamlit web interface
- Evaluation and feedback logging (CSV / SQLite)
- Example dataset for memo generation

---

## Project Structure
- `business_memo_system.py` – main pipeline (CLI)
- `streamlit_app.py` – Streamlit user interface
- `analyst_agent.py` – analysis agent
- `drafting_agent.py` – memo drafting agent
- `approval_agent.py` – validation and approval agent
- `llm_client.py` – interface to the language model
- `models.py` – shared data models
- `database.py` – database utilities
- `business_memo_cases.csv` – example input cases

---

## Architecture Overview
