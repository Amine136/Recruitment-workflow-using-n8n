# 🤖 Recruitment Workflow using n8n

> Automates several repetitive tasks in a typical hiring pipeline using **n8n**, **Gemini API**, **Google Apps**, and **LinkedIn** — from collecting candidate data to generating job posts, ranking resumes, and scheduling interviews automatically.

---

## 📋 Overview

The **Recruitment Workflow** is a low-code automation built with **[n8n](https://n8n.io)** to simplify and accelerate the hiring process.  
It integrates AI (Google Gemini), Google Workspace tools, and LinkedIn to handle key steps — from job post generation to candidate evaluation and interview scheduling.

---

## ⚙️ Workflow Description

### 🔹 Step 1 — Generate & Post Job Descriptions
- Trigger: Chat input through n8n.
- Uses **Google Gemini API** via a LangChain node to transform short role descriptions into full LinkedIn-style job posts.
- Posts automatically to **LinkedIn** using the LinkedIn node.

### 🔹 Step 2 — Collect Candidate Applications
- Reads applications submitted through a **Google Form** (stored in a Google Sheet).
- Downloads uploaded **resumes** from Google Drive.

### 🔹 Step 3 — Evaluate Resumes with AI
- Extracts text content from resumes.
- Sends candidate resumes to **Gemini LLM** for structured scoring based on:
  - Technical requirements (60 pts)
  - Professional experience (30 pts)
  - Education & certifications (10 pts)
- Updates candidate **scores and ranks** in Google Sheets.

### 🔹 Step 4 — Rank & Select Top Candidates
- A **JavaScript node** sorts candidates by their rank.
- Selects the **top 5** candidates for interviews.

### 🔹 Step 5 — Schedule Interviews Automatically
- Creates interview events in **Google Calendar**.
- Invites the selected candidates by email.

---

## 🧠 AI Prompts Used

**1️⃣ Job Post Generator (Gemini):**  
Generates a complete LinkedIn job post following style rules (emojis, clean structure, hashtags, etc.).

**2️⃣ Resume Evaluator (Gemini):**  
Evaluates resumes based on predefined scoring logic and outputs structured JSON with:
```json
{
  "score": 87,
  "breakdown": {
    "requirements": 55,
    "experience": 25,
    "education_languages_certifications": 7
  },
  "strengths": ["Strong Python skills", "Experience with TensorFlow"],
  "gaps": ["Limited cloud experience"]
}
```

---

## 🧩 Technologies Used

| Tool / Service             | Purpose                                 |
| -------------------------- | --------------------------------------- |
| **n8n**                    | Workflow orchestration                  |
| **Google Gemini API**      | Job post generation & resume evaluation |
| **Google Sheets**          | Store and update candidate data         |
| **Google Drive**           | Host uploaded resumes                   |
| **Google Calendar**        | Schedule interview events               |
| **LinkedIn API**           | Auto-publish job posts                  |
| **JavaScript (Code node)** | Rank top candidates                     |

---

## 🖼️ Workflow Screenshot

![Workflow Screenshot](./workflow_screenshot.png)

---

## 🚀 How to Use

1. **Import the workflow JSON** into your n8n instance.
2. Set up credentials for:

   * Google APIs (Drive, Sheets, Calendar)
   * LinkedIn API
   * Gemini API (via LangChain)
3. Update any spreadsheet or document links as needed.
4. Execute the workflow or trigger it via chat input.
5. Watch the automation handle your recruitment pipeline end-to-end!

---

## 📂 Repository Structure

```
Recruitment-workflow-using-n8n/
├── recruitment_workflow.json      # Cleaned n8n workflow
├── workflow_screenshot.png        # Visual representation
└── README.md                      # Documentation
```

---

## 🪪 License

This project is licensed under the **MIT License** — feel free to use, modify, and share.

---

## 👤 Author

**Ouni Mohamed Amine**
[www.ouni.site](https://www.ouni.site)
💼 AI Engineer | Automation Enthusiast

```

---

Would you like me to also generate a `.gitignore` and `LICENSE` file (MIT style) so your repo looks complete?
```
