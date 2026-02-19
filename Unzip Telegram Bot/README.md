# ⚡ Zippy: The Telegram Unzipper

A high-utility n8n workflow that automates the extraction of compressed files directly within Telegram.

## 🛠 Functionality
- **Input:** Accepts `.zip` archives sent to the bot.
- **Processing:** Automatically unzips files and splits the contents.
- **Logic:** Uses a `Switch` node to differentiate between commands and file uploads.
- **Filtering:** A `Filter` node ensures only the extracted files are processed and returned.
- **Output:** Delivers the extracted documents back to the Telegram chat.



## 🚀 Deployment
1. Import `Zippy.json` into n8n.
2. Connect your Telegram Bot credentials.
3. Ensure your n8n instance has `Binary Mode` set to "Separate" in settings for file handling.