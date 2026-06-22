# ResearchMind — Multi-Agent AI Research System

ResearchMind is an AI-powered **multi-agent research pipeline** that autonomously searches, reads, writes, and critiques research on any topic.

Instead of relying on a single LLM response, this system uses **four specialized AI agents** working together like a research team:

* **Search Agent** → Finds relevant live web sources
* **Reader Agent** → Scrapes and extracts deeper content
* **Writer Chain** → Drafts a structured research report
* **Critic Chain** → Reviews and scores the report

Built using **LangChain + Groq + Tavily + BeautifulSoup + Streamlit**

---

## Live Demo

**Streamlit App:** *(Add your deployed URL here)*

Example:

```bash
https://your-app-name.streamlit.app
```

---

## System Architecture

This project follows an agentic workflow where each AI component has a dedicated responsibility.

### Overall Workflow

![Workflow](images/workflow_overview.png)

---

### Search Agent Flow

Uses **Tavily API** for live internet search.

![Search Agent](images/search_agent.png)

---

### Reader Agent Flow

Uses **BeautifulSoup** to scrape and extract detailed content.

![Reader Agent](images/reader_agent.png)

---

## Features

* Multi-agent autonomous research workflow
* Live web search integration
* Deep content scraping
* Structured report generation
* Research critique and scoring
* Markdown report download
* Modern dark UI
* Streamlit Cloud deployment

---

## Tech Stack

### AI / LLM

* LangChain
* Groq API
* Llama 3.1 8B Instant

### Search

* Tavily Search API

### Scraping

* BeautifulSoup
* Requests

### Frontend

* Streamlit

### Backend

* Python

---

## Project Structure

```bash
multi-agent-system/
│── agents.py          # Agent definitions
│── tools.py           # Tavily + scraping tools
│── pipeline.py        # Multi-agent pipeline logic
│── app.py             # Streamlit frontend
│── requirements.txt
│── pyproject.toml
│── README.md
│── .gitignore
```

---

## How It Works

### Step 1: Search Agent

Searches live internet for recent sources.

Example:

```text
Quantum Computing Breakthroughs in 2025
```

---

### Step 2: Reader Agent

Chooses relevant URLs and scrapes content.

---

### Step 3: Writer Chain

Creates a structured report:

* Introduction
* Key Findings
* Conclusion
* Sources

---

### Step 4: Critic Chain

Reviews the generated report and provides:

* Score
* Strengths
* Weaknesses
* Final verdict

---

## Application UI

### Homepage

![Homepage](images/homepage.png)

---

### Pipeline Execution

![Pipeline Running](images/pipeline_running.png)

---

### Final Generated Report

![Report Output](images/report_output.png)

---

### Critic Feedback

![Critic Output](images/critic_output.png)

---

## Sample Generated Report

A sample generated report is included in this repository:

**File:** [research_report_1782051131.md](https://github.com/user-attachments/files/29190702/research_report_1782051131.md)


Preview:

---

## Installation

Clone repository:

```bash
git clone https://github.com/yourusername/multi-agent-system.git
cd multi-agent-system
```

Install dependencies:

Using UV:

```bash
uv sync
```

Or pip:

```bash
pip install -r requirements.txt
```

---

## Environment Variables

Create a `.env` file:

```env
GROQ_API_KEY=your_groq_api_key
TAVILY_API_KEY=your_tavily_api_key
```

For Streamlit deployment:

Add in **Secrets.toml**

```toml
GROQ_API_KEY="your_groq_api_key"
TAVILY_API_KEY="your_tavily_api_key"
```

---

## Run Locally

```bash
uv run streamlit run app.py
```

---

## Deployment

Deployed on **Streamlit Cloud**

Steps:

1. Push code to GitHub
2. Connect repo to Streamlit Cloud
3. Add API keys in Secrets
4. Deploy

---

## Future Improvements

* PDF export support
* Citation validation
* Better source ranking
* Multi-document synthesis
* Research memory system
* Academic paper integration (Arxiv, Semantic Scholar)

---

## Author

**Smruti Ranjan Nayak**

B.Tech CSE
KIIT University
Aspiring Data Scientist

GitHub: https://github.com/DataScientistNayak

---

## License

MIT License
