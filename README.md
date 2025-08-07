# 📲 WhatsApp + Google Drive Automation (n8n + Twilio)

This project automates Google Drive file listing and other actions using **WhatsApp commands**. Built with **n8n**, this integration allows users to interact with Google Drive directly from WhatsApp using simple keywords like `LIST`.

---

## ✅ Project Features

- 🔁 Send commands via WhatsApp and receive real-time replies
- 📂 List files from a connected Google Drive folder
- 🧠 Built using n8n, a no-code/low-code workflow engine
- 🔒 Secured interaction using Twilio Sandbox and OAuth2
- 🚀 Easily extendable with future commands like `UPLOAD`, `DELETE`, etc.

---

## 🛠️ Tech Stack

| Tool       | Purpose                                |
|------------|----------------------------------------|
| n8n        | Workflow Automation Engine             |
| Twilio     | WhatsApp Messaging Integration         |
| Google API | Google Drive Access                    |
| Node.js    | Backend for running n8n locally        |

---

## 📦 Folder Structure

```
whatsapp-drive-automation/
├── n8n-workflow/
│   └── whatsapp-gdrive-workflow.json     # Exported n8n workflow file
├── docs/
│   └── sample-output.png                 # (Optional) Screenshots, diagrams
├── README.md                            # Project documentation
└── .gitignore
```

---

## 🚀 Setup Guide

### 1. Clone the Repository

```bash
git clone https://github.com/YOUR-USERNAME/whatsapp-drive-automation.git
cd whatsapp-drive-automation
```

---

### 2. Install & Run n8n Locally

```bash
npm install -g n8n
n8n
```

> n8n usually runs at [http://localhost:5678](http://localhost:5678) by default.

---

### 3. Setup Google Drive API

1. Go to [Google Cloud Console](https://console.cloud.google.com/)
2. Create a new project
3. Enable the **Google Drive API**
4. Navigate to **APIs & Services > Credentials**
5. Create **OAuth 2.0 Client ID**
6. Download your credentials or note the **Client ID** and **Client Secret**
7. In n8n, create a new credential using Google Drive (OAuth2) and paste these values

---

### 4. Setup Twilio WhatsApp Sandbox

1. Sign up at [Twilio](https://www.twilio.com/)
2. Go to **Messaging > Try it Out > WhatsApp Sandbox**
3. Note your:
   - Sandbox number (e.g. `+14155238886`)
   - Sandbox keyword (e.g. `join image-rock`)
4. Send the keyword to the number on WhatsApp to join
5. In n8n, add **Twilio Credentials** using your:
   - Account SID
   - Auth Token
   - From Number (`whatsapp:+14155238886`)

---

### 5. Import and Configure n8n Workflow

1. Open `http://localhost:5678`
2. Click **Import** > Upload the file `n8n-workflow/whatsapp-gdrive-workflow.json`
3. Click into each credential node and:
   - Link your Google Drive and Twilio credentials
4. Activate the workflow

---

## 💬 How to Use (WhatsApp Commands)

- Send `LIST` – to get list of files from your Google Drive
- Future support (extendable):
  - `UPLOAD` – upload a media file from WhatsApp to Drive
  - `DELETE <filename>` – delete a file from Drive
  - `HELP` – list available commands

---

## 📌 Notes

- This is a basic version and can be improved with better formatting, file links, thumbnails, and more command support.
- You can log WhatsApp messages in Google Sheets, Firebase, or a local DB for analytics.

---

## 🧠 Credits

Built by [Your Name]  
Powered by [n8n](https://n8n.io), [Twilio](https://www.twilio.com/), and [Google Cloud](https://console.cloud.google.com/)

---
