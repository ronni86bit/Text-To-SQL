# AskSQL – AI-Powered Natural Language to SQL Analytics Platform

AskSQL is an AI-powered analytics platform that allows users to query databases using plain English instead of writing SQL manually.

It converts natural language questions into executable SQL queries using Large Language Models (LLMs), retrieves real-time database results, and presents them through an intuitive interactive interface.

Example:

**User Input:**
*"Show me the top 5 customers with the highest total purchases last month."*

**Generated SQL:**

```sql
SELECT customer_name, SUM(total_purchase) AS total
FROM sales
WHERE purchase_date >= DATE_SUB(CURDATE(), INTERVAL 1 MONTH)
GROUP BY customer_name
ORDER BY total DESC
LIMIT 5;
```

---

## Features

* Natural Language → SQL query generation
* Real-time SQL execution on connected databases
* Schema-aware query generation for improved accuracy
* AI-powered analytics assistant for non-technical users
* Interactive web interface for querying and result visualization
* Query validation and safety guardrails
* Fast response generation using LLM APIs

---

## Tech Stack

**Backend:**
Python, FastAPI

**AI / LLM:**
OpenAI GPT-4 / LLM APIs, Prompt Engineering

**Database:**
MySQL / PostgreSQL / SQLite

**Frontend:**
Streamlit

**Tools:**
Git, GitHub, Virtual Environment

---

## Architecture

```text
User Query
   ↓
Natural Language Processing
   ↓
Database Schema Retrieval
   ↓
LLM Prompt Construction
   ↓
SQL Query Generation
   ↓
Query Validation
   ↓
Database Execution
   ↓
Results Display
```

---

## Project Workflow

1. User enters a question in plain English.
2. System retrieves relevant database schema metadata.
3. LLM generates context-aware SQL query.
4. Query validation ensures safe execution.
5. SQL executes against the database.
6. Results are returned in real time through the UI.

---

## Use Cases

* Business analytics dashboards
* Natural language database querying
* AI-powered reporting tools
* SQL automation for non-technical users
* Data exploration and insight generation

---

## Installation

### Clone the repository

```bash
git clone https://github.com/yourusername/AskSQL.git
cd AskSQL
```

### Create virtual environment

```bash
python -m venv venv
```

Activate environment:

**Windows**

```bash
venv\Scripts\activate
```

**Mac/Linux**

```bash
source venv/bin/activate
```

### Install dependencies

```bash
pip install -r requirements.txt
```

### Configure environment variables

Create a `.env` file:

```env
OPENAI_API_KEY=your_api_key
DB_HOST=localhost
DB_USER=root
DB_PASSWORD=your_password
DB_NAME=database_name
```

### Run the application

```bash
streamlit run app.py
```

---

## Future Improvements

* Multi-database support
* Query explanation mode
* SQL optimization suggestions
* Role-based access control
* Query history and chat memory
* Dashboard/chart generation
* Local LLM support (Ollama / Llama)

---

## Resume Highlights

This project demonstrates:

* LLM application engineering
* Prompt engineering
* Natural language processing
* Backend API development
* Database integration
* AI-assisted analytics
* Production-oriented system design

---

## Author

**Rohith Cherukuri**
AI / ML Engineer | Python Developer 
