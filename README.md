# 🎯 JobFit AI

> **Hackathon Project** — Instantly analyze how well your resume matches a job description.

[![Streamlit App](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](https://streamlit.io)

---

## ✨ Features

| Feature | Details |
|---|---|
| **Match Score (0–100%)** | AI-powered fit score with color-coded verdict |
| **Gap Analysis** | Matched / Partial / Missing skills + experience gaps |
| **Cover Letter** | Auto-generated, editable, company-specific letter |
| **Download Report** | One-click `.docx` with everything + resume |

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
git clone https://github.com/<your-username>/jobfit-ai.git
cd jobfit-ai
```

### 2. Install dependencies
```bash
pip install -r requirements.txt
```

### 3. Set your Anthropic API key

**Option A — Streamlit secrets (recommended for Streamlit Community Cloud)**

Create `.streamlit/secrets.toml`:
```toml
ANTHROPIC_API_KEY = "sk-ant-..."
```

**Option B — Environment variable**
```bash
export ANTHROPIC_API_KEY="sk-ant-..."
```

### 4. Run
```bash
streamlit run app.py
```

---

## ☁️ Deploy on Streamlit Community Cloud

1. Push this repo to GitHub
2. Go to [share.streamlit.io](https://share.streamlit.io) → **New app**
3. Select your repo and `app.py`
4. Under **Advanced settings → Secrets**, add:
   ```
   ANTHROPIC_API_KEY = "sk-ant-..."
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
- **AI Engine**: [Anthropic Claude](https://anthropic.com) (`claude-sonnet-4`)
- **Report Generation**: `python-docx`

---

## 📄 License

MIT — free to use, modify, and distribute.
