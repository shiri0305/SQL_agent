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