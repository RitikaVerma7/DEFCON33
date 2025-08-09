# 🛡️ DEF CON 33 Workshop — Building Lightweight Security Tools with LLMs

Welcome!  
This repo contains all notebooks, sample data, and instructions for DEF CON 33 workshop:  
**"Building Lightweight Security Tools with Agentic LLM Workflows"**.

The workshop focuses on building **two real-world, lightweight AI-powered security tools** using Python, spaCy, DSPy, and LangGraph.

---

## 📂 Labs Overview

### **Lab 1 — PII/PCI Redaction using spaCy + DSPy**
- Detect Personally Identifiable Information (PII) and Payment Card Information (PCI) in text.
- Automatically redact sensitive data before passing it to an LLM.
- Compare **NER-based detection (spaCy)** vs **structured prompting (DSPy)**.

➡️ [Lab 1 Notebook](lab1_pii_redaction/Lab1_PII_Redaction.ipynb)

---

### **Lab 2 — Email Phishing Classifier using LangGraph**
- Build an **agentic multi-step workflow** to classify emails as **ALLOW, INVESTIGATE, or BLOCK**.
- Agents include:
  1. Email Analyzer
  2. Threat Intelligence Checker
  3. URL Reputation Scanner
  4. Decision Coordinator
- Integrates external APIs like VirusTotal.

➡️ [Lab 2 Notebook](lab2_email_classifier/Lab2_Email_Classifier.ipynb)

---

## 🛠️ Setup Instructions

1. **Clone the repo**
   ```bash
   git clone https://github.com/<yourusername>/defcon-lightweight-security-tools.git
   cd defcon-lightweight-security-tools
