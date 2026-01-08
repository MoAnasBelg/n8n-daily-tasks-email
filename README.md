# 📧 Daily Tasks Email Reminder (n8n)

This n8n workflow sends a daily email reminder containing tasks stored in a Google Sheet.

---

## 🧠 Workflow Overview

1. **Schedule Trigger**
   - Runs daily at a specific time (default: 08:30)
   - Change time inside the Schedule Trigger node

2. **Google Sheets**
   - Reads tasks from a Google Sheet
   - Each row must contain a column named `tasks`

3. **Python Code**
   - Collects all task phrases (no word splitting)
   - Formats tasks using HTML `<br>` for proper email display

4. **Gmail**
   - Sends the formatted tasks to an email address

---

## 📊 Google Sheets Format

| tasks |
|------|
| get orders |
| EAT |
| LEARN| 
| READ |
| work |


⚠️ Column name must be exactly: `tasks`

---

## ⚙️ Setup Instructions

### 1️⃣ Import Workflow
- Open n8n
- Import workflow
- Paste `n8n-daily-tasks-workflow.json`

### 2️⃣ Configure Google Sheets
Replace:
PUT_YOUR_GOOGLE_SHEET_ID_HERE
with your actual Sheet ID.

### 3️⃣ Configure Email
Replace:
RECEIVER_EMAIL_HERE

vbnet
Copier le code
with the destination email.

### 4️⃣ Set Schedule
Adjust:
triggerAtHour
triggerAtMinute

yaml
Copier le code

---

## 🚀 Activate Workflow
- Set Google Sheets & Gmail credentials
- Activate workflow
- Enjoy automated daily reminders ✨

---

## 💡 Ideas for Extension
- Numbered tasks
- WhatsApp / Telegram messages
- Weekly summaries
- Multi-user support
