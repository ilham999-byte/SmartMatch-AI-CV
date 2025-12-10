SmartMatch AI 🚀

SmartMatch AI is an intelligent recruitment assistant designed to automate the screening of resumes using Generative Artificial Intelligence (LLMs). By bridging the gap between unstructured resume data and structured decision-making, this tool helps HR professionals focus on what matters most: talent acquisition.

📖 Overview
![hess1](https://github.com/user-attachments/assets/d4013deb-59c0-45d8-9e66-62c74c4d495f)

The recruitment process often faces a bottleneck at the initial screening phase. SmartMatch AI solves this by:

Centralizing Data: Using Google Forms and Google Drive as a "Data Lake".

Analyzing Content: Utilizing Large Language Models (LLM) to read and understand PDF resumes.

Scoring & Explaining: Providing a matching score against job requirements and, crucially, a textual justification for that score (Explainable AI).


✨ Key Features
1. Data Acquisition & Centralization

User-Friendly Interface: Candidates submit applications via Google Forms (accessible on any device).

Standardization: Enforces PDF format (max 10MB) and mandatory metadata (Email, Name).

Cloud Integration: Automatically syncs uploaded files to a specific Google Drive repository, triggering the analysis pipeline.

2. Intelligent Analysis (Streamlit & LLM)

![hess2](https://github.com/user-attachments/assets/290a2428-dba8-4785-ba72-0c65b7f1cd11)


Real-time Sync: The dashboard connects directly to the Cloud to retrieve new CVs.

Customizable Screening: Recruiters can define specific technical keywords (e.g., "Spring Boot, Java").

Automated Scoring: The system evaluates candidates and assigns a relevance score (e.g., 75% match).

Data Extraction: Automatically parses unstructured PDFs to extract structured data (Name, School, Key Competencies).

3. Explainable AI (XAI)

![hess3](https://github.com/user-attachments/assets/13d7feb0-4de8-4611-bdf3-ef771186e988)


Unlike "Black Box" algorithms, SmartMatch AI provides a textual justification for every score.

Example: "The candidate possesses good knowledge of Java, Spring Boot... which constitutes an asset for this post."

4. Reporting

Data Export: One-click generation of CSV reports containing all analysis data.

Compatibility: Files are ready for Excel or integration with other HR tools.

🛠️ Architecture & Tech Stack

The solution follows a modular architecture decoupling the User Interface (Data Entry) from the Processing Engine.

Frontend: Streamlit (Python-based web interface).

Backend logic: Python.

AI Engine: Llama 3.2 (Meta).

PDF Processing: PyPDF2 for text extraction.

Storage & Trigger: Google Drive & Google Forms.

🚀 Installation & Setup
Prerequisites

Python 3.8+
Ollama (if running Llama 3.2 locally)

A Google Cloud Platform project (for Drive API).

Steps

Clone the repository

git clone https://github.com/ilham999-byte/SmartMatch-AI.git

cd SmartMatch-AI

Install dependencies

pip install -r requirements.txt

Configure API Keys

Place your Google Service Account credentials JSON file in the root directory (e.g., credentials.json).

Configure your Llama 3.2 provider (e.g., Ollama URL or Groq/HuggingFace API key) in a .env file.

Run the Application

streamlit run app.py
🖥️ Usage Guide

Synchronize: Click the "Connect to Drive" button to fetch the latest resumes.

Define Requirements: Enter the job description or keywords (e.g., "Data Science, Python, NLP").

Analyze: Launch the analysis. The system will process files and display a table with:

Candidate Name

Matching Score

AI Explanation

Extracted Skills

Export: Click "Download CSV" to save the results.

🔮 Future Perspectives & Roadmap

This project is constantly evolving. Future iterations aim to implement:

Advanced Scoring: Moving from generic scoring to a nuanced 0-100 scale considering years of experience and soft skills.

Multi-Language Support: Optimization for English, French, and Arabic resumes within the same batch.

Semantic Search: Advanced filtering capabilities (e.g., "Show candidates with > 3 years experience").

LinkedIn Integration: Extending data sourcing beyond PDF uploads.

Encoding Optimization: Enhanced UTF-8-SIG support for perfect Excel compatibility with special characters.

🤝 Contributing

Contributions, issues, and feature requests are welcome! Feel free to check the issues page.

