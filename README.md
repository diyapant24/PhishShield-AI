🛡️ PhishShield AI

Autonomous Multimodal Cyber Defence & Multilingual Scam Detection

Built for the Google AI Startup Buildhackathon

«Scams don't only speak English. Your defence shouldn't either.»

---

📌 1. Problem Overview

Digital scams are becoming increasingly sophisticated, targeting everyday internet users, businesses and financial institutions.

Traditional security solutions face several challenges:

- Deepfake Scams: Fake voices imitate family members and trusted individuals.
- Phishing Attacks: Fraudulent WhatsApp messages and payment links look genuine.
- Language Barriers: Security warnings are often difficult to understand.
- Multimodal Threats: Scams can combine suspicious text, images, links and audio.

💡 2. The Solution: PhishShield AI

PhishShield AI is an AI-powered cybersecurity platform designed to detect, analyse and explain digital threats through an intelligent multi-agent system.

It uses Google's Gemini AI technology to analyse suspicious content and generate understandable security warnings in regional languages.

🛡️ 3. Four-Step Verification Process

Step 1: Multimodal Data Ingestion

- Accepts suspicious messages, URLs, images and audio.
- Collects user-submitted content for analysis.

Step 2: AI-Powered Threat Analysis

- Gemini analyses suspicious content.
- Identifies phishing indicators and potential fraud.
- Uses RAG to retrieve relevant threat information.

Step 3: Risk Explanation

- Explains why the content may be dangerous.
- Generates understandable warnings.
- Supports multilingual communication.

Step 4: Threat Reporting

- Records suspicious activities.
- Generates threat reports.
- Supports further investigation and reporting.

✨ 4. Key Features

- 🎙️ Deepfake Voice Analysis
- 📩 Phishing Message Detection
- 🖼️ Fraudulent Image Analysis
- 🔗 Suspicious URL Detection
- 🌐 Multilingual AI Explanations
- ⚡ Fast AI-Powered Scanning
- 🚨 Threat Reporting System

---

🏗️ 5. System Architecture

PhishShield AI follows a modular frontend-backend architecture.

       USER / CLIENT
             |
             v
     FRONTEND APPLICATION
       (React / Web UI)
             |
             v
       BACKEND SERVER
       (Python / FastAPI)
             |
             v
       DATA INGESTION
    Text | Image | Audio | URL
             |
             v
       GEMINI AI ENGINE
             |
       +-----+------+
       |            |
       v            v
   RAG ENGINE   THREAT ANALYSIS
       |            |
       +-----+------+
             |
             v
      EXPLAINER AGENT
             |
             v
     MULTILINGUAL WARNING
             |
             v
      REPORTING AGENT
             |
             v
       DATABASE / LOGS
             |
             v
      RESULTS TO USER

🧠 6. AI Agent Architecture

PhishShield AI consists of four major intelligent components:

1. Multimodal Scanner

Receives and analyses suspicious text, images, audio and URLs.

2. Analyst Agent

Uses Gemini AI to examine suspicious indicators and retrieve relevant information through RAG.

3. Explainer Agent

Converts technical threat analysis into simple, understandable multilingual warnings.

4. Reporting Agent

Organises suspicious activity records and prepares incident reports.

---

☁️ 7. Google AI & Cloud Technology Stack

Technology| Implementation Purpose
Gemini 2.5 Flash| Fast AI-powered analysis
Gemini Pro| Advanced language reasoning
Gemini Live API| Real-time voice interaction
Vertex AI RAG Engine| Threat knowledge retrieval
Vertex AI Vector Search| Similarity-based threat matching
BigQuery| Threat intelligence storage and analytics
Google Cloud Run / GKE| Backend cloud deployment
React| Frontend application
Python + FastAPI| Backend and API development

Note: These technologies describe the proposed architecture. Individual cloud services and AI integrations must be configured and tested before being considered operational.

---

💻 8. Core Technical Implementation

Frontend

React + JavaScript

Provides the user interface for:

