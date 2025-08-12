# SSL-AI-Scanner

**AI-powered SSL/TLS Health Scanner** — scans a domain with `sslyze`, summarizes risks, and produces a technical report (engineers) + plain-language report (execs).

### Features
- Protocol support (TLS 1.0/1.1/1.2/1.3), cipher groups, cert validity/chain.
- Clear risk ratings with impact & remediation steps.
- Optional LLM explanations (Ollama/OpenAI/Gemini); offline rule-based fallback.
- Outputs **Markdown + HTML** (PDF can be added later if you install a renderer).

---

## Quickstart (Windows)

1. **Python** 3.11+ installed and on PATH.


2. Create & activate venv:
```powershell
   py -3.11 -m venv .venv
   .\.venv\Scripts\Activate.ps1 

```
3. Install:
```
pip install -U pip
pip install -e .

```

4. Scan a site and generate reports:

````
sslai scan example.com --out out

````

This writes:

out/technical_report.md & out/technical_report.html

out/executive_report.md & out/executive_report.html

5. (Optional) Run the web UI:

`` 
sslai web --host 127.0.0.1 --port 8000
``

Open http://127.0.0.1:8000

6. (Optional) Enable AI explanations:

  *Local (Ollama):
``  
MODEL_PROVIDER=ollama
MODEL_NAME=llama3.1
``
  *OpenAI:``  
MODEL_PROVIDER=openai
OPENAI_API_KEY=sk-...
``
  *Gemini:``  MODEL_PROVIDER=gemini
GEMINI_API_KEY=...
``