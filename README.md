🤖 One Person Company — Autonomous AI Agents & Multi-Agent Workforce

<p align="center">
<strong>From LLM Fundamentals to an Autonomous, Supervised AI Workforce</strong>
</p>

<p align="center">
<img src="https://img.shields.io/badge/Python-3.10%2B-blue?logo=python&logoColor=white" />
<img src="https://img.shields.io/badge/Agentic_AI-Multi--Agent-purple" />
<img src="https://img.shields.io/badge/Orchestration-LangGraph-green" />
<img src="https://img.shields.io/badge/Validation-Pydantic-red" />
<img src="https://img.shields.io/badge/Workshop-2026-orange" />
<img src="https://img.shields.io/badge/Status-In_Progress-yellow" />
</p>

📌 About the Project

One Person Company — Autonomous AI Agents & Multi-Agent Workforce is a hands-on AI engineering project focused on designing, developing, and orchestrating autonomous AI agents capable of performing real-world business operations.

Developed as part of the One Person Company — AI Agents Bootcamp organized by the Department of Technical Training (DoTT), Aditya University, this repository documents a 12-day engineering journey covering the complete progression of Agentic AI development.

The journey begins with foundational Large Language Model (LLM) API integration and progresses through structured outputs, prompt engineering, tool calling, memory, Retrieval-Augmented Generation (RAG), LangGraph workflows, and multi-agent orchestration.

The final objective is to build a supervised AI-powered One Person Company, where a central Supervisor Agent coordinates specialized AI workers to automate communication, data management, and knowledge retrieval.

🎯 Project Objectives
Understand LLM fundamentals and integrate models through Python APIs.
Design effective prompts and generate structured, validated outputs.
Develop autonomous agents using reasoning and tool-execution loops.
Integrate external tools and APIs into AI workflows.
Implement conversational memory and Retrieval-Augmented Generation.
Build stateful, cyclic workflows using LangGraph.
Design hierarchical Supervisor–Worker multi-agent systems.
Implement Human-in-the-Loop (HITL) approval mechanisms.
Integrate Telegram, Gmail, and Google Sheets.
Improve reliability, security, performance, and cost efficiency.
🧠 Target System Architecture

The capstone system follows a Supervisor–Worker Multi-Agent Architecture powered by LangGraph.

A central Supervisor Agent receives user requests, understands the intent, and delegates tasks to specialized agents. Each worker performs a dedicated function, while a Human-in-the-Loop layer provides authorization before sensitive external operations are executed.

Architecture Diagram
mermaid
flowchart TD
    User(["📱 User / Trigger Layer<br/>Telegram Bot & Webhooks"])

    subgraph Engine["⚙️ LangGraph Orchestration & State Engine"]
        Supervisor{"🧠 Supervisor Agent<br/>Intent Routing & State Management"}

        DataAgent["📊 Data Worker<br/>Google Sheets CRUD"]

        RagAgent["📚 Knowledge Worker<br/>Vector RAG Retrieval"]

        CommsAgent["✉️ Communication Worker<br/>Gmail & Notifications"]

        Guardrails(["🛡️ Human-in-the-Loop<br/>Owner Approval & Guardrails"])
    end

    APIs[("☁️ External Workspace<br/>Google Sheets • Gmail • Logs")]

    User -->|Incoming Request| Supervisor

    Supervisor -->|Data Operations| DataAgent
    Supervisor -->|Knowledge Queries| RagAgent
    Supervisor -->|Communication Tasks| CommsAgent

    DataAgent --> Guardrails
    RagAgent --> Guardrails
    CommsAgent --> Guardrails

    Guardrails -->|Approved Actions| APIs
    Guardrails -->|Rejected / Modified| Supervisor

    APIs -.->|Execution Feedback| Supervisor
    Supervisor -.->|Response / Notification| User

