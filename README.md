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

### 2️⃣ Install Dependencies
Each lab has its own environment file.

**Lab 1 — PII/PCI Redaction**
```bash
cd lab1_pii_redaction
pip install -r requirements.txt
```
[![Open Lab 1 in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://github.com/RitikaVerma7/DEFCON33/blob/main/lab1_pii_redaction/Lab_1_Prompt_Engineering.ipynb)

**Lab 2 — Email Classifier**
```bash
cd ../lab2_email_classifier
pip install -r requirements.txt
```
[![Open Lab 2 in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/RitikaVerma7/DEFCON33/blob/main/lab2_email_classifier/Lab_2_Email_Classifier_Using_Langraph.ipynb)

> 💡 You can also run these labs in **Google Colab** without local installation. Just click the badge above for your chosen lab.

---

### 3️⃣ Get API Keys (if applicable)
Some labs require API keys for full functionality.

| Service      | Purpose                     | Link to Get Key |
|--------------|-----------------------------|-----------------|
| OpenAI       | LLM-powered tasks           | [Get API Key](https://platform.openai.com/account/api-keys) |
| VirusTotal   | URL/domain reputation check | [Get API Key](https://www.virustotal.com/gui/join-us) |

Store your keys in a `.env` file in the lab’s root folder:
```env
OPENAI_API_KEY=your_openai_key_here
VT_API_KEY=your_virustotal_key_here
```

---

### 4️⃣ Run the Notebook
- **Jupyter**: Launch with `jupyter notebook`
- **VSCode**: Open and run cells directly
- **Colab**: Click the badge above and run in the browser

