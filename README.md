# AI Career Copilot

**An AI-powered resume analysis tool that compares a resume with a job description and provides actionable feedback.**

[![Live Demo](https://img.shields.io/badge/Live%20Demo-Open%20App-brightgreen)](https://ai-career-copilot-8kys.onrender.com/)
[![Python](https://img.shields.io/badge/Python-3.x-blue)](https://www.python.org/)
[![Flask](https://img.shields.io/badge/Flask-Web%20App-black)](https://flask.palletsprojects.com/)
[![Powered by Gemini](https://img.shields.io/badge/AI-Google%20Gemini-4285F4)](https://ai.google.dev/)

## Live Demo

**Try the app:** https://ai-career-copilot-8kys.onrender.com/

Paste your resume and a target job description to receive an estimated match score and tailored suggestions for improving your application.

## Overview

AI Career Copilot is a Flask web application built to help job seekers understand how closely their resume aligns with a role. It sends the supplied resume and job description to Google's Gemini API and displays a structured analysis.

The match score is an **AI-generated estimate**, not an official score from a commercial Applicant Tracking System (ATS), and should be used as guidance rather than a hiring prediction.

## Features

- **Resume-to-job comparison** — evaluates the resume against a supplied job description.
- **Estimated ATS match score** — provides a score from 0 to 100.
- **AI summary** — gives a concise assessment of the candidate's fit.
- **Strengths** — highlights relevant skills, projects, and experience found in the resume.
- **Missing keywords** — identifies relevant terms from the job description that may be absent.
- **Improvement suggestions** — recommends practical ways to make the resume more relevant.
- **Web interface** — enter the resume and job description and view results in the browser.

## Technology Stack

- **Language:** Python
- **Backend:** Flask
- **AI:** Google Gemini API
- **HTTP requests:** Requests
- **Configuration:** python-dotenv
- **Production server:** Gunicorn
- **Frontend:** HTML, CSS, and JavaScript
- **Deployment:** Render
- **Version control:** Git and GitHub

## How It Works

1. The user enters resume text and a job description.
2. The Flask backend validates the submitted text.
3. The backend sends the content to the Gemini API with instructions to return a structured analysis.
4. The application validates the response and returns the analysis to the frontend.
5. The interface displays the estimated match score, summary, strengths, missing keywords, and improvement suggestions.

## Project Structure

```text
ai-career-copilot/
├── app.py
├── requirements.txt
├── .gitignore
└── templates/
    └── index.html
```

The `.env` file is used for local configuration and should **not** be committed to GitHub.

## Run Locally

### 1. Clone the repository

```bash
git clone https://github.com/pujalokku49-stack/ai-career-copilot.git
cd ai-career-copilot
```

### 2. Create and activate a virtual environment (recommended)

**Windows PowerShell:**

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Configure your Gemini API key

Create a `.env` file in the project root:

```text
GEMINI_API_KEY=your_gemini_api_key_here
```

Replace the placeholder locally with your own API key. **Never commit `.env` or share your API key publicly.**

### 5. Start the development server

```bash
python app.py
```

Open http://127.0.0.1:5000/ in your browser.

## Deploy on Render

This project can be deployed as a Render Web Service connected to the GitHub repository.

- **Build command:** `pip install -r requirements.txt`
- **Start command:** `gunicorn app:app`
- **Environment variable:** `GEMINI_API_KEY` — set its value in Render's environment settings. Do not put the secret in source code or the README.

## Security and Responsible Use

- Keep API keys in environment variables; never commit `.env`.
- Review Git status before pushing changes to ensure secrets are not staged.
- Resume content can contain personal information. Only submit information you are comfortable processing through the app and its AI provider.
- Suggestions are AI-generated and can be incomplete or incorrect. Review them before changing a resume.
- Add skills, tools, and achievements only when they accurately reflect your experience.
- The score is an estimate for guidance and is not an official ATS score or a guarantee of an interview.

## Future Improvements

Potential next steps include:

- PDF/DOCX resume upload and text extraction.
- Downloadable analysis reports.
- More robust validation and error handling.
- Unit and integration tests.
- Optional analysis history with clear privacy controls.
- Improved accessibility and mobile responsiveness.

## Author

**Puja Lokku**  
ApnoAI AI/ML Intern

- **GitHub:** https://github.com/pujalokku49-stack/
- **Live Project:** https://ai-career-copilot-8kys.onrender.com/

---

If you find this project useful, consider starring the repository.
