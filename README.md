# Telegram Chat Bot (n8n + OpenAI + Supabase)

This repository contains a Telegram chat bot built on **n8n**, powered by **OpenAI** and integrated with **Supabase**.

- Receives messages via **Telegram Trigger**  
- Generates responses using **OpenAI**  
- Accesses knowledge base through **Supabase Vector Store**  
- Stores chat history in **PostgreSQL**  

---

## 📂 Project Structure
- `workflows/` → n8n workflow JSON files  
- `db/` → Supabase/PostgreSQL setup SQL files  

---

## 🚀 Quick Setup
1. Clone or download this repository.  
2. Open n8n → go to **Workflows → Import from file** → import the JSON files from `workflows/`.  
3. On Supabase/PostgreSQL, run the SQL file located at `db/supabase_n8n_connect.sql`.  
4. Create a `.env` file and define the following variables:  

   ```env
   TELEGRAM_API_KEY=xxx
   OPENAI_API_KEY=xxx
   SUPABASE_URL=xxx
   SUPABASE_KEY=xxx
   POSTGRES_URL=xxx
⚠️ Note: Never commit your real API keys. The .env file is already ignored by .gitignore.

▶️ Run
Activate the imported workflows in n8n.

Authorize the Telegram node using the token provided by BotFather.

📝 License
MIT
