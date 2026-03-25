# AI Financial Statement Analysis Platform

A Python-based project for analyzing financial documents using LLM-powered extraction and reasoning. The repository combines a Streamlit frontend, FastAPI backend, report generation, and supporting analytics modules (financial ratios, anomaly detection, and sentiment analysis).

## Key Features

- Upload and analyze financial files (PDF, CSV, XLSX).
- Chat interface for document-aware financial Q&A.
- AI-assisted extraction of financial insights and metrics.
- Automated PDF report generation for analysis output.
- Financial ratio utility functions for due-diligence style checks.
- Optional anomaly detection module using a VAE model.
- Optional sentiment analysis module for financial text.

## Tech Stack

- Language: Python
- Frontend: Streamlit
- Backend API: FastAPI + Uvicorn
- AI/LLM: Google Gemini APIs, LangChain integrations
- Data & Modeling: Pandas, NumPy, PyTorch, scikit-learn
- Reporting: ReportLab, Matplotlib, WeasyPrint, Jinja2

## Project Structure

```text
combine/
|-- app.py                    # Streamlit UI
|-- backend.py                # FastAPI API for chat/upload/report
|-- run.py                    # Convenience script to start services
|-- report_generator.py       # PDF report generation
|-- financial_tools.py        # Financial ratio/helper calculations
|-- anomaly.py                # VAE-based anomaly detection module
|-- sentiment_analysis.py     # Financial sentiment analysis module
|-- langchain_integration.py  # LLM workflow integrations
|-- prompts.py                # Prompt templates
|-- financial_data.csv        # Sample data
|-- requirements.txt          # Python dependencies
|-- test_report_generation.py # Basic test script
|-- vae_financial.pth         # Saved model artifact
```

## How To Run

### 1. Clone and enter the project

```bash
git clone https://github.com/Manav-Pathak/financial-doc-analyzer.git
cd combine
```

### 2. Create and activate a virtual environment

```bash
python -m venv .venv
```

Windows (PowerShell):

```bash
.\.venv\Scripts\Activate.ps1
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Configure environment variables

Create a `.env` file in the project root:

```env
GOOGLE_API_KEY=your_google_api_key
HF_TOKEN=your_huggingface_token_optional
```

If your Streamlit app expects secrets, add `.streamlit/secrets.toml`:

```toml
[google]
api_key = "your_google_api_key"
```

### 5. Start the app

Option A (recommended for this repo):

```bash
python run.py
```

Option B (manual):

```bash
uvicorn backend:app --reload
streamlit run app.py
```

Then open:

- Frontend: http://localhost:8501
- Backend: http://localhost:8000

## Demo Video



https://github.com/user-attachments/assets/3764959e-a037-4da2-a98c-d3f92d4acda3


