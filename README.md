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

**Streamlit App:** https://srn-researchmind-multi-agent-system.streamlit.app/

---

## System Architecture

This project follows an agentic workflow where each AI component has a dedicated responsibility.

### Overall Workflow

### Search Agent Flow

Uses **Tavily API** for live internet search.

<img width="637" height="308" alt="Screenshot 2026-06-22 101927" src="https://github.com/user-attachments/assets/7d37048d-fc1e-4a9d-983d-fafefdd1ffb4" />

---

### Reader Agent Flow

Uses **BeautifulSoup** to scrape and extract detailed content.

<img width="485" height="317" alt="Screenshot 2026-06-22 101943" src="https://github.com/user-attachments/assets/c80d0fc7-75a3-419f-9b61-418fb2594fa6" />

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
<img width="959" height="440" alt="Screenshot 2026-06-21 194440" src="https://github.com/user-attachments/assets/5855bce4-208f-4895-9f04-657d548713db" />

---

### Pipeline Execution

<img width="959" height="440" alt="Screenshot 2026-06-21 194502" src="https://github.com/user-attachments/assets/048d0356-c781-453b-94ff-9a9ae950565b" />


---

### Final Generated Report

<img width="959" height="437" alt="Screenshot 2026-06-21 194523" src="https://github.com/user-attachments/assets/7d478a69-c346-4367-8de6-3bc2fc17f37a" />
<img width="940" height="435" alt="Screenshot 2026-06-21 194538" src="https://github.com/user-attachments/assets/ff83b1fe-f23d-4cf7-9fa1-93ec9b13e59f" />
<img width="959" height="425" alt="Screenshot 2026-06-21 194554" src="https://github.com/user-attachments/assets/da358d4b-0fe5-4240-8b0f-aab15e1eea02" />

---

### Critic Feedback


<img width="959" height="401" alt="Screenshot 2026-06-21 194613" src="https://github.com/user-attachments/assets/f515b18c-a08e-47b3-9f22-73494d90d54f" />

---

## Sample Generated Report

A sample generated report is included in this repository:

**File:** [research_report_1782051131.md](https://github.com/user-attachments/files/29190876/research_report_1782051131.md)



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
