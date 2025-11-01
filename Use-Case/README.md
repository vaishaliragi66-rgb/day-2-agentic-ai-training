

```md
#  SmartTaskFlow-n8n  
**Automating task parsing and multi-channel communication using n8n + React**

---

## 🚀 Overview

**SmartTaskFlow** is an intelligent automation system that connects a **React-based front end** with **n8n workflows** to process natural-language commands.  
It interprets user inputs like reminders or file-sharing tasks and executes them automatically — sending messages, emails, or attachments to the right recipients.

### ✨ Example
> “Remind Ria to submit the report via Gmail.”  
→ SmartTaskFlow parses the task, identifies the recipient and action, and triggers the n8n workflow to send the mail instantly.

---

## ⚙️ Tech Stack

| Component | Technology |
|------------|-------------|
| Frontend | React (Vite) |
| Automation | n8n |
| Backend Bridge | Webhooks + Fetch API |
| Styling | Poppins Font + Custom CSS |
| Hosting | ngrok (for local tunneling) |
| Optional | Upstash / Redis for caching |

---

## 🧩 Architecture

```

User (Voice/Text Input)
↓
React Frontend (VoiceInput.jsx / FileUpload.jsx)
↓
n8n Webhook (POST Request via fetch)
↓
LLM Task Parser → JSON Task Array
↓
Conditional Routing:

* Gmail Node (for emails)
* Telegram Node (for quick messages)
* File Handling Nodes (for attachments)
  ↓
  Automated Task Completion ✅

````

---

## 🔧 Setup Guide

### 1. Clone the Repository
```bash
git clone https://github.com/vaishaliragi66-rgb/agentic-ai-training-66.git
cd agentic-ai-training-66
````

### 2. Install Frontend Dependencies

```bash
npm install
npm run dev
```

### 3. Run n8n with CORS Enabled

```bash
docker run -it --rm \
  -p 5678:5678 \
  -e N8N_CORS_ALLOW_ORIGIN="http://localhost:5173" \
  -v ~/.n8n:/home/node/.n8n \
  n8nio/n8n
```

### 4. Connect Frontend to n8n

Update your webhook URLs inside your React code (e.g., `VoiceInput.jsx`)
to point to your **ngrok** tunnel, e.g.

```
https://nonextendible-hyperexcitably-flora.ngrok-free.dev/webhook/your-webhook-id
```

---

## 🧠 Features

✅ Voice + Text input support
✅ File uploads with automated delivery
✅ Smart JSON parsing via LLM
✅ Gmail + Telegram message dispatch
✅ Error handling + loop automation in n8n
✅ Modular architecture for scaling

---

## 🧵 Folder Structure

```
project-root/
├── src/
│   ├── components/
│   │   ├── VoiceInput.jsx
│   │   ├── FileUploader.jsx
│   ├── App.jsx
│   ├── index.css
│   └── App.css
├── n8n_workflows/
│   └── TaskFlow.json
├── package.json
└── README.md
```

---

## 🪄 Future Improvements

* Integration with Google Calendar or Notion
* Multi-user role support
* Cloud deployment with persistent storage
* Improved LLM-based intent detection

---

## 💫 Author

**Vaishnavi Ragi**
💻 Engineering Student | ⚡ Automation Enthusiast | 🎨 Aesthetic Builder
GitHub → [@vaishaliragi66-rgb](https://github.com/vaishaliragi66-rgb)

---

> *“Don’t just automate tasks — orchestrate intelligence.”* 🚀

```

