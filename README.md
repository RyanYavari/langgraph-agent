# langgraph-research-agent

A multi-agent research assistant that autonomously plans, searches, and synthesizes answers from the web using LangGraph.

[![Python](https://img.shields.io/badge/Python-3.11-blue)](https://python.org)
[![LangGraph](https://img.shields.io/badge/LangGraph-latest-green)](https://langchain-ai.github.io/langgraph/)
[![LangSmith](https://img.shields.io/badge/LangSmith-tracing-orange)](https://smith.langchain.com/)

---

## Overview

This system uses a graph of specialized agents to handle complex research queries end-to-end. Given a question, the system plans a research strategy, retrieves information via MCP-connected tools, and synthesizes a cited answer with full observability via LangSmith tracing and quality measured by RAGAS evals.

## Architecture

| Agent | Role |
|---|---|
| Planner | Decomposes the user query into sub-tasks |
| Researcher | Executes searches via MCP tool integrations |
| Synthesizer | Combines retrieved context into a final cited answer |

## Tech Stack

- **Orchestration:** LangGraph
- **Observability:** LangSmith
- **Tool Integration:** MCP servers
- **Evaluation:** RAGAS

## Key Features

- Multi-agent graph with clearly defined roles and handoffs
- Human-in-the-loop approval gates at critical decision points
- End-to-end LangSmith tracing for full run observability
- RAGAS evaluation suite measuring answer faithfulness and relevance

## Setup
```bash
git clone https://github.com/RyanYavari/langgraph-research-agent
cd langgraph-research-agent
pip install -r requirements.txt
cp .env.example .env
```

## Author

Ryan Yavari · [LinkedIn](https://www.linkedin.com/in/ryan-yavari/) · [GitHub](https://github.com/RyanYavari)
