# BDA-Final-Project-ML-Research-Navigator
ML Research Navigator is an AI-assisted research intelligence platform designed to help researchers evaluate, explore, and validate research ideas using retrieval-grounded literature analysis.

Unlike traditional academic search engines that focus on finding papers, Research Navigator focuses on answering a higher-level question:

> Is this research idea promising, novel, and worth pursuing?

The system combines literature retrieval, concept analysis, pitfall detection, baseline recommendation, research-gap discovery, and evidence-based scoring into a single workflow.


---

# Why ML Research Navigator?
Traditional academic search engines help users find papers. Research Navigator helps users evaluate whether a research direction is promising, saturated, flawed, or worth pursuing with built-in clear ML domain doctrines into the prompts.

---

# Features

## Literature Retrieval

* Concept-based paper discovery
* Multi-venue search support
* Publication year filtering
* Retrieval-grounded analysis

## Research Intelligence

* Methodology comparison
* Related concept discovery
* Research gap analysis
* Baseline candidate recommendation
* SWOT analysis
* Concept popularity and saturation analysis

## Concept Validation

* Doctrinal pitfall detection
* Evidence-driven evaluation
* S-to-F grading framework
* Confidence scoring

## Explainable Outputs

Every major conclusion is supported by:

* Retrieved papers
* Evidence matrices
* Coverage statistics
* Explicit reasoning chains

---

# System Workflow

Research Navigator follows a retrieval-grounded workflow:

```text
User Query
    ↓
Concept Pitfall Radar
    ↓
Literature Retrieval
    ↓
Evidence Matrix Construction
    ↓
Research Vector Construction
    ↓
Unified Scoring Kernel
    ↓
Research Report Generation
```

The system is designed to minimize unsupported conclusions by separating evidence collection from analysis.

---

# Architecture

```text
┌──────────────────────────┐
│         User             │
└────────────┬─────────────┘
             │
             ▼
┌──────────────────────────┐
│      Gradio Frontend     │
└────────────┬─────────────┘
             │
             ▼
┌──────────────────────────┐
│     Query Constructor    │
└────────────┬─────────────┘
             │
             ▼
┌──────────────────────────┐
│     Concept Pitfall      │
│         Radar            │
└────────────┬─────────────┘
             │
             ▼
┌──────────────────────────┐
│     Literature Search    │
│      (LLM + APIs)        │
└────────────┬─────────────┘
             │
             ▼
┌──────────────────────────┐
│      Evidence Matrix     │
│       Constructor        │
└────────────┬─────────────┘
             │
             ▼
┌──────────────────────────┐
│      Research Vector     │
│       Constructor        │
└────────────┬─────────────┘
             │
             ▼
┌──────────────────────────┐
│   Unified Scoring Kernel │
└────────────┬─────────────┘
             │
             ▼
┌──────────────────────────┐
│     Report Generator     │
└────────────┬─────────────┘
             │
             ▼
┌──────────────────────────┐
│ Structured Research      │
│ Report + Scores          │
└──────────────────────────┘
```

---

# Supported Analysis Types

* Explain / Compare Methodologies
* Related Concept Discovery
* Research Gap Analysis
* Baseline Recommendation
* Concept Popularity Analysis
* Saturation Risk Analysis
* SWOT Analysis
* Concept Validation
* Pitfall Detection

---

# Installation

## Requirements

* Python 3.10+
* Gradio
* OpenAI API access
* Internet connection

Install dependencies:

```bash
pip install gradio
pip install openai
```

Additional dependencies may be required depending on the selected search provider.

---

# Configuration

Set your API key before launching:

```python
from openai import OpenAI

client = OpenAI(
    api_key="YOUR_API_KEY"
)
```

Select the desired search-enabled model in the application interface.

---

# Running the Application

Current release is provided as a Jupyter Notebook (`.ipynb`).

## Option 1: VS Code

1. Open the notebook in VS Code.
2. Install the Python and Jupyter extensions if required.
3. Execute notebook cells sequentially.
4. Launch the Gradio interface.
5. Open the generated local or public Gradio URL in a web browser.

## Option 2: Jupyter Notebook / JupyterLab

1. Open the notebook.
2. Run all cells.
3. Wait for Gradio initialization.
4. Open the generated URL.

After launch, users can interact with Research Navigator through the web interface.

---

# Example Query

Research Concept:

```text
Stock prediction with attribute atomized HINs and SSM
```

Requested Analysis:

```text
- Concept Validation
- Baseline Candidates
- Research Gap Analysis
- SWOT Analysis
```

Output:

```text
Retrieved Papers
Evidence Matrix
Baseline Recommendations
Saturation Scores
SWOT Scores
Research Direction Suggestions
```

---

# Current Limitations

* Analysis quality depends on retrieved search results.
* Search APIs may return incomplete coverage.
* Some publishers restrict full-text access.
* LLM-generated reasoning remains dependent on evidence quality.
* Large literature surveys may incur significant API costs.

---

# Future Work

* PDF export
* Citation export
* Automatic evidence matrix visualization
* Multi-agent research workflows
* Local retrieval database
* Long-term project memory
* Collaborative research sessions

---

# Disclaimer

Research Navigator is intended to assist research exploration and decision-making.

Users should independently verify important conclusions, citations, and research recommendations before publication or deployment.
