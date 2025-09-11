# 📡 RSS to Telegram Otomasyonu (n8n Workflow)

🌐 **Language Selection:** [Türkçe](README.md) | [English](README.en.md)

---

This project contains a workflow built with **n8n** that collects news from multiple RSS feeds and automatically shares them through a **Telegram bot**.

---

## 🚀 Features
- Supports multiple RSS feeds
- Filters duplicate news items (duplicate check)
- Runs automatically every 10 minutes (Scheduler)
- Sends news to Telegram with image + title + summary
- Easy to customize

---

## 🛠️ Technologies Used
- [n8n](https://n8n.io/) – Automation platform
- [Telegram Bot API](https://core.telegram.org/bots/api) – For sending news
- RSS Feed sources

---

## 🔧 Installation & Usage

1. **Clone the project**
   ```bash
   git clone https://github.com/<username>/my-rss-telegram-bot.git
   cd my-rss-telegram-bot
   ```

2. **Install and run n8n**  
   - Follow [official documentation](https://docs.n8n.io/hosting/) to set it up.  
   - Import `workflow.json` file into n8n via **Import Workflow**.

3. **Create Telegram Bot**  
   - Message [@BotFather](https://t.me/BotFather) on Telegram.  
   - Create a new bot and get the token.  
   - Add the token in n8n credentials.  
   - Find `Chat ID` via `https://api.telegram.org/bot<TOKEN>/getUpdates`.

4. **Add RSS sources**  
   - Insert RSS feed URLs into `RSS 1` and `RSS 2` nodes.  
   - Add more nodes if you need additional feeds.

5. **Run the workflow**  
   - Scheduler will automatically trigger every 10 minutes.  
   - News will be filtered through duplicate check and sent to Telegram.

---

## 📸 Example Workflow
![Workflow Diagram](docs/workflow-diagram.png)

---

## 🤝 Contributing
Fork the project and open a Pull Request to contribute.  
You can add new RSS feeds or different message formats.

---

## 📄 License
This project is licensed under the [MIT License](LICENSE).
