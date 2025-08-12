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