- Message scanning.
- Image and audio uploads.
- Language selection.
- Threat analysis results.

Backend

Python + FastAPI

Handles:

- User requests.
- Data ingestion.
- AI API communication.
- Response processing.
- Threat reporting.

Gemini AI Integration

Example of the message-analysis backend:

from fastapi import FastAPI
from pydantic import BaseModel
from google import genai
import os

app = FastAPI()

client = genai.Client(
    api_key=os.environ["GEMINI_API_KEY"]
)

class ScanRequest(BaseModel):
    message: str

@app.post("/scan")
async def scan(request: ScanRequest):

    prompt = f"""
    Analyse this message for phishing
    and fraudulent activities:

    {request.message}

    Identify suspicious indicators
    and recommend safety actions.
    """

    response = client.models.generate_content(
        model="gemini-2.5-flash",
        contents=prompt
    )

    return {"analysis": response.text}

This is a starter implementation of the text-scanning API.

---

📂 9. Project Structure

PhishShield-AI/
│
├── frontend/
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   ├── App.jsx
│   │   └── App.css
│   └── package.json
│
├── backend/
│   ├── main.py
│   ├── scanner.py
│   ├── gemini_ai.py
│   ├── rag_engine.py
│   ├── explainer.py
│   ├── reporting.py
│   └── requirements.txt
│
├── database/
│   └── schema.sql
│
├── docs/
│   └── architecture.md
│
├── .env.example
├── .gitignore
├── LICENSE
└── README.md

---

🚀 10. Getting Started

Prerequisites

- Python 3.10+
- Node.js 18+
- Git
- Gemini API Key

Step 1: Clone Repository

git clone https://github.com/diyapant24/PhishShield-AI.git

cd PhishShield-AI

Step 2: Configure Backend

cd backend

pip install -r requirements.txt

Create a ".env" file:

GEMINI_API_KEY=your_api_key_here

Step 3: Run Backend

uvicorn main:app --reload

Step 4: Run Frontend

Open another terminal:

cd frontend

npm install

npm run dev

These commands apply once the corresponding application files and dependencies have been added to the repository.

---

💰 11. Business Model & Go-To-Market

B2C – Business to Consumer

Starter (Free)

- Scam message scanning.
- Image checking.
- Multilingual warnings.

Shield (Premium)

- Advanced threat analysis.
- Live voice protection (when implemented).
- Threat reporting.

B2B – Business to Business

Enterprise Plan

- Team security dashboard.
- Threat intelligence.
- API integration.
- Multilingual customer support.

B2B2C – Business to Business to Consumer

Banks and telecom companies can integrate PhishShield AI into their platforms to provide security services directly to customers.

---

🎯 12. Target Users

- Everyday smartphone users.
- Senior citizens and families.
- Banks and financial institutions.
- Telecom companies.
- Businesses handling digital communication.

🌍 13. Our Vision

To make digital communication safer for everyone through intelligent, multilingual and accessible AI-powered cybersecurity.

One Platform. Multiple Languages. Stronger Digital Protection.

---

🤝 14. Contributing

Contributions from developers, AI researchers and cybersecurity enthusiasts are welcome.

How to Contribute

1. Fork this repository.
2. Create a new feature branch.
3. Make your changes.
4. Test your implementation.
5. Submit a Pull Request.

Contribution Guidelines

- Maintain clean and readable code.
- Follow coding standards.
- Test new features.
- Report bugs and suggest improvements.
- Never expose API keys or confidential information.

---

📜 15. License

This project is licensed under the MIT License.

---

👩‍💻 16. Project Information

Category| Details
Project Name| PhishShield AI
Domain| AI & Cybersecurity
AI Technology| Google Gemini
Backend| Python / FastAPI
Frontend| React
Cloud Platform| Google Cloud
Focus| Multimodal AI & Agentic Cyber Defence
Business Model| B2C, B2B & B2B2C

---

Built with the vision of making cybersecurity accessible to everyone. 🛡️