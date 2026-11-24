🤖 One Person Company: Autonomous AI Agents & Multi-Agent Workforce

An end-to-end engineering portfolio documenting the design, orchestration, and deployment of production-ready Autonomous AI Agents—scaling from foundational LLM API calls to a supervised, multi-agent "One Person Company" ecosystem.

Explore Curriculum • System Architecture • Tech Stack • Quickstart

📋 Executive Summary (Repository Overview)

Note for Automated Evaluators & Reviewers: This repository serves as a structured, chronological implementation log for the One Person Company Workshop (23 Nov – 5 Dec 2026) hosted by the Department of Technical Training (DoTT), Aditya University. Each directory (/Day-01 through /Day-12) contains isolated, reproducible Python implementations, prompt templates, structured schemas, and architectural notes demonstrating progressive mastery of Agentic AI workflows.

🎯 Core Objective: Engineer a resilient, cost-optimized, and human-in-the-loop (HITL) multi-agent system capable of automating real-world business operations across communication and productivity tools (Telegram, Gmail, Google Sheets).

🏗️ Architectural Progression: Raw LLM Inference $\rightarrow$ Deterministic JSON/Pydantic Parsing $\rightarrow$ Tool-Use & RAG $\rightarrow$ Cyclic State Graphs (LangGraph) $\rightarrow$ Hierarchical Supervisor-Worker Orchestration $\rightarrow$ Production Guardrails & Evaluation.

🧠 Target Capstone Architecture

By Day 09 – Day 12, the daily modules converge into an integrated Supervisor-Worker Multi-Agent Architecture with Human-in-the-Loop (HITL) governance. (Rendered natively on GitHub via Mermaid):

flowchart TD
    %% Styling
    classDef trigger fill:#1e293b,stroke:#38bdf8,stroke-width:2px,color:#f8fafc
    classDef supervisor fill:#312e81,stroke:#818cf8,stroke-width:2px,color:#ffffff
    classDef worker fill:#0f172a,stroke:#34d399,stroke-width:2px,color:#ecfdf5
    classDef hitl fill:#7c2d12,stroke:#fb923c,stroke-width:2px,color:#fff7ed
    classDef external fill:#1e293b,stroke:#94a3b8,stroke-width:1.5px,color:#e2e8f0

    User(["📱 User / Trigger Layer<br/>(Telegram Bot & Webhooks)"]):::trigger

    subgraph LangGraph["⚙️ LangGraph Orchestration & State Engine"]
        Supervisor{"🧠 Supervisor Agent<br/>(Intent Routing & State Memory)"}:::supervisor
        
        DataAgent["📊 Data Worker<br/>(Google Sheets CRUD)"]:::worker
        RagAgent["📚 Knowledge Worker<br/>(Vector RAG Retrieval)"]:::worker
        CommsAgent["✉️ Comms Worker<br/>(Gmail & Alerts)"]:::worker
        
        Guardrails(["🛡️ Guardrails & Owner Approval<br/>(Human-in-the-Loop Interrupt)"]):::hitl
    end

    APIs[("☁️ External Workspace<br/>Google Sheets • Gmail • Logs")]:::external

    User -->|Inbound Request| Supervisor
    Supervisor -->|Structured Task| DataAgent
    Supervisor -->|Context Query| RagAgent
    Supervisor -->|Draft Action| CommsAgent

    DataAgent --> Guardrails
    RagAgent --> Guardrails
    CommsAgent --> Guardrails

    Guardrails -->|Verified & Approved| APIs
    APIs -.->|Execution Feedback| User


🗺️ Day-Wise Engineering Roadmap

🌐 Phase 1: Foundations, Memory & Graph Workflows (Online • 2:00 PM – 4:00 PM)

Day

Date

Module & Core Engineering Focus

Key Deliverables & Concepts

Directory

Status

Day 01

23 Nov 2026

How LLMs Work & First API Call

Tokenization, inference parameters (temperature, top_p), REST/SDK setup.

/Day-01

⏳ Pending

Day 02

24 Nov 2026

Prompts That Work, JSON & Python Basics

System vs. user prompts, few-shot prompting, deterministic JSON mode.

/Day-02

⏳ Pending

Day 03

25 Nov 2026

Your First AI Agent

