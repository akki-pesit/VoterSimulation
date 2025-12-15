# Synthetic Voter Simulation

Simple Python project that generates a synthetic dataset of 2016 American voters, crafts LLM prompts for each voter, generates candidate messages (REP / DEM) via OpenAI, and queries a local Ollama model to simulate vote choices.

## Files
- `sample.ipynb` — main notebook implementing data generation, prompt creation, and model calls.
- `synthetic_voters_2016.csv` — output dataset produced by the notebook.
- `README.md` — this file.

## Requirements
- Python 3.10+ and `pip`.
- Install dependencies:
    pip install pandas numpy python-dotenv openai ollama-client

## Environment (Windows)
Set the OpenAI API key (used by the OpenAI SDK) in your user environment:
    setx OPENAI_API_KEY "your_api_key_here"

Ensure Ollama is running locally (the notebook expects `http://localhost:11434/v1`).

## How to run
1. Open `sample.ipynb` in PyCharm or Jupyter.
2. Ensure dependencies are installed and environment variables set.
3. Run notebook cells in order.

Outputs:
- `synthetic_voters_2016.csv` (1000 rows by default).
- Candidate messages generated via OpenAI.
- Simulated votes using the local Ollama model with concurrency.

## Notes
- The notebook uses a seeded random generator for reproducible datasets.
- Candidate messages are generated with an OpenAI model; simulated voter choices are produced by a local Ollama model.
- Review and follow the terms of service and usage policies for any LLMs and datasets used.

## License
Project files contain no license by default; add one if needed.
