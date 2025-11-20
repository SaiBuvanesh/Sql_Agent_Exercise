## Agentic SQL Analyst — Powered by Gemini 2.5 Flash

This repository contains the Jupyter Notebook **`SQL_Agent_Demo.ipynb`** 

This Exercise project showcases **Agentic AI** — autonomous systems that can *Sense → Reason → Act* — by building a natural-language interface within jupyter notebookfor a SQL database.

---

## 🌟 Project Goal: From Language to Action

The primary goal is to prove that an **LLM can function as a Reasoning Engine (“The Brain”)**, using **tool adapters (“The Hands”)** to generate and execute real SQL queries.

| Feature       | Technical Component       | Agentic Module              |
|---------------|---------------------------|-----------------------------|
| Brain         | Gemini 2.5 Flash          | Reasoning & Planning        |
| Tool          | LangChain SQL Toolkit     | Action / Execution          |
| Environment   | SQLite Database           | Perception                  |
| Flow          | ReAct-Style Loop          | Autonomy & Self-Correction  |

---

##  Getting Started

### Prerequisites

- Python **3.10+**
- Jupyter Notebook or VS Code (with Notebook support)
- Gemini API Key (Free) → https://aistudio.google.com/

---

## 📦 Installation

Install all required libraries:

```bash
pip install -U langchain langchain-community langchain-openai sqlalchemy ipywidgets python-dotenv
```
Setup Instructions

Open the Notebook : SQL_Agent_Demo.ipynb
Insert Your API Key

In the setup cell, replace:
```bash

os.environ["GOOGLE_API_KEY"] = "YOUR_GOOGLE_API_KEY_HERE"

```
with your actual Gemini API key.

### Cells 1–3 initialize the entire agent:

- Cell 1	Initializes Gemini LLM (The Brain)
- Cell 2	Creates fresh company_data.db dummy database (Perception)
- Cell 3	Builds the SQL Agent Executor + Tools (The Hands)
- Cell 4  Start Chatting 

When you see:

- GEMINI AGENT READY!

You’re ready to interact with the SQL Agent.

💬 Demo Commands to Try
1. Perception (Schema Inspection)
🧑 You: list the columns in the employees table

2. Reasoning + SQL Execution
🧑 You: name of the employee who earns the maximum salary

- (Expected: Eve)

3. Aggregation Query
🧑 You: what is the total salary expense of the Engineering department?

In the notebook, you can see this clearly inside the **Agent Thinking Log**, which captures the verbose output printed by LangChain’s SQL agent.  
If the agent hits a syntax issue or refers to a non-existent column, the log will show:

- ❌ The failed SQL  
- 🔍 The database error message  
- 🔄 The agent’s revised query  
- ✅ The final correct answer

This feedback loop is what makes the system *agentic* rather than just predictive — it doesn’t stop at generating an answer, it **evaluates, adjusts, and retries**, much like a real analyst would.

### 📌 *When Data and Code Learn to Think: The Rise of Agentic Intelligence*  
[Read the full blog post](https://medium.com/@arsaibuvanesh/when-data-and-code-learn-to-think-the-rise-of-agentic-intelligence-0ff1db905387?postPublishedType=repub)
