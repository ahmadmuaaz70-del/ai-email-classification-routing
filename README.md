<img width="960" height="540" alt="image" src="https://github.com/user-attachments/assets/96ec2f47-35a3-4904-9f2b-3ed9de8e6260" /># 🤖 AI Email Classification & Intelligent Routing System

I built this project to solve a common business problem: teams spend too much time reading and sorting emails that don't require human attention.

Instead of manually reviewing every email, this automation uses Google Gemini to understand the email, classify it, determine whether a human needs to review it, log every email into Google Sheets, and notify the team through Telegram only when immediate action is required.

My goal wasn't simply to automate emails—it was to build a workflow that could understand email context, reduce unnecessary notifications, and demonstrate how AI can support real business processes.

---

## 🏗️ How It Works

The workflow starts whenever a new email arrives in Gmail.

Google Gemini analyzes the email and returns structured information such as the category, department, priority, confidence score, and whether the email requires human attention.

A JavaScript node prepares the AI response for the rest of the workflow.

Every processed email is logged into Google Sheets to create a searchable audit trail. If the AI determines that immediate action is required, a Telegram notification is sent automatically. Otherwise, the workflow ends without interrupting the team.

```text
Gmail Trigger
      │
      ▼
Google Gemini AI
      │
      ▼
JavaScript Processing
      ├────────────► Google Sheets (Log Every Email)
      │
      ▼
Needs Human?
      │
    Yes
      ▼
Telegram Notification
```

---

## 💼 Business Problem

Businesses receive hundreds of emails every day, but not every email needs immediate attention.

Invoices, customer complaints, job applications, newsletters, billing receipts, meeting reminders, and promotional emails all arrive in the same inbox. Someone has to read each one, decide where it belongs, and determine whether it requires action.

This manual process takes time, interrupts employees, and increases the risk of missing important emails.

---

## 💡 Solution

I built this project to automate the first stage of email handling.

Instead of relying on keyword matching, Google Gemini understands the context of each email and returns structured information that the workflow can use to make decisions automatically.

Every email is logged into Google Sheets for record keeping, while only emails that require human attention generate a Telegram notification.

The result is a workflow that reduces repetitive work, keeps a complete audit trail, and helps teams focus on the emails that actually matter.

---

## ✨ Key Features

* AI-powered email understanding using Google Gemini
* Automatic email classification
* Department and priority assignment
* Human attention detection
* Google Sheets audit log for every processed email
* Telegram notifications for important emails only
* Context-aware decision making instead of simple keyword matching
* Modular workflow built with n8n


