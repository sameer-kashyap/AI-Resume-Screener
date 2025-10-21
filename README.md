# 🤖 AI Resume Screener – Automated Candidate Evaluation Workflow (n8n + Gemini AI)

### 📘 Overview
The **AI Resume Screener** is a fully automated **HR recruitment assistant** built using **n8n** and **Google Gemini AI**.  
It automates the **resume screening process**, scoring each candidate against a job description, and logs results in real time to Google Sheets — eliminating hours of manual effort for HR professionals.

---

### ⚙️ Workflow Summary
1. **Candidate Form Submission**  
   A candidate fills an **n8n form** (Name, Email, Resume upload, and Job Role).

2. **Google Drive Upload**  
   The submitted resume (PDF) is automatically uploaded to a designated Drive folder.

3. **Resume Extraction**  
   The workflow extracts text from the PDF for AI analysis.

4. **Job Description Fetch**  
   Based on the selected role, the corresponding job description is retrieved from Google Sheets.

5. **AI Screening (Gemini API)**  
   The Gemini model analyzes the candidate’s resume against the job description using a scoring logic (0–10 scale).  
   - 7 or above → **Qualified**  
   - Below 7 → **Unqualified**

6. **Result Logging**  
   The summary, score, and status are appended to a Google Sheet for easy HR review.

---

### 🧠 AI Logic (Gemini Prompt)
The model compares every skill and qualification in the job description with the candidate’s resume.  
- Missing or unclear requirements lead to point deductions.  
- Provides a **summary justification** and a **quantitative score**.  

This ensures unbiased and consistent screening.

---

### 🧩 Tech Stack
- **n8n** – Workflow automation platform  
- **Google Drive API** – Resume storage  
- **Google Sheets API** – Job data + log management  
- **Google Gemini API** – Resume analysis  
- **Extract PDF Node** – Text extraction from resumes  

---

### 💡 How HR Benefits
✅ **Saves time** – Automates resume screening instantly after submission  
✅ **Objective evaluation** – Removes human bias through AI scoring  
✅ **Centralized dashboard** – HRs can track every application via Google Sheets  
✅ **Scalable** – Can handle hundreds of submissions automatically  
✅ **Customizable** – HRs can modify job descriptions or scoring rules easily  

---

### 🚀 Future Enhancements
🔹 Integration with **Gmail/Slack** for instant candidate notifications  
🔹 Dashboard visualization using **Looker Studio / Power BI**  
🔹 AI-generated feedback emails for candidates  
🔹 Multi-role handling for large-scale recruitment  
🔹 HR approval stage before sending final updates  

---

### 📈 Example Output
| Date | Candidate | Job Role | Score | Status | Summary |
|------|------------|----------|--------|---------|----------|
| 2025-10-21 | Priyank Singh | Sales | 7 | Qualified | Resume matches 80% of required skills; missing CRM expertise. |

---

### 🧩 Workflow Nodes Used
- `Form Trigger` → Collect candidate details  
- `Google Drive (Upload File)` → Save resumes  
- `Extract PDF` → Parse resume content  
- `Google Sheets (Get All JDs)` → Fetch job description  
- `If Node (Filter JDs)` → Match correct JD  
- `Gemini Model` → Analyze resume  
- `Set Node` → Format JSON output  
- `Google Sheets (Append Row)` → Store results  

---

### 👨‍💼 Author
**Sameer Kashyap**  
AI Automation Enthusiast | No-Code Developer | Building intelligent workflow systems  
📧 kashyapsameer731@gmail.com  
🔗 [LinkedIn](https://linkedin.com)

---

