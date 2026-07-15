# Agent of Justice

An autonomous courtroom simulation where five role-based LLM agents — Judge,
Prosecutor, Defense Lawyer, Plaintiff, and Defendant — run through a
structured legal trial with shared, evolving context.

## How it works

Each agent is a lightweight class wrapping Hugging Face's `InferenceClient`
(no orchestration framework like CrewAI — just custom Python classes and
step-wise context passing). The trial runs in four stages:

1. **Opening statements** — both lawyers introduce the case.
2. **Arguments & cross-examination** — lawyers question the plaintiff and
   defendant.
3. **Closing statements** — lawyers summarize their positions.
4. **Verdict** — the judge rules, conditioned on the full trial transcript.

## Structure

```
courtfin.py         # Core simulation script
CourtFin.ipynb       # Interactive notebook version
CourtSim.ipynb       # Alternate simulation notebook
Infere.ipynb         # Inference experimentation
cases.csv            # Sample case inputs
output3.csv          # Sample run outputs
screenshots/          # Simulation run screenshots
```

## Running it

```bash
git clone https://github.com/ShlokP06/agents-of-justice.git
cd agents-of-justice
pip install huggingface_hub
export HF_TOKEN=your_hf_token   # Windows: set HF_TOKEN=your_hf_token
python courtfin.py
```

Or open `CourtFin.ipynb` to run the simulation interactively, stage by
stage.

## Notes

This is a simulation for exploring multi-agent LLM interaction — it does
not provide legal advice.
