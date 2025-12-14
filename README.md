# LangGraph-Based Intelligent SQL Agent
LangGraph-orchestrated intelligent SQL agent that converts natural language questions into executable SQL queries, executes them on a relational database, and returns structured results via a FastAPI backend.
This is a stateful SQL Agent that:
- Accepts natural language questions
- Translates them into SQL
- Executes queries on a real database
- Handles errors and retries using LangGraph control flow
- Exposes the agent via a FastAPI REST API
## High level Flow 
![Alt text](flow.png)
## Why LangGraph?
Because:
* You need state
* You need conditional routing
* You may need retry loops
* You want deterministic control over agent behavior
## Tech Stack 

| Syntax      | Description |
| ----------- | ----------- |
|Layer	|Technology|
|Language	|Python 3.10+|
|Agent Framework	|LangGraph|
|LLM	|OpenAI / Azure OpenAI (configurable)|
|Database	|SQLite (start simple)|
|Backend API	|FastAPI|
|ORM / SQL	|SQLAlchemy|
|Environment	|.env|

## Repository Structure
```plaintext
langgraph-sql-agent/langgraph-sql-agent/
│
├── app/
│   ├── main.py              # FastAPI entry
│   ├── agent/
│   │   ├── graph.py         # LangGraph definition
│   │   ├── state.py         # Graph state schema
│   │   ├── nodes.py         # Agent nodes
│   │   └── tools.py         # SQL execution tools
│   │
│   ├── db/
│   │   ├── models.py        # SQLAlchemy models
│   │   ├── init_db.py       # Sample data
│   │   └── session.py
│   │
│   └── config.py
│
├── tests/
├── README.md
├── requirements.txt
└── .env.example
```
