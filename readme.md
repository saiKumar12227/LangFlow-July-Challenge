# 📊 SaaS Support Ticket Sentiment Report Automation with Langflow

Automated, explainable monthly customer support sentiment analytics for SaaS companies, fully implemented as a modular, maintainable **Langflow** project.

---

## 🚀 Overview

This project auto-generates monthly summary reports for customer support tickets, analyzing sentiment, calculating response time, and delivering formatted results via email to key stakeholders. It showcases advanced Langflow orchestration, including control flow, data transformation, custom components, optimization, and robust integration with LLMs and SMTP email.

---

## 🏆 Project Highlights

- **Zero manual steps:** End-to-end automation from file ingestion to report delivery
- **State-of-the-art LLM integration:** Dynamic ticket-by-ticket sentiment classification
- **Enterprise-ready:** Email dispatch (SMTP), robust error handling, secure key management
- **Custom components:** For response time, summary formatting, and SMTP
- **Token & component optimized:** Under 20 streamlined, maintainable Langflow nodes

---

## 💡 Problem Solved

SaaS businesses often need a recurring, actionable report on support tickets:
- How happy were customers last month?
- How fast are responses?
- Which issues dominate?

This project answers those questions—**effortlessly**.

---

## 🛠️ Architecture & Flow

Here’s how your flow handles the business challenge:

1. **Data Input**
    - Loads ticket data from `.csv` via Langflow’s File component.

2. **Data Cleaning & Preparation**
    - Cleans textual anomalies.
    - Preps each ticket for LLM analysis.

3. **Loop and Sentiment Analysis**
    - Loops over each ticket.
    - Uses a prompt template to pass structured ticket info to an LLM (Google Gemini, OpenAI, Anthropic, etc.) for *consistent* Positive/Neutral/Negative classification.

4. **Result Integration**
    - Converts LLM output (JSON) into a DataFrame, adding sentiment as a new column.

5. **Response Time Calculation (Custom Component)**
    - Calculates days between ticket open & close, appending to the DataFrame.

6. **Report Formatting (Custom Component)**
    - Aggregates ticket count, average response time, and counts per sentiment.
    - Composes perfectly formatted Markdown for email.

7. **Email Sending (Custom SMTP Component)**
    - Emails the report to stakeholders—configurable for any SMTP provider.

8. **End-to-End Orchestration**
    - All steps chained via modern, non-legacy Langflow components.
    - Designed for minimal token usage, high parallelization, and error resilience.

---

## 🔩 Custom Components

**Response Time Calculator:** Adds `response_time_days` column based on open/close dates.  
**Ticket Summary Formatter:** Returns subject/body as Markdown, ready for email dispatch.  
**SMTP Email Sender:** Secure, generic sender compatible with Gmail, Outlook, etc.

---

## 🎯 Key Features for Recruiters & HR

- **Modern workflow orchestration**—leverages latest-gen LLMs and data tools
- **Reusable components & modularity**—built for adaptability and scaling
- **Pro-grade automation**—error handling, logging, and security built in
- **No vendor lock**—works with any ticket input, any SMTP

---

## 👩‍💻 Tech Stack

- **Langflow** (v1.5+)
- **Python** (for custom nodes)
- **LLM Providers:** Google Gemini, OpenAI GPT, Anthropic, or free OpenRouter
- **Pandas**—data manipulation in custom components

---
## 📂 Files Included

- `Langflow-tickets-sentiment-aggregator.json` – Fully configured Langflow flow
- `README.md` (this file)

---

## 🔒 Security/Privacy

- SMTP credentials are parameterized and never hardcoded in artifacts.
- API keys are managed securely via Langflow’s secret inputs.
- Data stays local; can be easily adapted for GDPR/PII-sensitive environments.

---

## ✅ How to Run (Quickstart)

1. Install [Langflow](https://docs.langflow.org/)
2. Import the JSON flow via the Langflow UI.
3. Configure:
    - File path(s) to your support tickets CSV
    - LLM API key (for Google, OpenAI, etc.)
    - SMTP credentials
    - Email recipients
4. Run the flow
5. Check your inbox for a formatted summary report!

---

## 🌟 Why This Stands Out

- **Production-grade**: Handles real-world messy data, missing values, and date issues.
- **Minimal effort, maximal insight**: Useful for non-technical managers and product leaders.
- **Showcases advanced LLM operations**: Looping, prompt design, structured output, DataFrame integration.

---

## 🔗 More

- Find me on Discord: **sai12215135**
- Email: [chsaikumar1227@gmail.com](mailto:chsaikumar1227@gmail.com)
- [Langflow Docs](https://docs.langflow.org/)

---

## 📣 Looking for a Data/AI Automation Engineer?

Let’s talk! My portfolio goes beyond demos; I engineer scalable, maintainable, and explainable solutions that deliver business insight with no hand-holding.  

*Clone, reuse, or reach out for a walkthrough!*

> **Note:** This project is designed for demonstration and portfolio purposes. Adjust SMTP/email credentials and input datasets as needed for live use.