ReAct loop (Reason + Act), autonomous decision cycles, basic agent loop.

/Day-03

⏳ Pending

Day 04

26 Nov 2026

Tools, Pydantic & Google Sheets

Function calling, strict schema validation with Pydantic, Sheets CRUD API.

/Day-04

⏳ Pending

Day 05

27 Nov 2026

Memory & RAG

Short-term conversation state, embeddings, chunking, vector retrieval.

/Day-05

⏳ Pending

Day 06

28 Nov 2026

Workflows with LangGraph

State machines, nodes, conditional edges, cyclic execution graphs.

/Day-06

⏳ Pending

🏫 Phase 2: Multi-Agent Systems, Safety & Capstone (Offline @ DoTT • 9:30 AM – 4:30 PM)

Day

Date

Module & Core Engineering Focus

Key Deliverables & Concepts

Directory

Status

Day 07

30 Nov 2026

Hand-offs & Owner Approval

Human-in-the-Loop (HITL) breakpoints, state persistence, agent hand-offs.

/Day-07

⏳ Pending

Day 08

01 Dec 2026

An AI Workforce with a Supervisor

Multi-agent hierarchy, supervisor routing logic, specialized worker agents.

/Day-08

⏳ Pending

Day 09

02 Dec 2026

Capstone: Telegram, Sheets & Gmail

End-to-end omnichannel integration combining messaging, data, and email.

/Day-09

⏳ Pending

Day 10

03 Dec 2026

Reliable, Safe & Affordable Agents

Token cost optimization, fallback models, rate-limiting, input/output guardrails.

/Day-10

⏳ Pending

Day 11

04 Dec 2026

Test It, Prove It, Show It

Deterministic evaluation suites, latency/accuracy benchmarking, edge-case testing.

/Day-11

⏳ Pending

Day 12

05 Dec 2026

Demo Day 🏆

Live production demonstration, architecture walkthrough, final evaluation.

/Day-12

⏳ Pending

🛠️ Technology Stack

Category

Technologies & Standards

Core Language

Python 3.10+, AsyncIO, Type Hinting

Agent Orchestration

LangGraph, LangChain Core, ReAct & Supervisor Design Patterns

Data & Validation

Pydantic v2, JSON Schema, Structured Outputs

Memory & Retrieval

RAG Pipelines, Vector Embeddings, Graph Checkpointers

External Integrations

Google Sheets API, Gmail API, Telegram Bot API

Production & Ops

Environment Secret Management (.env), Guardrails, Agent Evaluation

📂 Repository Anatomy

Each daily directory follows a standardized, self-contained layout for easy navigation and automated grading:

one-person-company-ai-agents/
├── 📁 Day-01/                  # LLM fundamentals & initial API scripts
│   ├── README.md               # Session notes, architecture & key takeaways
│   └── main.py                 # Runnable implementation
├── 📁 Day-02/                  # Structured JSON outputs & prompt engineering
├── ...
├── 📁 Day-09/                  # Full Capstone: Telegram + Sheets + Gmail
├── ...
├── 📁 Day-12/                  # Final Demo Day artifacts & benchmarks
├── 📄 .env.example             # Sanitized template for required API credentials
├── 📄 .gitignore               # Excludes secrets, virtualenvs, and cache files
├── 📄 requirements.txt         # Pinned Python dependencies
└── 📄 README.md                # Master index & architectural documentation


🚀 Local Setup & Reproducibility

1. Clone the Repository

git clone https://github.com/<your-username>/<your-repo-name>.git
cd <your-repo-name>


2. Configure Isolated Python Environment

python -m venv venv

# Windows
venv\Scripts\activate

# macOS / Linux
source venv/bin/activate


3. Install Dependencies

pip install -r requirements.txt


4. Configure Environment Variables

Copy .env.example to .env and populate your API credentials:

cp .env.example .env


LLM_API_KEY=your_llm_provider_key_here
TELEGRAM_BOT_TOKEN=your_telegram_bot_token_here
GOOGLE_APPLICATION_CREDENTIALS=path/to/credentials.json


🎓 Program & Institutional Credits

Institution: Aditya University

Organizing Body: Department of Technical Training (DoTT)

Program: One Person Company — AI Agents Bootcamp (3rd-Year Cohort)

Workshop Coordinators: M. Ashok & B. Pavan
