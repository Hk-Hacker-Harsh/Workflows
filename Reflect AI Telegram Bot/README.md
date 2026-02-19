# 🧠 Reflect AI: Socratic Brainstorming Agent

An AI-powered Telegram bot built with n8n and Ollama, designed to act as a **Socratic Mirror**. Instead of providing answers, it asks targeted "5W" questions to force the user to clarify their own thoughts.

## 🤖 AI Persona: Reflect@i_bot
The agent follows a strict **Socratic Mirror** prompt:
- **Constraint:** Responses are always < 20 words.
- **Objective:** Ask one simple 5W question (What, Why, How, When, Where).
- **Rules:** - No advice given; user does 100% of the thinking.
    - Uses the user's name for a personalized "mirroring" experience.
    - Detects "stuck" states and offers non-directive hints or alternate views.

## 🛠 Tech Stack
- **AI Model:** Llama 3.2:3b (Running locally via Ollama).
- **Orchestration:** n8n (AI Agent & LangChain nodes).
- **Memory:** PostgreSQL (Stores session history to track the 5W progression).
- **Interface:** Telegram Trigger.

## 🚀 Deployment
1. Import `Reflect AI.json`.
2. Connect your **Ollama** node to your local instance.
3. Connect **PostgreSQL** for Chat Memory.
4. Input the system prompt provided in the repo to your Ollama node.