Core Components
Component	Responsibility
User Interface	Receives requests through Telegram and webhooks.
Supervisor Agent	Understands user intent, delegates tasks, and coordinates workers.
Data Worker	Performs structured Google Sheets operations.
Knowledge Worker	Retrieves relevant information using RAG pipelines.
Communication Worker	Handles Gmail drafting and communication workflows.
LangGraph Engine	Manages workflow state, execution paths, and agent coordination.
Human-in-the-Loop	Controls sensitive operations through owner approval.
External Workspace	Connects the agents with Google services and application logs.
Expected Workflow
The user submits a request through Telegram.
The Supervisor Agent interprets the request.
The supervisor identifies the appropriate specialized worker.
The selected worker processes the task using its assigned tools.
The proposed operation passes through the configured validation and approval process.
The owner approves, rejects, or modifies the proposed action when authorization is required.
Approved operations are executed through the relevant external API.
The result is recorded and communicated back to the user.
The workflow state is updated for future interactions.
🗺️ 12-Day Engineering Roadmap

The project is divided into two phases, progressing from foundational AI concepts to integrated multi-agent systems.

🌐 Phase 1 — Foundations, Memory & Graph Workflows

Mode: Online

Schedule: 23 November – 28 November 2026

Time: 2:00 PM – 4:00 PM

Day	Date	Module	Core Concepts	Directory
01	23 Nov 2026	How LLMs Work & First API Call	Tokenization, inference parameters, temperature, top-p, REST APIs, SDK integration.	Day-01/
02	24 Nov 2026	Prompt Engineering, JSON & Python	System prompts, user prompts, few-shot prompting, structured JSON outputs.	Day-02/
03	25 Nov 2026	Your First AI Agent	ReAct loop, reasoning, tool execution, autonomous decision cycles.	Day-03/
04	26 Nov 2026	Tools, Pydantic & Google Sheets	Function calling, structured schemas, Pydantic validation, Sheets CRUD.	Day-04/
05	27 Nov 2026	Memory & RAG	Conversation memory, embeddings, chunking, vector retrieval, contextual search.	Day-05/
06	28 Nov 2026	Workflows with LangGraph	State machines, nodes, edges, conditional routing, cyclic workflows.	Day-06/
🏫 Phase 2 — Multi-Agent Systems, Safety & Capstone

Mode: Offline @ Department of Technical Training (DoTT)

Schedule: 30 November – 5 December 2026

Time: 9:30 AM – 4:30 PM

Day	Date	Module	Core Concepts	Directory
07	30 Nov 2026	Agent Hand-offs & Owner Approval	Human-in-the-Loop, interrupts, persistent state, agent hand-offs.	Day-07/
08	01 Dec 2026	An AI Workforce with a Supervisor	Multi-agent hierarchy, supervisor routing, specialized worker agents.	Day-08/
09	02 Dec 2026	Capstone: Telegram, Sheets & Gmail	Omnichannel integration, messaging, spreadsheet operations, email automation.	Day-09/
10	03 Dec 2026	Reliable, Safe & Affordable Agents	Token optimization, fallback models, rate limiting, error handling, guardrails.	Day-10/
11	04 Dec 2026	Testing, Evaluation & Benchmarking	Test suites, accuracy, latency, edge cases, performance benchmarking.	Day-11/
12	05 Dec 2026	Final Demo Day 🏆	Integrated system demonstration, architecture walkthrough, final implementation.	Day-12/
Learning Progression
mermaid
flowchart TD
    A["Day 01<br/>LLM Fundamentals"]
    B["Day 02<br/>Prompt Engineering & JSON"]
    C["Day 03<br/>AI Agents & ReAct"]
    D["Day 04<br/>Tools & Pydantic"]
    E["Day 05<br/>Memory & RAG"]
    F["Day 06<br/>LangGraph Workflows"]
    G["Day 07<br/>Human-in-the-Loop"]
    H["Day 08<br/>Supervisor & Workers"]
    I["Day 09<br/>Integrated Capstone"]
    J["Day 10<br/>Reliability & Guardrails"]
    K["Day 11<br/>Testing & Benchmarking"]
    L["Day 12<br/>Final Demonstration"]

    A --> B --> C --> D --> E --> F
    F --> G --> H --> I --> J --> K --> L

