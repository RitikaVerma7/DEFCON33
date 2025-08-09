# Lab 1 — Prompt Engineering for Security Tasks

## 📝 Overview
This lab demonstrates how to use **prompt engineering** and lightweight NLP tooling to perform security-related text processing, including:
- **CVE extraction** from noisy logs.
- **Secure code review** with GenAI.
- **PII/PCI redaction** using `spaCy`, regex, and DSPy.

The focus is on **crafting effective prompts** and integrating them with targeted tools to improve accuracy, reduce hallucinations, and enforce secure output formats.

---

## 📂 Files in This Lab
| File | Description |
|------|-------------|
| `Lab_1_Prompt_Engineering.ipynb` | Main notebook for the lab |
| `sample_inputs.txt` | Example text for testing (logs, code, PII) |

---

## 💡 Things to Try

### 1️⃣ CVE Extraction from Noisy Logs
- Modify the prompt to return CVE IDs with **context** (e.g., surrounding log lines).
- Ask the LLM to **group CVEs by year** or tag them with **risk levels**.
- Try feeding logs in **different formats** (CSV, JSON lines, etc.).
- Introduce **noise or obfuscation** in the log — does the LLM still detect CVEs?

### 2️⃣ Secure Code Review with GenAI
- Change the code snippet to include **multiple vulnerabilities** (e.g., hardcoded secrets + SQL injection).
- Ask for **line numbers** where vulnerabilities occur.
- Change the output format to **YAML** or **Markdown** (simulate report generation).
- Add a prompt variant that asks the model to **write unit tests** for the fixed code.
- Remove part of the prompt — observe changes in **precision**.

### 3️⃣ PII Redaction with spaCy + Regex
- Extend regex patterns to detect:
  - IPv4 / IPv6 addresses
  - Credit card numbers
  - API keys or tokens
- Visualize **redacted vs original** text side-by-side.
- Introduce **edge cases** like misformatted phone numbers or emails.
- Integrate into a **streaming input** (chat-style redaction).

### 4️⃣ PII Redaction with DSPy
- Modify the DSPy signature to also return **reasoning steps** for each PII detected.
- Add a **confidence score** for PII type detection.
- Use DSPy with a **different LLM backend** (e.g., `lm="openai/gpt-4"`).
- Combine DSPy with **Guardrails** to enforce JSON validation.

---

## 🔗 References
- [spaCy Named Entity Recognition](https://spacy.io/usage/linguistic-features#named-entities)
- [Regex101](https://regex101.com/)
- [OpenAI API Docs](https://platform.openai.com/docs/)
- [DSPy Documentation](https://github.com/stanfordnlp/dspy)
