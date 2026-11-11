# 🤖 Multi-Agent Project Generator

An AI-powered, multi-agent system designed to transform a user's project requirements into a structured, ready-to-develop software project.

The goal is simple: **Describe an idea, generate its initial implementation, and continue development from a working project foundation instead of starting from scratch.**

---

## 🚀 Overview

The Multi-Agent Project Generator is a tool repository for an AI bot that automates the initial stages of software development.

Instead of relying on a single LLM to generate an entire application in one response, the system follows a multi-agent workflow where individual agents handle specific responsibilities.

The system aims to:

- Understand user requirements.
- Analyze project objectives and technical constraints.
- Generate a structured development plan.
- Design an appropriate project architecture.
- Create the initial folder and file structure.
- Generate boilerplate code and essential configuration files.
- Establish a foundation that developers can modify and extend.

The generated project is intended to be a starting point, not necessarily a production-ready application.

## 🧠 Core Architecture

The system follows a modular, agent-based architecture.

```text
             USER REQUIREMENT
                    |
                    v
             ORCHESTRATOR
                    |
                    v
               PLANNER
                    |
          Project Development Plan
                    |
                    v
            AGENT WORKFLOW
                    |
        +-----------+-----------+
        |           |           |
        v           v           v
    ARCHITECT    CODER       CONFIG
      AGENT      AGENT       AGENT
        |           |           |
        +-----------+-----------+
                    |
                    v
            PROJECT GENERATOR
                    |
                    v
             GENERATED FILES
                    |
                    v
             INITIAL PROJECT
```

*Note: This represents the intended architecture. Individual agents and their responsibilities will be implemented incrementally.*

## 🛠️ Technology Stack

| Component | Technology |
|---|---|
| Programming Language | Python |
| AI Planning | Google Gemini |
| LLM Integration | Google GenAI SDK |
| Configuration | Python dotenv |
| Workflow | Multi-Agent Architecture |
| Output | Generated project files and directories |

## 📂 Planned Repository Structure

```text
project-generator/
│
├── agents/
│   ├── planner.py
│   ├── architect.py
│   ├── developer.py
│   └── config_agent.py
│
├── orchestrator/
│   └── orchestrator.py
│
├── tools/
│   ├── file_manager.py
│   ├── directory_manager.py
│   └── code_generator.py
│
├── output/
│   └── generated_projects/
│
├── config/
│   └── settings.py
│
├── .env.example
├── .gitignore
├── requirements.txt
└── README.md
```

*The structure is a planned layout and may evolve as the workflow develops.*

## ⚙️ Workflow

### 1. Requirement Input
The user provides a project description, including its objectives, features, and preferred technologies.

### 2. Project Planning
The Planner Agent analyzes the requirement and generates a structured development plan.

### 3. Architecture Design
The Architect Agent determines the appropriate application structure, modules, and technical dependencies.

### 4. Code Generation
Specialized agents generate the initial source code, configuration files, and required boilerplate.

### 5. Project Assembly
The system creates directories and writes the generated files into the appropriate locations.

### 6. Development Handoff
The generated project is handed over to the developer for further implementation, debugging, customization, and improvements.

## 🔐 Environment Setup

Clone the repository:

```bash
git clone <YOUR_REPOSITORY_URL>
cd project-generator
```

Create a virtual environment:

```bash
python -m venv venv
```

Activate it:

**Windows**
```bash
venv\Scripts\activate
```

**Linux / macOS**
```bash
source venv/bin/activate
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Create a `.env` file:

```env
GEMINI_API=your_gemini_api_key
```

Run the application:

```bash
python main.py
```

*The execution command will be finalized when the main entry point is implemented.*

## 🎯 Development Roadmap

- [x] Initial project concept and architecture.
- [x] Initial planning-agent implementation.
- [ ] Central orchestrator implementation.
- [ ] Structured project planning.
- [ ] Architecture generation agent.
- [ ] Code generation agent.
- [ ] Automated directory and file creation.
- [ ] Dependency and configuration generation.
- [ ] Agent-to-agent communication.
- [ ] Generated project validation.
- [ ] Error handling and retry mechanisms.
- [ ] Support for multiple technology stacks.
- [ ] End-to-end project generation.

## 🔮 Future Scope

The long-term objective is to evolve this repository into a reusable AI development system capable of:

- Generating complete application foundations from natural-language requirements.
- Supporting multiple programming languages and frameworks.
- Allowing agents to review and improve one another's outputs.
- Detecting missing files, dependencies, and implementation issues.
- Maintaining project context for future development sessions.
- Extending generated projects without rebuilding them from scratch.

## 📌 Project Philosophy

**Generate the foundation. Let the developer build the product.**

The system is designed to eliminate repetitive initial development work while keeping the generated code accessible, understandable, and editable by developers.

---

**Status:** Early Development / Initial MVP

**Project Type:** AI | Multi-Agent Systems | Developer Automation