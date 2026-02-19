# 🤖 AI Resume Screener  
### Automated Candidate Evaluation Workflow (n8n + Gemini AI)

The **AI Resume Screener** is a fully automated HR recruitment assistant built using **n8n** and **Google Gemini AI**.

It automates the resume screening process by analyzing candidate resumes against job descriptions, assigning a structured score, and logging results in real time to Google Sheets — significantly reducing manual screening effort.

---

## 📘 Project Overview

Manual resume screening:
- Is time-consuming  
- Does not scale efficiently  
- May introduce unconscious bias  

This workflow automates candidate evaluation from submission to final decision logging.

---

## ⚙️ Workflow Summary

1. **Candidate Form Submission**  
   Candidate submits Name, Email, Resume (PDF), and Job Role via n8n form.

2. **Resume Storage (Google Drive)**  
   Resume is automatically uploaded to a designated Google Drive folder.

3. **PDF Text Extraction**  
   Resume content is extracted for AI analysis.

4. **Job Description Retrieval**  
   The relevant job description is fetched from Google Sheets based on selected role.

5. **AI Evaluation (Gemini API)**  
   The Gemini model:
   - Compares resume skills with job requirements  
   - Assigns a score (0–10)  
   - Generates a structured summary  

   **Scoring Rule:**
   - 7 or above → ✅ Qualified  
   - Below 7 → ❌ Unqualified  

6. **Result Logging**  
   Candidate name, role, score, status, and summary are appended to Google Sheets for HR review.

---

## 🧠 AI Evaluation Logic

- Matches required skills with resume content  
- Deducts points for missing or unclear requirements  
- Generates:
  - Numerical score  
  - Qualification decision  
  - Justification summary  

Ensures consistent, objective screening.

---

## 🧩 Tech Stack

- **n8n** – Workflow automation  
- **Google Drive API** – Resume storage  
- **Google Sheets API** – JD storage & result logging  
- **Google Gemini API** – AI resume analysis  
- **Extract PDF Node** – Resume parsing  

---

## 🔗 Workflow Architecture

Form Trigger  
↓  
Upload Resume to Drive  
↓  
Extract PDF Text  
↓  
Fetch Job Description  
↓  
Filter Matching Role  
↓  
Gemini AI Evaluation  
↓  
Format Result  
↓  
Append to Google Sheets  

---

## 📊 Example Output

| Date       | Candidate        | Role  | Score | Status     | Summary |
|------------|-----------------|-------|-------|------------|---------|
| 2025-10-21 | Priyank Singh   | Sales | 7     | Qualified  | Resume matches 80% of required skills; missing CRM expertise. |

---

## 💡 HR Benefits

- ✅ Instant resume evaluation  
- ✅ Reduced manual workload  
- ✅ Objective scoring  
- ✅ Centralized application tracking  
- ✅ Scalable for high-volume hiring  

---

## 🚀 Future Enhancements

- Gmail/Slack notification integration  
- AI-generated feedback emails  
- HR approval stage before final decision  
- Analytics dashboard (Looker Studio / Power BI)  
- Multi-role recruitment support  



### 👨‍💼 Author
**Sameer Kashyap**  
AI Automation Enthusiast | No-Code Developer | Building intelligent workflow systems  
📧 kashyapsameer731@gmail.com  
🔗 [LinkedIn](https://linkedin.com)

---

## ⭐ Support

If you find this project useful, consider giving it a ⭐ on GitHub.
