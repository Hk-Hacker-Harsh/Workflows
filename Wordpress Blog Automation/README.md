# 🤖 AI Blog Automation (Telegram to WordPress)

This repository contains an **n8n workflow** that automates the process of turning raw thoughts or links sent via Telegram into SEO-optimized, Gen-Z styled blog posts on WordPress.

## 🚀 How it Works
1. **Telegram Trigger:** You send a message or a raw link to your Telegram Bot.
2. **Title AI Agent:** Uses **Ollama (Llama 3.2:3b)** to generate a high-impact, SEO-friendly title (40-60 chars).
3. **Content AI Agent:** Transforms the raw input into a formatted Markdown post with a "Gen Z Tech Creator" vibe.
4. **Markdown Converter:** Converts the AI output into HTML for WordPress compatibility.
5. **WordPress Node:** Automatically creates and publishes the post under a specific author ID.
6. **Telegram Notification:** Sends a confirmation message back to you with the live link to the post.

## 🛠️ Tech Stack
* **n8n:** Workflow automation.
* **Ollama:** Local LLM hosting (Running `llama3.2:3b`).
* **WordPress:** The destination CMS.
* **Telegram Bot API:** The input and output interface.

## 📋 Setup Instructions
1. **Import Workflow:** Import the `Blog_Automation.json` file into your n8n instance.
2. **Configure Ollama:** Ensure Ollama is running locally or on your server with the `llama3.2:3b` model pulled.
3. **Set Credentials:**
   * **Telegram API:** Connect your bot token.
   * **WordPress API:** Connect your site using Application Passwords.
   * **Ollama API:** Set your Ollama host URL (usually `http://localhost:11434`).
4. **Node Adjustments:** Update the `authorId` in the WordPress node to match your site's user ID.

## 📝 Configuration Note
The AI agents are tuned with a specific persona (CyberSecurity/Data Science). You can modify the **System Message** in the "Title AI Agent" and "Content AI Agent" nodes to match your own voice and niche.