# Medical Content Quality Checker (Streamlit Demo)

A tiny demo to showcase AI-assisted medical text review for:
- Medical factuality checks
- Compliance & risk detection (misleading/exaggerated/forbidden claims)
- Patient readability scoring & rewrite suggestions

> ⚠️ Disclaimer: This tool is for demo and research purposes. It does not replace licensed medical professionals or formal compliance review.

## Quick Start

### 1) Setup
```bash
git clone https://github.com/fjanna/medical-content-quality-checker.git
cd medical-content-quality-checker
python -m venv .venv
source .venv/bin/activate  # Windows PowerShell: .venv\Scripts\Activate.ps1` 
pip install -r requirements.txt
### 2) Enable LLM
export OPENAI_API_KEY="**sk-替换成你自己的Key**"
# Optional model override (默认 gpt-4o-mini)
export OPENAI_MODEL="gpt-4o-mini"
streamlit run app.py
