# 📡 RSS to Telegram Automation (n8n Workflow)

🌐 **Language Selection:** [Türkçe](README.md) | [English](README.en.md)
---

This n8n workflow dynamically collects real-time news from multiple RSS feeds. The content is automatically delivered to your Telegram group or channel via a dedicated bot, ensuring your audience receives consistent and automated news updates.

---

## 🚀 Features
- Supports multiple RSS feeds
- Filters duplicate news items (duplicate check)
- Runs automatically every 10 minutes (Scheduler)
- Sends news to Telegram with image + title + summary
- Easy to customize
- New RSS sources or different message formats can be added.

---

## 🛠️ Technologies Used
- [n8n](https://n8n.io/) – Automation platform
- [Telegram Bot API](https://core.telegram.org/bots/api) – For sending news
- RSS Feed sources [RSS LIST](https://bakinazik.github.io/rss/)

---

## 🔧 Installation & Usage

1.  **Download the project**
    
    [Click to download](https://drive.usercontent.google.com/u/0/uc?id=1Swuaw-etASp2KgeeVL1HQ--QGfAKf4c8&export=download)


3.  **Install and run n8n**
    - Follow the [official documentation](https://docs.n8n.io/hosting/) for installation.
    - Import the `workflow.json` file via the **Import Workflow** option in the n8n interface.

4.  **Create a Telegram Bot**
    - Create a new bot on Telegram via [@BotFather](https://t.me/BotFather).
    - Get the token and add it to the n8n credentials section.
    - Use `https://api.telegram.org/bot<TOKEN>/getUpdates` to find your `Chat ID`.

5.  **Add RSS sources**
    - Enter the RSS URLs into the `RSS 1` and `RSS 2` nodes.
    - Add new (RSS READ) nodes for additional RSS sources if necessary.

6.  **Run the workflow**
    - The Scheduler will automatically trigger every 10 minutes.
    - News will pass through the duplicate check and be sent to Telegram.

---

## 📸 Example Workflow
![Workflow Diagram](docs/workflow-diagram.png)

---

## 🤝 Contributing
To contribute, you can fork the project and open a Pull Request.

---

## 📄 License
This project is licensed under the [MIT License](LICENSE).
