# 📡 RSS to Telegram Automation (n8n Workflow)

🌐 **Language Selection:** [Türkçe](BENİOKU.md) | [English](README.md)
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
- RSS Feed sources

---

## 🔧 Installation & Usage

1.  **Download the project**
    
     [⬇️ İndirmek için tıkla](https://drive.usercontent.google.com/u/0/uc?id=1Swuaw-etASp2KgeeVL1HQ--QGfAKf4c8&export=download)

3.  **Install and run n8n**
    - Follow the [official documentation](https://docs.n8n.io/hosting/) for installation.
    - Import the `telegram_news_bot.json` file via the **Import Workflow** option in the n8n interface.

4.  **Create a Telegram Bot**
    - Create a new bot on Telegram via [@BotFather](https://t.me/BotFather) using the `/newbot` command.
    - Get the token (API) and add it to the n8n credentials section.
    - Add your bot to your channel with "administrator" permissions and approve the required permissions.
    - To find your `Chat ID`:
        - Write any message in the group you created, then use the following URL in your browser:
          
          `https://api.telegram.org/bot<TOKEN>/getUpdates`
          
        - Replace `<TOKEN>` with the token sent by @BotFather.
        - On the page that opens, you will see a JSON output with message details. Find the `chat` object. The `id` value within this object is the `Chat ID` you are looking for.

6.  **Add RSS sources**
    - Enter the RSS URLs into the `RSS 1` and `RSS 2` nodes.
    - [RSS LIST](https://bakinazik.github.io/rss/)
    - Add new (RSS READ) nodes for additional RSS sources if necessary.

7.  **Run the workflow**
    - The Scheduler will automatically trigger every 10 minutes.
    - News will pass through the duplicate check and be sent to Telegram.

---

## 📸 Diagram
![Workflow Diagram](docs/workflow-diagram.png)

---

## 🤝 Contributing
To contribute, you can fork the project and open a Pull Request.

---

## 📄 License
This project is licensed under the [MIT License](LICENSE).
