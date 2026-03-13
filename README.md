# application-tracking-system
Application Tracking System

# AI Resume Analyzer — Intelligent ATS Tracking System

An AI-powered Applicant Tracking System (ATS) that evaluates resumes against job descriptions using Natural Language Processing and Large Language Models.

The system analyzes uploaded resumes and job descriptions to compute a **JD Match Score**, detect **missing skills**, and generate **AI-powered feedback** similar to how an ATS system and Technical HR reviewer evaluate candidates.

Built using **Python, Streamlit, OpenAI GPT, LangChain, and Scikit-learn**.

---

# Demo Workflow

1. Upload Job Description (PDF)
2. Upload Resume (PDF)
3. Click Analyze
4. System generates:

- JD Match Percentage
- Position Match Recommendation
- Missing Skills
- AI Generated Resume Review
- Candidate Summary

---

# Key Features

AI Resume Evaluation  
ATS Keyword Matching  
Job Description Skill Extraction  
Position Match Recommendation  
Resume Feedback Generation  
PDF Resume Parsing  
Interactive Web Interface

---

# System Architecture
            User Uploads Files
                   │
                   ▼
            Streamlit Web UI
                   │
                   ▼
           PDF Text Extraction
               (PyPDF2)
                   │
                   ▼
        Keyword Extraction Engine
           (Scikit-Learn NLP)
                   │
                   ▼
          JD Match Score Engine
                   │
                   ▼
            OpenAI LLM Analysis
              (LangChain)
                   │
                   ▼
         Resume Evaluation Report

---

# Technology Stack

| Layer | Technology |
|-----|-----|
Frontend | Streamlit |
Backend | Python |
AI Engine | OpenAI GPT |
LLM Framework | LangChain |
NLP | Scikit-learn |
PDF Processing | PyPDF2 |
Environment Config | python-dotenv |

---

# Core ATS Matching Algorithm

The system extracts keywords from the Job Description using:

This produces a realistic approximation of **how ATS screening works**.

---

# AI Resume Analysis

After computing the ATS score, the system sends the following to the LLM:

- Job Description
- Resume Text
- JD Match Score
- Position Match Result

The AI returns:

Experience Estimate  
Missing Skills  
Overall Resume Evaluation  
Candidate Fit Assessment

---

# Position Match Logic

A resume is marked as **Position Match = Yes** when:
JD Match >= 38%

OR

All major job description skills exist in the resume.

---

# Project Structure
application-tracking-system
│
├── app.py
├── requirements.txt
├── .env
├── README.md
└── LICENSE

---

# Example Output
JD Match: 72%

Position Match: Yes

Experience: 7 years

Skills Missing:
Kubernetes
Docker
AWS

Overall Summary:
Candidate demonstrates strong backend engineering experience and good alignment with the role. Adding cloud-native technologies and container orchestration experience would strengthen the profile.
