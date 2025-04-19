# ⚖️ Agent of Justice

**Agent of Justice** is a fully autonomous courtroom simulation where five role-based agents—**Judge**, **Prosecutor**, **Defense Lawyer**, **Plaintiff**, and **Defendant**—engage in a structured legal trial. The system simulates realistic court proceedings using LLM prompts and state-passed context logic across the entire flow of a trial.

---

## 📁 Repository Structure

```
agent-of-justice/
│
├── courfin.py                  # Core simulation script
├── courtfin.ipynb              # Interactive demo (same logic)
├── Agent_of_Justice.pdf        # Project documentation
├── data.csv                    # Sample inputs and outputs
├── screenshots/                # Visuals of simulation
└── README.md                   # This file
```

---

## ⚙️ How It Works

The simulation follows four well-defined stages:

1. **Opening Statements** – Both lawyers introduce the case.
2. **Arguments & Cross-Examination** – Lawyers ask questions to both Plaintiff and Defendant.
3. **Closing Statements** – Lawyers summarize their arguments.
4. **Final Verdict** – Judge delivers a verdict based on prior context.

Each agent is an instance of a simple class that uses the `InferenceClient` to call a language model. No external orchestration or framework like CrewAI is used—just custom Python classes and step-wise logic to simulate the flow of trial with memory.

---

## 📦 Setup

### 1. Clone this repo

```bash
git clone https://github.com/your-username/agent-of-justice.git
cd agent-of-justice
```

### 2. Install dependencies

```bash
pip install inference
```

### 3. Set up API Key

Create a `.env` file:

```
INFERENCE_API_KEY=your_key_here
```

---

## 🚀 Running the Simulation

### Command Line

```bash
python courfin.py
```

### Jupyter Notebook

Open and run `courtfin.ipynb` to interact with the system in stages.

---

## 🧠 Output Structure

Example output flow:

```
[Opening - Prosecutor]: The facts are clear...
[Defense]: The contract was vague...
[Judge Verdict]: The court rules in favor of the Plaintiff.
```

---

## 🧩 Customization

- Swap in other LLMs via `InferenceClient`
- Change prompt texts for new case contexts
- Expand with memory modules or external RAG

---

## 📌 Notes

- This is a simulation. It does not provide legal advice.
- Screenshots of actual runs are stored in the `screenshots/` folder.
---