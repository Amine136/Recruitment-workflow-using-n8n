# Recruitment Workflow using n8n

This repository contains an **automated recruitment workflow** built with [n8n](https://n8n.io/).  
The workflow helps streamline the hiring process — from receiving applications to storing and managing candidate data automatically.

---

## 🚀 Overview

The **Recruitment Workflow using n8n** automates several repetitive tasks in a typical hiring pipeline.  
It is designed to:

- Receive new candidate submissions (via email, form, or webhook)
- Extract and clean candidate data (name, email, CV link, skills, etc.)
- Store the structured data in a database or spreadsheet
- Send automated notifications or follow-ups
- Provide HR with a clean, centralized candidate dashboard

---

## 🧩 Files

| File | Description |
|------|--------------|
| `recruitment_workflow.json` | Cleaned n8n workflow JSON file (ready to import) |
| `workflow_screenshot.png` | Visual representation of the workflow in n8n |
| `README.md` | Documentation and setup instructions |
| `.gitignore` | Optional file to keep repo clean |

---

## 🖼️ Workflow Preview

![Workflow Preview](workflow_screenshot.png)

---

## ⚙️ How to Use

1. Open your **n8n** instance (local or cloud).
2. Go to **Workflows → Import from File**.
3. Upload the file `recruitment_workflow.json`.
4. Configure your credentials (email, database, or webhook as needed).
5. Activate the workflow and watch the automation run! 🎉

---

## 🧠 Description of the Workflow

This workflow automates key recruitment operations:
- Triggers on new job applications.
- Parses and validates candidate information.
- Filters or ranks candidates based on predefined criteria.
- Sends notifications or forwards data to HR systems.
- Optionally stores structured records in a database for analytics or tracking.

It can be adapted to different hiring platforms (LinkedIn, Google Forms, custom forms, etc.).

---

## 🪪 License

This project is licensed under the **MIT License** – feel free to use and modify it for your own workflows.

---

## 👨‍💻 Author

Created by **[Ouni Mohamed Amine](https://www.ouni.site)**  
AI Engineer | Automation Enthusiast | Data Scientist
