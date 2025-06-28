# ⚙️ Automating Manual Workflows on [Client's Platform]

> **Role:** Data Scientist / Automation Engineer  
> **Tech Stack:** Python, Pandas, FastAPI, Platform APIs  
> **Published:** 26 Feb, 2025

---

## 🧾 Project Overview

This project was about saving **time and sanity**.

Our client had two critical but painfully manual workflows on their internal platform. These jobs required multiple steps — preparing data, formatting it, and submitting payloads — and were being done **manually**, often taking **days to complete**.

I helped automate both workflows end-to-end by using the platform’s APIs and turning the process into **10-minute jobs**, triggered via **FastAPI endpoints**.

---

## 🧩 The Manual Pain Points

Each job had similar bottlenecks:

1. Analysts would extract platform data, clean it manually in Excel  
2. They’d format it to match required payload structures  
3. Submit data in chunks (through web interface or ticket)  
4. Repeat until complete (sometimes over 1–2 days per job)

It was slow, error-prone, and impossible to scale as volume grew.

---

## ⚡ Our Automation Strategy

We approached this with a clean and modular automation pipeline:

- ✅ **Data Preparation with Pandas**  
   - Loaded and cleaned raw data  
   - Mapped it to required fields using dictionary lookups and rules  
   - Generated API-ready payloads in batchable chunks

- ✅ **Platform Integration via API**  
   - Reverse-engineered API patterns from the platform  
   - Authenticated and hit the relevant endpoints in controlled batches  
   - Handled rate limits, retries, and logging

- ✅ **FastAPI Service Layer**  
   - Built simple REST endpoints (`/run-job-1`, `/run-job-2`) to trigger both automations  
   - Allowed scheduling, testing, and extensibility from day one

---

## ⏱️ Results

- 🔄 **Two formerly manual jobs are now fully automated**
- 🕒 **Each runs in under 10 minutes** — down from 1–2 days
- ✅ **Zero manual intervention required**
- 📉 Reduced errors and improved consistency across submissions
- 📈 Freeed up analysts to focus on meaningful work instead of formatting spreadsheets

---

## 🛠 Tools & Stack

| Area               | Tools / Libraries           |
|--------------------|-----------------------------|
| Data Transformation | Pandas, NumPy               |
| API Interaction     | `requests`, batch processing logic  
| API Hosting         | FastAPI                     |
| Auth / Secrets      | `.env`, platform tokens     |
| Logs / Retry Logic  | Custom status + retry hooks |

---

## 🧠 What I Learned

- How to navigate and leverage poorly documented APIs  
- How small automations can have **huge business impact**  
- The value of thinking like an engineer *and* a user when designing automation  

---

> ⚠️ **Note**: No client-specific code or credentials are shared in this repo. This documentation exists to outline the solution and its results for portfolio purposes.
