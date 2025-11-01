# 🧠 SmartTaskFlow-n8n  
**Automating task parsing and multi-channel communication using n8n + React**

---

## 🚀 Overview  
**SmartTaskFlow** is an intelligent automation system that connects a **React-based front end** with **n8n workflows** to process user tasks.  
It interprets user inputs like reminders or file-sharing tasks and executes them automatically — sending messages, emails, or attachments.

### ✨ Example  
> “Remind Ria to submit the report via Gmail.”  
→ SmartTaskFlow parses the task, identifies the recipient and action, and triggers the n8n workflow to send the mail instantly.

---

## 🧩 Tech Stack  

| Component | Technology |
|------------|-------------|
| Frontend | React (Vite) |
| Automation | n8n |
| Backend Bridge | Webhooks + Fetch API |
| Language Parsing | LLM (via n8n Code Node) |
| Styling | Poppins Font + Custom CSS |
| Hosting | ngrok (for local tunneling) |
| Optional | Upstash / Redis for caching |

---

## 🏗️ Architecture  

**Flow:**  
`User (Voice/Text Input)` → `React Frontend (VoiceInput.jsx / FileUpload.jsx)` →  
`n8n Webhook (POST via Fetch)` → `LLM Task Parser` →  
`JSON Task Array` → `Conditional Routing` →  
`Gmail Node (for emails)` / `Telegram Node (for messages)`  

---

## ⚙️ Features  

- 🎙️ Voice or text command input  
- 📂 File upload with automatic routing  
- 🤖 LLM-based task extraction  
- 📤 Smart multi-channel sending (Gmail, Telegram)  
- 🔁 Dynamic looping for multiple recipients/files  

---

## 🧰 Setup  

```bash
# Clone repo
git clone https://github.com/vaishaliragi66-rgb/agentic-ai-training-66.git
cd agentic-ai-training-66

# Install dependencies
npm install

# Run local server
npm run dev
🧾 License

MIT License © 2025 SmartTaskFlow
