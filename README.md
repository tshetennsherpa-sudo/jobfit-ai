# 🎯 JobFit AI
## Live Site: https://jobready-ai.streamlit.app/
> **Hackathon Project** — Instantly analyze how well your resume matches a job description.

[![Streamlit App](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](https://jobready-ai.streamlit.app/)

---

## ✨ Features
| Feature | Details |
|---|---|
| **Match Score (0–100%)** | AI-powered fit score with color-coded verdict |
| **Gap Analysis** | Matched / Partial / Missing skills + experience gaps |
| **Cover Letter** | Auto-generated, editable, company-specific letter |
| **Download Files** | 3 separate `.docx` files — report, cover letter & resume |
| **Application Tracker** | Save applications to Supabase — persists across sessions |

### Score Legend
| Score | Verdict |
|---|---|
| **≥ 80%** | 🚀 Apply Immediately! |
| **60–79%** | 🤔 Consider Carefully |
| **< 60%** | ⚠️ Significant Gaps |

---

## 🚀 Quick Start

### 1. Clone
```bash
git clone https://github.com/tshetennsherpa-sudo/jobfit-ai.git
cd jobfit-ai
```

### 2. Install dependencies
```bash
pip install -r requirements.txt
```

### 3. Set your API keys
Create `.streamlit/secrets.toml`:
```toml
GEMINI_API_KEY = "your-gemini-api-key"
SUPABASE_URL = "https://your-project-id.supabase.co"
SUPABASE_KEY = "your-supabase-anon-key"
```

> 🔑 Get your free Gemini API key at [aistudio.google.com](https://aistudio.google.com)
> 🗄️ Get your free Supabase project at [supabase.com](https://supabase.com)

### 4. Set up Supabase table
Create a table called `applications` with these columns:

| Column | Type |
|---|---|
| `id` | int8 (primary key, auto) |
| `created_at` | timestamp (auto) |
| `company` | text |
| `applicant` | text |
| `score` | int2 |
| `status` | text |
| `notes` | text |
| `date_applied` | date |

### 5. Run
```bash
streamlit run app.py
```

---

## ☁️ Deploy on Streamlit Community Cloud

1. Push this repo to GitHub
2. Go to [share.streamlit.io](https://share.streamlit.io) → **New app**
3. Select your repo and `app.py`
4. Under **Advanced settings → Secrets**, add:
   ```toml
   GEMINI_API_KEY = "your-gemini-api-key"
   SUPABASE_URL = "https://your-project-id.supabase.co"
   SUPABASE_KEY = "your-supabase-anon-key"
   ```
5. Click **Deploy** 🎉

---

## 🗂️ Project Structure
```
jobfit-ai/
├── app.py               # Main Streamlit application
├── requirements.txt     # Python dependencies
├── .streamlit/
│   └── secrets.toml     # (local only, gitignored)
└── README.md
```

---

## 🛠️ Tech Stack
- **Frontend/Backend**: [Streamlit](https://streamlit.io)
- **AI Engine**: [Google Gemini](https://aistudio.google.com) (`gemini-2.5-flash`)
- **Database**: [Supabase](https://supabase.com) (PostgreSQL)
- **Report Generation**: `python-docx`

---

## 📄 License
MIT — free to use, modify, and distribute.