🛠️ Technology Stack
Category	Technologies	Application
Programming Language	Python 3.10+, AsyncIO, Type Hints	Core application development
LLM Integration	LLM APIs, Python SDKs	Model inference and generation
Agent Frameworks	LangChain Core, LangGraph	Agent development and orchestration
Agent Patterns	ReAct, Supervisor–Worker	Autonomous execution and delegation
Structured Outputs	JSON, JSON Schema, Pydantic v2	Data validation and structured responses
Memory & Retrieval	Embeddings, Vector Search, RAG	Contextual knowledge retrieval
State Management	LangGraph Checkpointers	Persistent workflow state
Messaging	Telegram Bot API	User interaction and notifications
Email	Gmail API	Email drafting and communication
Productivity	Google Sheets API	Spreadsheet and data operations
Configuration	Python-dotenv, Environment Variables	Application configuration
Reliability	Retry Logic, Rate Limiting, Fallback Models	Resilient execution
Testing	Pytest, Custom Evaluation Scripts	Testing and benchmarking
📂 Repository Structure

The repository follows a modular, chronological structure. Each day contains an independent implementation demonstrating the concepts introduced in that module.

text
one-person-company-ai-agents/
│
├── Day-01/
│   ├── README.md
│   └── main.py
│
├── Day-02/
│   ├── README.md
│   └── main.py
│
├── Day-03/
│   ├── README.md
│   └── main.py
│
├── Day-04/
│   ├── README.md
│   └── main.py
│
├── Day-05/
│   ├── README.md
│   └── main.py
│
├── Day-06/
│   ├── README.md
│   └── main.py
│
├── Day-07/
│   ├── README.md
│   └── main.py
│
├── Day-08/
│   ├── README.md
│   └── main.py
│
├── Day-09/
│   ├── README.md
│   └── main.py
│
├── Day-10/
│   ├── README.md
│   └── main.py
│
├── Day-11/
│   ├── README.md
│   └── main.py
│
├── Day-12/
│   ├── README.md
│   └── main.py
│
├── .env.example
├── .gitignore
├── requirements.txt
└── README.md

Daily Module Organization

Each daily directory follows a consistent documentation and implementation format:

File	Description
README.md	Module overview, learning objectives, technical concepts, architecture, and execution instructions.
main.py	Runnable Python implementation of the primary module concept.
Supporting files	Prompt templates, schemas, configuration files, test cases, and sample datasets when required.

This organization keeps the implementations modular, easy to understand, and independently executable.

🚀 Getting Started

Follow these steps to set up the project locally.

Prerequisites
Python 3.10 or higher.
Git.
An API key from your selected LLM provider.
Telegram Bot Token for Telegram integration.
Google Cloud credentials for Gmail and Google Sheets integration.
1. Clone the Repository
bash
git clone https://github.com/<your-username>/<your-repo-name>.git

cd <your-repo-name>

2. Create a Virtual Environment
bash
python -m venv venv


Windows:

bash
venv\Scripts\activate


macOS / Linux:

bash
source venv/bin/activate

3. Install Dependencies
bash
python -m pip install --upgrade pip

pip install -r requirements.txt

4. Configure Environment Variables

Create a .env file using the example template:

bash
cp .env.example .env


For Windows PowerShell:

powershell
Copy-Item .env.example .env


Add the required credentials:

env
# LLM Provider
LLM_API_KEY=your_llm_provider_api_key

# Telegram Bot
TELEGRAM_BOT_TOKEN=your_telegram_bot_token

# Google Workspace
GOOGLE_APPLICATION_CREDENTIALS=path/to/credentials.json


Never commit API keys, private credentials, or sensitive environment files to GitHub.

5. Run an Individual Module

Each daily implementation can be executed independently.

Example:

bash
python Day-01/main.py


To explore subsequent modules:

bash
python Day-02/main.py
python Day-03/main.py


Refer to the corresponding README.md inside each directory for module-specific dependencies and execution instructions.

🔐 Security & Responsible AI

