# BIAI SmartCRM — Submission Note

I built a lightweight CRM prototype using the 20 fictional enquiries supplied in the BIAI Round 2 pack. The application displays a five-stage sales pipeline (New, Contacted, Interested, Paid, Lost), lets users edit and track each enquiry, and highlights leads that have not been followed up in 48 hours. It also includes a message assistant to extract customer details and suggest a language-appropriate reply.

**AI tools:** I used ChatGPT to assist with application design, implementation and documentation. The running app supports OpenAI's `gpt-4o-mini` for structured extraction and reply drafting when configured with an API key. Without a key, it explicitly uses rule-based and template fallbacks rather than presenting those as AI. Outputs should be checked by a person before use.

**Limitations:** This is a local prototype with CSV storage, no login, no multi-user support, and no integration for sending real messages. Message extraction is imperfect, especially without an API key.

**Next steps:** Add a database, user authentication, structured validation and audit logs, stronger multilingual testing, and a secure messaging integration.

*Before submitting, edit this note to accurately reflect the tools you actually used and features you tested.*
