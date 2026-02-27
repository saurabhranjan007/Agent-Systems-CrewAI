# Agent-Systems-CrewAI

A comprehensive educational codebase demonstrating the **CrewAI framework** for building intelligent multi-agent systems. This course progresses through 6 lessons (L2-L7) with increasing complexity, from basic agent creation to production-ready collaborative workflows.

## 📋 Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Project Structure](#project-structure)
- [Lessons Breakdown](#lessons-breakdown)
- [How to Run](#how-to-run)
- [Environment Setup](#environment-setup)
- [Key Concepts](#key-concepts)
- [Troubleshooting](#troubleshooting)

## 🎯 Overview

This repository contains practical examples and tutorials for building AI-powered multi-agent systems using CrewAI. Each lesson introduces new concepts and builds on previous knowledge:

- **Foundation**: Creating agents with roles, goals, and backstories
- **Integration**: Adding tools and external capabilities to agents
- **Collaboration**: Orchestrating multiple agents to work together
- **Real-World Applications**: Job application automation, financial analysis, event planning, customer support

## ✨ Features

- **Progressive Learning Path**: 6 structured lessons with increasing complexity
- **Practical Examples**: Real-world use cases (article writing, customer support, financial analysis, job applications)
- **Tool Integration**: Demonstrates web scraping, API calls, and custom tool creation
- **Multi-Agent Patterns**: Task delegation, role specialization, quality assurance, collaboration
- **Well-Documented**: Jupyter notebooks with detailed explanations and expected outputs
- **Modular Design**: Self-contained lessons with reusable utilities

## 📦 Prerequisites

Before you begin, ensure you have:

- **Python 3.8+** installed
- **pip** or **conda** package manager
- **API Keys** for:
  - OpenAI (GPT-3.5 or GPT-4) - `OPENAI_API_KEY`
  - Serper (for web search) - `SERPER_API_KEY` (required for L2, L3, L4)
  - Optional: Other service APIs depending on the lesson

## 🚀 Installation

### 1. Clone the Repository
```bash
git clone https://github.com/saurabhranjan007/Agent-Systems-CrewAI.git
cd Agent-Systems-CrewAI
```

### 2. Create a Virtual Environment
```bash
# Using venv
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# OR using conda
conda create -n crewai-env python=3.10
conda activate crewai-env
```

### 3. Install Dependencies
```bash
pip install -r requirements.txt
```

**Required Packages:**
- `crewai==0.28.8` - Multi-agent orchestration framework
- `crewai_tools==0.1.6` - Built-in tools (web search, file operations)
- `langchain_community==0.0.29` - LLM integrations and utilities

## 📁 Project Structure

```
Agent-Systems-CrewAI/
├── README.md                          # This file
├── requirements.txt                   # Project dependencies
├── utils.py                           # Shared utilities (API key management, output formatting)
│
├── L2/
│   └── L2_research_write_article.ipynb    # Lesson 2: Multi-Agent Research & Article Writing
│
├── L3/
│   ├── L3_customer_support.ipynb          # Lesson 3: Customer Support with Tools
│   └── utils.py                           # Lesson-specific utilities
│
├── L4/
│   ├── L4_tools_customer_outreach.ipynb   # Lesson 4: Custom Tools & Business Outreach
│   ├── utils.py                           # Lesson-specific utilities
│   └── instructions/                      # Business strategy templates
│       ├── enterprise_solutions_framework.md
│       ├── small_business_engagement.md
│       └── tech_startups_outreach.md
│
├── L5/
│   ├── L5_tasks_event_planning.ipynb      # Lesson 5: Event Planning & Task Orchestration
│   └── utils.py                           # Lesson-specific utilities
│
├── L6/
│   ├── L6_collaboration_financial_analysis.ipynb  # Lesson 6: Financial Analysis Collaboration
│   └── utils.py                           # Lesson-specific utilities
│
└── L7/
    ├── L7_job_application_crew.ipynb      # Lesson 7: Job Application Automation
    ├── fake_resume.md                     # Sample resume for job application
    └── utils.py                           # Lesson-specific utilities
```

## 📚 Lessons Breakdown

| Lesson | Topic | Focus | Key Agents |
|--------|-------|-------|-----------|
| **L2** | Research & Article Writing | Basic multi-agent collaboration | Planner, Writer, Editor |
| **L3** | Customer Support | Tool integration & quality assurance | Support Agent, Quality Assurance |
| **L4** | Business Outreach | Custom tools & business strategies | Sales Agent, Custom Tool Creator |
| **L5** | Event Planning | Task delegation & coordination | Organizer, Coordinator, Evaluator |
| **L6** | Financial Analysis | Complex collaboration workflows | Analyst, Risk Manager, Trader |
| **L7** | Job Application | Real-world automation | Resume Reviewer, Tailorer, Interviewer |

### Detailed Lesson Descriptions

#### **Lesson 2: Research & Article Writing (L2)**
Learn the fundamentals of CrewAI by building a content creation pipeline.
- Create Agents with specific roles and backstories
- Define Tasks for agents to execute
- Orchestrate agents through a Crew
- Generate a full blog article on a given topic

#### **Lesson 3: Customer Support (L3)**
Extend your agents with tools and implement quality assurance.
- Integrate external tools (web search, file operations)
- Build multi-step quality assurance workflows
- Handle customer inquiries with specialized agents
- Evaluate output quality

#### **Lesson 4: Business Outreach (L4)**
Create custom tools and implement business-focused strategies.
- Build custom tools for specific tasks
- Implement sentiment analysis
- Create targeted outreach strategies for different business segments
- Use instruction templates for consistent messaging

#### **Lesson 5: Event Planning (L5)**
Master task coordination and delegation patterns.
- Design complex task hierarchies
- Implement task dependencies
- Coordinate multiple agents on a single project
- Handle planning, logistics, and evaluation

#### **Lesson 6: Financial Analysis (L6)**
Build collaborative workflows for complex domains.
- Create domain-specific agents (Risk Analyst, Trader, Researcher)
- Implement financial data analysis
- Build trading recommendation systems
- Coordinate specialized agents with different expertise

#### **Lesson 7: Job Application (L7)**
Apply everything to a real-world use case.
- Automate resume screening and tailoring
- Create interview preparation agents
- Build end-to-end job application workflows
- Practical insights into production-like multi-agent systems

## 🎮 How to Run

### Option 1: Run All Lessons
```bash
# Navigate to each lesson directory and run the Jupyter notebook
cd L2
jupyter notebook L2_research_write_article.ipynb
```

### Option 2: Run Specific Lesson
```bash
# Example: Run Lesson 5 (Event Planning)
cd L5
jupyter notebook L5_tasks_event_planning.ipynb
```

### Option 3: Run from Command Line
```bash
# Start Jupyter Lab to browse all notebooks
jupyter lab
# Then navigate to any lesson folder and open the notebook
```

### Within Jupyter Notebook
1. Open the notebook file in Jupyter
2. Ensure your `.env` file is properly configured (see [Environment Setup](#environment-setup))
3. Execute cells sequentially from top to bottom
4. Follow the markdown explanations between code cells

## 🔐 Environment Setup

### 1. Create a `.env` File

Create a `.env` file in the project root directory:

```bash
# In the Agent-Systems-CrewAI directory
touch .env
```

### 2. Add Your API Keys

Add the following to your `.env` file:

```env
# Required: OpenAI API Key
OPENAI_API_KEY=sk-your-openai-api-key-here

# Required for Lessons 2, 3, 4: Serper API Key (web search)
SERPER_API_KEY=your-serper-api-key-here

# Optional: Other API keys depending on custom tools
# DATABASE_URL=your-database-url
# OTHER_API_KEY=your-api-key
```

### 3. Verify Setup

Run this quick test to verify your environment:

```python
# In any Jupyter cell
from utils import get_openai_api_key, get_serper_api_key
import os

openai_key = get_openai_api_key()
serper_key = get_serper_api_key()

print(f"OpenAI Key configured: {bool(openai_key)}")
print(f"Serper Key configured: {bool(serper_key)}")
os.environ["OPENAI_MODEL_NAME"] = 'gpt-3.5-turbo'  # or 'gpt-4'
```

## 🧠 Key Concepts

### Agents
Autonomous entities with:
- **Role**: What the agent is (e.g., Content Writer, Customer Support Agent)
- **Goal**: What it's trying to accomplish
- **Backstory**: Context to help the LLM understand the role
- **Tools**: External capabilities (web search, file operations, custom functions)

### Tasks
Specific work items assigned to agents:
- **Description**: What needs to be done
- **Expected Output**: What the task should produce
- **Agent**: Which agent executes the task

### Crew
Orchestration layer that:
- Manages multiple agents
- Coordinates task execution
- Handles inter-agent communication
- Produces final output

### Tools
External capabilities integrated into agents:
- Built-in tools: Web search, file reading, code execution
- Custom tools: Domain-specific functions
- Integration: LangChain tool wrappers

## 🛠️ Troubleshooting

### Issue: "API Key not found"
**Solution**: 
- Ensure `.env` file exists in the project root
- Verify API keys are correctly formatted in `.env`
- Try loading environment with: `from utils import load_env; load_env()`

### Issue: "Module not found: crewai"
**Solution**:
```bash
pip install -r requirements.txt
# Or manually:
pip install crewai==0.28.8 crewai_tools==0.1.6 langchain_community==0.0.29
```

### Issue: "Jupyter kernel not found"
**Solution**:
```bash
# Ensure Jupyter is installed in your virtual environment
pip install jupyter jupyterlab
# Then run:
jupyter notebook
```

### Issue: "Web search is not working (L2-L4)"
**Solution**:
- Verify `SERPER_API_KEY` in your `.env` file
- Check Serper API quota at https://serper.dev/dashboard
- Ensure internet connection is active

### Issue: "Slow agent responses"
**Solution**:
- Switch to faster model: `GPT-3.5-turbo` (cheaper & faster)
- Check if API rate limits are being hit
- Add delays between requests if running multiple notebooks

### Issue: "Output formatting issues"
**Solution**:
- Reload the notebook cell: `from utils import pretty_print_result`
- Use the `pretty_print_result()` function for better formatting

## 📖 Getting Started

1. **Start with L2**: Understand the basics of agents, tasks, and crews
2. **Progress through L3-L5**: Learn tool integration, collaboration patterns, and task orchestration
3. **Study L6**: See how complex domain-specific workflows are built
4. **Experiment with L7**: Apply concepts to a real-world use case
5. **Customize**: Modify prompts, agents, and tasks for your own use cases

## 🤝 Contributing

This is an educational repository. Feel free to:
- Extend lessons with new agents and tasks
- Add custom tools
- Create new lesson modules
- Fix issues or improve documentation

## 📝 License

This project is provided for educational purposes.

## 🔗 Resources

- **CrewAI Documentation**: https://docs.crewai.co
- **OpenAI API**: https://platform.openai.com
- **Serper API**: https://serper.dev
- **LangChain**: https://python.langchain.com