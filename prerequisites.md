
# 🛠️ Pre-requisites for Workshop: Executing `aicallcenter.ipynb` with Groq API & LangSmith Tracing

To participate effectively in this workshop, please complete the following setup before the session.

---

## ✅ 1. Python Environment Setup

Ensure Python 3.11 is installed.

### Set up virtual environment (recommended):
```bash
python -m venv aicallcenter-env
source aicallcenter-env/bin/activate  # macOS/Linux
aicallcenter-env\Scripts\activate     # Windows
```

---

## 📦 2. Install Required Python Packages

```bash
pip install openai groq jupyter langchain langchain-core langchain-community langchain-openai langsmith langgraph python-dotenv httpx requests pygments langgraph-checkpoint-sqlite pygraphviz 
```

---

## 🔑 3. Groq API Key Setup

1. Create an account or log in at [https://console.groq.com](https://console.groq.com)
2. Go to **API Keys**, create a key.
3. Set it in your environment:
   - macOS/Linux:
     ```bash
     export GROQ_API_KEY="your-groq-api-key"
     ```
   - Windows CMD:
     ```cmd
     set GROQ_API_KEY=your-groq-api-key
     ```

---

## 📊 4. LangSmith Tracing Setup

LangSmith enables debugging, observability, and performance tracking for LangChain agents.

### Steps:

1. Create a LangSmith account: [https://smith.langchain.com](https://smith.langchain.com)
2. Go to **Settings > API Keys**
3. Add the following to your environment:
   ```bash
   export LANGCHAIN_API_KEY="your-langsmith-api-key"
   export LANGCHAIN_TRACING_V2="true"
   export LANGCHAIN_ENDPOINT="https://api.smith.langchain.com"
   export LANGCHAIN_PROJECT="aicallcenter-workshop"
   ```
   Or in Python:
   ```python
   import os
   os.environ["LANGCHAIN_API_KEY"] = "your-langsmith-api-key"
   os.environ["LANGCHAIN_TRACING_V2"] = "true"
   os.environ["LANGCHAIN_ENDPOINT"] = "https://api.smith.langchain.com"
   os.environ["LANGCHAIN_PROJECT"] = "aicallcenter-workshop"
   ```

---

## 📓 5. Running the Notebook

1. Launch Jupyter:
   ```bash
   jupyter notebook
   ```
2. Open `aicallcenter.ipynb`
3. Confirm your environment variables are set correctly before executing.

