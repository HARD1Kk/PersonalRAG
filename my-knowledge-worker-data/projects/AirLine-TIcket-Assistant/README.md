## Airline Ticket Assistant

An AI-powered Jupyter Notebook that helps explore airline ticket options, pricing, and itineraries. This repo is structured for clarity when viewed on GitHub.

### Features
- **Prototype workflow**: Input trip details, call models/agents, format results
- **Reproducible setup**: Simple virtual environment + `requirements.txt`
- **Safe-by-default**: Uses environment variables for API keys

### Repository Contents
- `AIrLine TIcket assisatant.ipynb`: Main notebook
- `README.md`: This file

### Quickstart
1) Create and activate a virtual environment
```bash
python -m venv .venv
.venv\\Scripts\\activate  # Windows
# source .venv/bin/activate  # macOS/Linux
```

2) Install dependencies (create later if you don't have one yet)
```bash
pip install -r requirements.txt
```

3) Launch Jupyter
```bash
jupyter notebook
```

### Configuration
Store secrets in a `.env` file (do not commit this file):
```bash
# example
OPENAI_API_KEY=sk-...
AZURE_OPENAI_ENDPOINT=...
AZURE_OPENAI_KEY=...
```
Load in Python (example):
```python
import os
from dotenv import load_dotenv
load_dotenv()
openai_key = os.getenv("OPENAI_API_KEY")
```

### Usage
Recommended run order:
1. Configuration: load environment variables
2. Input: set origin, destination, dates, passengers
3. Model/Agent: run the assistant logic
4. Results: inspect itineraries and pricing

Tips:
- Clear notebook outputs before committing to keep diffs small
- If using paid APIs, prefer small, mockable examples for public repos
- Pin versions in `requirements.txt` for reproducibility

### Requirements
If needed, generate from your current environment:
```bash
pip freeze > requirements.txt
```

Suggested packages (if you plan to use them):
- `python-dotenv` for loading `.env`
- `openai` or Azure/OpenAI SDKs
- `pandas`, `numpy`, `requests` for data and HTTP

### .gitignore
Add a `.gitignore` at the repo root to avoid committing noisy or sensitive files:
```gitignore
.env
.ipynb_checkpoints/
__pycache__/
.venv/
venv/
*.py[cod]
data/
models/
*.pt
*.bin
*.h5
*.pkl
```



