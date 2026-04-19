# Debate

A lightweight debate-style multi-agent AI crew built with `crewai`.

This repository demonstrates a simple debate workflow with two agents (`debater` and `judge`) and three tasks (`propose`, `oppose`, and `decide`). The crew runs sequentially and is configured in the `src/debate/config` files.

## Project structure

- `pyproject.toml` — package metadata and dependencies
- `src/debate/crew.py` — crew definition and agent/task wiring
- `src/debate/main.py` — entrypoint for running the crew
- `src/debate/config/agents.yaml` — agent definitions
- `src/debate/config/tasks.yaml` — task definitions
- `output/` — generated outputs from the debate run

## Requirements

- Python 3.10, 3.11, or 3.12
- `crewai` runtime

## Setup

1. Create and activate a virtual environment:

   ```powershell
   python -m venv .venv
   .venv\Scripts\Activate.ps1
   ```

2. Install dependencies:

   ```powershell
   pip install crewai[tools]
   ```

3. Create an `.env` file and add any required API keys.

## Run

From the repository root:

```powershell
python -m debate.main
```

Or, if you installed package entrypoints:

```powershell
debate
```

The default motion is:

```python
{'motion': 'There needs to be strict laws to regulate LLMs'}
```

## Customize

- Edit `src/debate/config/agents.yaml` to adjust agent roles and settings
- Edit `src/debate/config/tasks.yaml` to change task prompts and behavior
- Edit `src/debate/crew.py` to modify crew composition and workflow
- Edit `src/debate/main.py` to pass different inputs or runtime options


## Notes

- The default LLM is `gemini/gemini-2.5-flash`.
- Crafted for crewAI, this project is intended as a lightweight demo of multi-agent coordination.


