# Lab 2 — Agentic Email Classifier Using LangGraph

## 📝 Overview
This lab demonstrates how to build an **agentic multi-step workflow** for email classification using **LangGraph**.  
The system uses multiple specialized agents to analyze email content, check URL reputation, perform threat intelligence lookups, and make a final decision on whether to allow, investigate, or block an email.

We explore how to:
- Design an **agentic framework** with modular steps.
- Combine **LLM reasoning** with structured data checks.
- Integrate external threat intelligence into the decision process.

---

## 📂 Files in This Lab
| File | Description |
|------|-------------|
| `Lab_2_Email_Classifier_Using_Langraph.ipynb` | Main notebook for the lab |
| `sample_emails.json` | Test email dataset (phishing + benign cases) |

---

## 💡 Things to Try

### 🟢 Starter Variants (Beginner-Friendly)
- Change **email examples** to see how the system responds.
- Modify **risk thresholds** for classifying phishing vs. safe.
- Swap out URLs in test cases to trigger different reputation checks.
- Print **only the final decision** instead of all agent steps for a minimal output.
- Add **emoji indicators** for risk levels (✅ safe, ⚠ investigate, 🚨 phishing).

### 🚀 Advanced Variants (Deeper Exploration)
Explore ways to extend, stress-test, or productionize your agentic email classifier:

#### 🔁 Workflow Variants
- Run agents in **parallel** (e.g., URL reputation + LLM reasoning simultaneously).
- Add a **Human-in-the-Loop (HITL)** checkpoint before acting on high-risk emails.
- Insert a **guardrails agent** to validate output format, tone, or confidence.

#### ✍️ Prompt Engineering Variants
- Ask the model: *"Why might this be phishing?"* to elicit reasoning chains.
- Use **few-shot prompts** with known phishing patterns (BEC, invoice scams).
- Force structured output in **JSON**, **Markdown**, or **tagged evidence** with confidence scores.

#### 🔗 External Threat Validation
- Add a **WHOIS domain age lookup** to detect newly registered domains.
- Integrate with **PhishTank**, **AbuseIPDB**, or a custom threat intelligence feed.
- Flag inconsistencies like **display name ≠ email domain** or suspicious reply-to headers.

---

## 🔗 References
- [LangGraph Documentation](https://www.langchain.com/langgraph)
- [WHOIS Lookup](https://whois.domaintools.com/)
- [PhishTank API](https://phishtank.org/developer_info.php)
- [AbuseIPDB API](https://docs.abuseipdb.com/)
