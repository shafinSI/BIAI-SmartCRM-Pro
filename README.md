# BIAI SmartCRM — Round 2 Task 1

A Streamlit CRM built with the **20 fictional sample enquiries provided by BIAI**. Supports stage tracking, editing, optional LLM-assisted extraction and language-matched replies, and a 48-hour follow-up monitor.

## Run locally

```powershell
py -m venv .venv
.\.venv\Scripts\Activate.ps1
pip install -r requirements.txt
streamlit run app.py
```

Open the local URL shown by Streamlit (usually http://localhost:8501).

## AI configuration

Paste an OpenAI API key into the app sidebar, or set the `OPENAI_API_KEY` environment variable. AI extraction and drafting call `gpt-4o-mini`. Without a key, the app **does not claim to use AI**: it uses labelled keyword/regex extraction and response templates. Review all outputs before sending. API usage may incur charges.

## Data and persistence

Only the supplied sample CSV is bundled. The app writes edits to `crm_data.csv` locally. Use the sidebar reset to restore original data. This is a prototype, not production-ready. Do not upload real customer information.

## Known limitations

- Message extraction without an API key is limited to keyword matching and phone regex.
- AI-generated content can be incorrect; human verification is necessary.
- No authentication, role-based permissions, hosted database, or outbound WhatsApp integration.
- Follow-up timestamps are interpreted in the local machine timezone.
- CSV persistence is unsuitable for multiple concurrent users; a database is the next step.

## Next steps

Add SQLite/PostgreSQL, authentication, reliable language classification, stronger structured validation, audit history, and an authorized messaging integration.
