# 🛠️ Coding Buddy
### AI-powered coding assistant that turns natural language into working projects.

**Coding Buddy** is built with **LangGraph** and behaves like a multi-agent dev team: it takes a plain-English request and produces a complete, runnable codebase — file by file — following real developer workflows.

---

## 🏗️ Architecture
![Coding Buddy Architecture](coding-buddy-main/resources/coder_buddy_diagram.png)

- **Planner Agent** — analyzes your request and drafts a detailed project plan.  
- **Architect Agent** — decomposes the plan into explicit engineering tasks with file-level context.  
- **Coder Agent** — implements tasks, writes files, and uses available tools like a real developer.

---

## 🚀 Getting Started
### Prerequisites
- **uv** installed (Python package/deps manager).  
- **Groq** account and API key.

> Create your `.env` from `.sample_env` and add the required keys/values.

### ⚙️ Installation & Startup
```bash
# 1) Create & activate a virtual environment
uv venv
source .venv/bin/activate    # Windows: .\.venv\Scripts\activate

# 2) Install dependencies
# If using requirements:
uv pip install -r requirements.txt
# If managed via pyproject:
# uv sync   # (alternative for pyproject-based installs)

# 3) Configure environment
cp .sample_env .env
# then edit .env with your GROQ_API_KEY and other variables

# 4) Run
python main.py
