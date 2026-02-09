# STARK – Student Advising & Resource Knowledge Platform

STARK is an AI-powered academic and career assistance platform designed to help students with advising, resume analysis, skill gap identification, FAQs, event discovery, and job matching. The platform integrates multiple datasets, LLM-powered responses, and a unified dashboard to deliver personalized and contextual student support.

---

## Overview

STARK serves as a centralized student support system by combining academic data, career resources, and AI-driven insights into a single platform. It assists students throughout their academic journey—from course planning to career readiness.

---

## Features

### AI Chatbot
- Answers student FAQs using a fine-tuned large language model (LLM)
- Provides academic guidance, course clarification, and general queries
- Uses contextual information from university datasets

### Resume Analyzer
- Extracts key skills, experience, and ATS-relevant metrics from resumes
- Generates job match scores against job descriptions
- Suggests improvements to enhance ATS compatibility

### Skill Gap Assessment
- Compares student profiles with job descriptions
- Identifies missing or weak skills
- Recommends relevant courses, clubs, or activities

### Career & Academic Data Integration
- Uses CSV-based datasets, including:
  - Advising notes
  - Course catalog
  - Jobs and events
  - Clubs and announcements
  - Student profile data
- Supports SQLite database storage (`stark.db`)

### Student Dashboard (Web Interface)
- Built using HTML and CSS
- Includes:
  - Role-based login previews
  - Live chatbot previews
  - Integrated student portal UI mockups

### Utility Modules
- Automated database initialization and seeding
- Context injection for LLM responses
- Data preprocessing and cleaning scripts

---

## Project Structure

```text
STARK/
│
├── app.py
├── main_chatbot.py                  # Backend orchestrator & chatbot logic
├── resume_analyzer_integrated.py    # Resume & ATS analysis
├── summary_module.py                # Summarization and NLU helpers
├── stark_context.py                 # Knowledge base and system prompts
├── ats_checker_updated.py
├── student_faq_chatbot_llm.py
├── init_db.py                       # Database initialization
├── seed_more_data.py                # Populate database with datasets
├── stark.db                         # SQLite database (if present)
│
├── data/                            # CSV datasets
│   ├── advising_notes.csv
│   ├── ats_jobs.csv
│   ├── career_data.csv
│   ├── chat_logs.csv
│   ├── resumes_index.csv
│   └── ... (additional datasets)
│
├── index.html
├── stark_full_spa.html              # Full portal mockup
├── stark_agent_live_preview.html
├── stark_ai_portal_role_based_login_dashboards.html
│
├── notes/                           # Development notes
└── README.md

---

## Getting Started

### Prerequisites
- Python 3.8+
- pip

---

### Installation

Install the required dependencies:

```bash
pip install -r requirements.txt
You can generate the requirements.txt file using:
pip freeze > requirements.txt

Initialize the Database
Initialize the SQLite database:
python init_db.py
Skip this step if stark.db already exists.

Run the Application
Start the application:
python app.py

