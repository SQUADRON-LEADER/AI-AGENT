![image](https://github.com/user-attachments/assets/c6074ec8-b877-4c42-89e1-496c1ee266a8)


# 🤖 AI Integration Detector (n8n - Gmail & Calendar)

Welcome to the **AI Integration Detector**, a smart agent built with **n8n** that determines whether **Google Calendar** and **Gmail** integrations are properly configured and active. This agent simplifies workflow monitoring, helping you verify if the necessary Google services are connected and being utilized.

---

## 🚦 Badges

![Status](https://img.shields.io/badge/status-active-brightgreen)
![n8n](https://img.shields.io/badge/powered%20by-n8n-blue)
![License](https://img.shields.io/github/license/yourusername/ai-integration-detector)
![PRs Welcome](https://img.shields.io/badge/PRs-welcome-blueviolet)

---

## 🧰 You’ll Need

* 🟢 [Node.js](https://nodejs.org/) (v14+ recommended)
* ⚙️ [n8n](https://n8n.io/) (CLI or Docker)
* 🔐 Google Cloud account with:

  * 📧 Gmail API enabled
  * 📅 Calendar API enabled

---

## 🛠️ Installation & Setup

### 📦 Clone the Repository

```bash
git clone https://github.com/yourusername/ai-integration-detector.git
cd ai-integration-detector
```

### 🚀 Setting Up n8n

1. **Install n8n** (if not already installed):

   ```bash
   npm install n8n -g
   ```

2. **Start n8n**:

   ```bash
   n8n
   ```

   Or with Docker:

   ```bash
   docker run -it --rm \
     -p 5678:5678 \
     -v ~/.n8n:/home/node/.n8n \
     n8nio/n8n
   ```

3. **Create Google Credentials**:

   * Go to [Google Cloud Console](https://console.cloud.google.com/)
   * Create OAuth 2.0 credentials
   * Enable Gmail API & Calendar API
   * Add credentials to n8n (under **Credentials > Google OAuth2 API**)

4. **Import the Workflow**:

   * Open `n8n` UI (usually at `http://localhost:5678`)
   * Import the workflow JSON from this repo: `gmail-calendar-check.workflow.json`

---

## 💡 Usage

Once set up, your AI agent can:

* ✅ Detect if **Gmail** credentials are active and messages are being retrieved
* 📆 Verify if **Calendar** events are accessible via API
* 🤖 Notify or trigger actions based on integration status

### 🎯 Example Use Case

* You want to validate during onboarding if a user has connected both Gmail and Calendar
* Your agent runs a check:

  * If both integrations are connected → ✅ Success message
  * If one or both are missing → ⚠️ Prompt user to connect services

### 📜 Sample Output


![image](https://github.com/user-attachments/assets/e8b59e63-5f49-4964-8703-79c10f78db7e)

![image](https://github.com/user-attachments/assets/75478890-276d-4997-a7ef-a0c363daeb25)



```
✅ Gmail Integration: Active
✅ Calendar Integration: Active
```

or

```
⚠️ Gmail Integration: Not Found
✅ Calendar Integration: Active
```

---

## 🌟 Features

* Plug-and-play with n8n
* Reusable in other workflows
* Extendable to support other Google APIs
* Minimal setup, maximum insight

---

## 🤝 Contributing

We welcome all contributions!

### 🧾 Guidelines

* Use clear and consistent naming (e.g., `feature/gmail-check`)
* Format code using Prettier
* Write meaningful commit messages

### 🔀 Pull Request Process

1. Fork the repo
2. Create a feature branch
3. Commit your changes
4. Submit a pull request with a clear explanation

---

## 📄 License

This project is licensed under the **MIT License**.
See the [LICENSE](./LICENSE) file for details.

---

## 📬 Contact

For questions, suggestions, or collaboration:

* GitHub: [@SQUADRON-LEADER](https://github.com/SQUADRON-LEADER)
* Email: [aayush05.af@gmail.com](mailto:aayush05.af@gmail.com)

---

> Made with ❤️ using n8n, Node.js, and Google APIs
