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

➡️ [Lab 1 Notebook](lab1_pii_redaction/Lab_1_Prompt_Engineering.ipynb)

---

### **Lab 2 — Email Phishing Classifier using LangGraph**
- Build an **agentic multi-step workflow** to classify emails as **ALLOW, INVESTIGATE, or BLOCK**.
- Agents include:
  1. Email Analyzer
  2. Threat Intelligence Checker
  3. URL Reputation Scanner
  4. Decision Coordinator
- Integrates external APIs like VirusTotal.

➡️ [Lab 2 Notebook](lab2_email_classifier/Lab_2_Email_Classifier_Using_Langraph.ipynb)

---

## 🛠️ Setup Instructions

### ​​​ Install Dependencies
Each lab has a dedicated environment file.

**Lab 1 — Prompt Engineering (PII/PCI Redaction)**  
```bash
cd lab1_pii_redaction
pip install -r requirements.txt
```  
[![Open Lab 1 in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/RitikaVerma7/DEFCON33/blob/main/lab1_pii_redaction/Lab_1_Prompt_Engineering.ipynb)

**Lab 2 — Email Classifier (Using LangGraph)**  
```bash
cd ../lab2_email_classifier
pip install -r requirements.txt
```  
[![Open Lab 2 in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/RitikaVerma7/DEFCON33/blob/main/lab2_email_classifier/Lab_2_Email_Classifier_Using_Langraph.ipynb)

>  You can also run these labs directly in **Google Colab**—just click the appropriate badge above.

---

### ​​​ Get API Keys (if applicable)
Some labs require API keys for full functionality.

| Service     | Purpose                     | Get a Key from               |
|-------------|-----------------------------|-------------------------------|
| OpenAI      | LLM-powered tasks           | [OpenAI Account](https://platform.openai.com/account/api-keys) |
| VirusTotal  | URL/domain reputation check | [VirusTotal](https://www.virustotal.com/gui/join-us)         |

Store them in a `.env` file in the lab directory:

```env
OPENAI_API_KEY=your_openai_key_here
VT_API_KEY=your_virustotal_key_here
```

---

### ​​​ Run the Notebook
- **Jupyter**: Run `jupyter notebook` in the lab directory
- **VSCode**: Open the `.ipynb` and run cells
- **Colab**: Simply click the badge and go—no setup needed
