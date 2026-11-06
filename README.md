# ✦ BIAI SmartCRM Pro
### Multilingual CRM & Sales Intelligence Workspace

**A modern, AI-assisted customer relationship management prototype built for the BIAI AI Intern — Round 2 technical assessment.**

SmartCRM Pro transforms scattered customer enquiries into an organized sales pipeline, helping teams manage conversations, monitor opportunities, and prioritize follow-ups.

**Tech Stack:** Python · Streamlit · Pandas · OpenAI API (optional) · CSV

---

## 🎯 The Problem

Customer enquiries arrive through WhatsApp, Facebook, websites, and phone calls. Without a centralized system, important conversations can be overlooked, follow-ups may be delayed, and sales teams may struggle to track potential customers.

**SmartCRM Pro provides a simple workspace to organize these enquiries and make follow-up decisions easier.**

## ✨ Key Features

### 📊 Interactive Sales Dashboard
- Overview of total enquiries and pipeline activity
- Five-stage sales pipeline: `New → Contacted → Interested → Paid / Lost`
- Visual breakdown of enquiry sources and interests
- Quick identification of active opportunities

### 📥 Enquiry Management
- Search and filter customer enquiries
- Edit customer names, phone numbers, interests, and statuses
- Add internal notes and record follow-up activity
- Export CRM records to CSV

### 🤖 Multilingual Message Assistant
- Process pasted customer messages in Bangla, Banglish, or English
- Extract available contact information and enquiry interests
- Suggest context-appropriate customer replies
- Support optional OpenAI-powered extraction and response generation

**AI transparency:** When a valid OpenAI API key is configured, the assistant can use `gpt-4o-mini`. Otherwise, it uses clearly labelled rule-based extraction and reply templates. The fallback is not presented as generative AI.

### ⏰ Follow-up Monitoring
- Identify enquiries requiring attention after 48 hours
- Highlight overdue follow-ups
- Generate a statistics-based activity summary

### 🎨 User-Friendly Interface
- Modern dashboard with custom styling
- Four organized application tabs
- Searchable tables and visual analytics
- Simple workflow for managing sales enquiries

---

## 🏗️ Application Workflow

```text
Customer Enquiry
       |
       v
Message Extraction
(AI or Rule-Based Fallback)
       |
       v
Structured CRM Record
       |
       v
Sales Pipeline
       |
       +----> Suggested Reply
       |
       +----> Follow-up Monitoring
       |
       +----> Dashboard & Reports
```

## 🛠️ Technology Stack

| Technology | Purpose |
|---|---|
| Python | Core application logic |
| Streamlit | Interactive web interface |
| Pandas | Data processing and management |
| OpenAI API | Optional AI-assisted extraction and drafting |
| CSV | Local prototype data storage |

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/shafinSI/BIAI-SmartCRM-Pro.git
cd BIAI-SmartCRM-Pro
```

### 2. Create a virtual environment

```bash
python -m venv .venv
```

On Windows PowerShell, dependencies can be installed using:

```powershell
.\.venv\Scripts\python.exe -m pip install -r requirements.txt
```

### 3. Prepare sample data

The assessment dataset is not included in this public repository.

For an authorized local run, place the BIAI-provided sample CSV at:

```text
sample-data/sample-enquiries.csv
```

The application expects the original sample dataset structure.

### 4. Launch the application

```powershell
.\.venv\Scripts\python.exe -m streamlit run app.py
```

Open `http://localhost:8501` in your browser.

### 5. Enable AI (Optional)

Enter a valid OpenAI API key in the application's sidebar or configure the `OPENAI_API_KEY` environment variable.

Without an API key, the application remains usable through its rule-based and template fallbacks.

**Never commit API keys or secrets to GitHub.**

---

## 📁 Project Structure

```text
BIAI-SmartCRM-Pro/
├── app.py
├── requirements.txt
├── README.md
├── LOOM_SCRIPT.md
├── SUBMISSION_NOTE.md
├── .gitignore
└── sample-data/           # Local only; not publicly committed
    └── sample-enquiries.csv
```

## 🧪 Dataset & Testing

Developed around the 20 fictional customer enquiries supplied for the BIAI Round 2 assessment.

The dataset contains multilingual messages and different enquiry types, providing a useful foundation for demonstrating CRM operations and message handling.

No real customer data is required.

## ⚠️ Current Limitations

- Generative AI features require a valid API key and have not been independently verified in a deployed environment.
- Without an API key, extraction uses limited keyword and regular-expression matching.
- Follow-up summaries are statistics-based rather than AI-written.
- Local CSV storage is not suitable for concurrent production users.
- Authentication, role-based access control, and direct messaging integrations are not implemented.
- AI-generated replies should be reviewed before being sent to customers.

## 🔮 Future Improvements

- PostgreSQL-backed multi-user CRM
- Secure authentication and team permissions
- More reliable Bangla and Banglish intent classification
- Structured AI output validation
- Automated follow-up notifications
- Messaging platform integrations
- AI-generated weekly sales intelligence reports
- Cloud deployment and persistent storage

---

## 🎓 Project Context

**BIAI AI Intern — Round 2 | Task 1: BIAI CRM**

Built to demonstrate practical software development, multilingual message processing, CRM workflow design, and responsible AI integration.

**Developer:** Shafin Imtiaz

**GitHub:** https://github.com/shafinSI

---

*SmartCRM Pro — From scattered enquiries to organized opportunities.*