Security and controlled execution are important considerations when developing autonomous AI systems.

The project follows these engineering principles:

Environment-based configuration: Keep API keys and sensitive credentials outside source code.
Input validation: Validate incoming data using Pydantic and explicit schemas.
Output validation: Verify LLM-generated structured data before tool execution.
Human authorization: Require owner approval for sensitive or consequential actions.
Error handling: Implement exception handling, retries, and safe failure paths.
Rate limiting: Prevent uncontrolled API requests and execution loops.
Cost optimization: Monitor token consumption and use appropriate models for different tasks.
State persistence: Preserve workflow context across interruptions.
Logging: Maintain execution records for debugging and observability.
🧪 Testing & Performance

The project incorporates testing and benchmarking as part of the engineering workflow.

Key areas include:

Area	Description
Functional Testing	Verify that each agent performs its assigned task correctly.
Schema Validation	Test structured outputs against Pydantic models and JSON schemas.
Tool Execution	Verify tool selection, parameters, and execution results.
Agent Coordination	Test supervisor routing and worker delegation.
Retrieval Testing	Measure relevance and accuracy of retrieved information.
HITL Testing	Verify approval, rejection, and interruption workflows.
Integration Testing	Test communication with Telegram and Google APIs.
Latency Benchmarking	Measure task execution and response times.
Cost Monitoring	Track token consumption and API usage.
Error Handling	Test recovery from invalid inputs, API failures, and timeouts.

Performance results and implementation-specific test evidence will be documented alongside the relevant daily modules.

📊 Project Progress
Day	Module	Status
Day 01	LLM Fundamentals & API Integration	⏳ Pending
Day 02	Prompt Engineering & Structured JSON	⏳ Pending
Day 03	Autonomous AI Agents	⏳ Pending
Day 04	Tools, Pydantic & Google Sheets	⏳ Pending
Day 05	Memory & RAG	⏳ Pending
Day 06	LangGraph Workflows	⏳ Pending
Day 07	Human-in-the-Loop	⏳ Pending
Day 08	Supervisor–Worker Architecture	⏳ Pending
Day 09	Telegram, Sheets & Gmail Capstone	⏳ Pending
Day 10	Reliability, Safety & Optimization	⏳ Pending
Day 11	Testing & Benchmarking	⏳ Pending
Day 12	Final Demonstration	⏳ Pending

Status Legend:

⏳ Pending
🔄 In Progress
✅ Completed
⚠️ Blocked
🏆 Expected Project Outcomes

The final project aims to bring together the following capabilities:

Python-based LLM integrations and structured model interactions.
Autonomous agents with reasoning and tool-execution capabilities.
Validated structured outputs using Pydantic and JSON Schema.
Memory-enabled AI workflows and contextual RAG retrieval.
Stateful orchestration using LangGraph.
Specialized worker agents coordinated by a central supervisor.
Human-in-the-Loop approval and execution governance.
Telegram-based user interaction.
Google Sheets data operations.
Gmail communication workflows.
Error handling, cost optimization, and production-oriented guardrails.
Testing, benchmarking, and documented implementation results.
🎓 Program & Institutional Credits
Attribute	Details
Institution	Aditya University
Organizing Department	Department of Technical Training (DoTT)
Program	One Person Company — AI Agents Bootcamp
Cohort	3rd-Year Cohort
Workshop Duration	23 November – 5 December 2026
💡 Project Vision

One Human. Multiple AI Agents. One Coordinated Digital Workforce.

The vision behind this project is to explore how autonomous AI agents can transform the way individuals manage business operations.

Rather than building isolated AI scripts, this project focuses on creating an interconnected ecosystem where specialized agents can understand instructions, collaborate, access external tools, retrieve knowledge, and execute approved tasks.

From foundational LLM API calls to a supervised multi-agent architecture, this repository represents a practical journey into the engineering of modern Agentic AI systems.

<p align="center">
<strong>Built with Python ❤️ and Agentic AI</strong>
<br>
<sub>One Person Company AI Agents Bootcamp | Aditya University | 2026</sub>
</p>
