# chef-assistant

An AI-powered personal chef assistant built with LangChain.

This project uses a LangChain agent and a Tavily web search tool to suggest recipes and cooking instructions based on the ingredients you have available.

## Key files

- `personal_chef.py` - defines the `web_search` tool and creates the `agent` using a system prompt.
- `langgraph.json` - configuration for loading the agent graph and environment settings.
- `env_utils.py` - helper script for verifying Python environment, virtual environment, and dependency setup.
- `requirements.txt` / `pyproject.toml` - project dependencies.

## Requirements

- Python 3.12 or 3.13
- `pip` or a virtual environment manager
- `.env` file with any required API keys or environment values

## Setup

1. Create and activate a virtual environment:

   Windows PowerShell:
   ```powershell
   python -m venv .venv
   .\.venv\Scripts\Activate.ps1
   ```

   Windows CMD:
   ```cmd
   python -m venv .venv
   .\.venv\Scripts\activate
   ```

2. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

   Or, if you are using `uv`:

   ```bash
   uv sync
   ```

3. Create a `.env` file in the repository root if one is not already present.

4. Optionally run the environment checker:

   ```bash
   python env_utils.py
   ```

5. Start the LangGraph development server to test the agent locally:

   ```bash
   langgraph dev
   ```