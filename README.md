# 📖 API Manual Helper

The **API Manual Helper** is an intelligent assistant designed to make API documentation more accessible and interactive. Instead of manually searching through large API manuals, users can query the bot in **natural language** and receive contextual answers.  

It integrates **n8n** for workflow automation, **Pinecone** for vector search, **OpenAI models** for semantic understanding, and **Telegram** as the chat interface.  

---

## 🚀 Features
- 🔎 **Semantic Search on API Docs** – Ask questions like *“How do I authenticate requests?”* and get direct answers.  
- 📂 **Google Drive Integration** – Store and manage your API manuals in a shared knowledge base.  
- ⚡ **OpenAI Embeddings + Chat Model** – Provides context-aware answers in plain English.  
- 🔗 **n8n Workflow** – Automates query → search → answer → response pipeline.  
- 💬 **Telegram Bot Interface** – Users can ask queries directly in Telegram.  
- 📌 **Step-by-step Guides** – Extracts relevant parts of the API manual and explains usage.  

---

## 🛠️ Tech Stack
- [n8n](https://n8n.io/) – Workflow orchestration  
- [Pinecone](https://www.pinecone.io/) – Vector database for semantic search  
- [OpenAI](https://platform.openai.com/) – Embeddings + LLM for NLP  
- [Telegram Bot API](https://core.telegram.org/bots/api) – Messaging platform  
- [Google Drive](https://www.google.com/drive/) – API manual storage  

---

## 📊 Architecture Flow
flowchart TD
    A[User asks API question in Telegram] --> B[Telegram Bot]
    B --> C[n8n Webhook]
    C --> D[OpenAI Embedding]
    D --> E[Pinecone Vector DB]
    E --> F[Relevant API Manual Sections]
    F --> G[OpenAI Chat Model]
    G --> H[Answer Generated]
    H --> I[Send Response to User via Telegram]
    C -->|Optional| J[Google Drive Knowledge Base]

📖 Usage

Once connected, open your Telegram Bot and start asking API-related questions.

💬 Example Queries to Ask the Bot

Show me REST API example

📌 Bot will return a sample REST API request/response from the manual.

How to upsert the account

📌 Bot will retrieve the API guide section on account upsert and explain request body & endpoint.

REST API for Salesforce

📌 Bot will provide the Salesforce REST API documentation snippet and authentication details.

🔮 Future Improvements

✅ Support for multiple API manuals

✅ Export query responses to PDF/Markdown

✅ REST API for external integration

✅ Interactive code examples

🤝 Contributing

Pull requests are welcome! For major changes, please open an issue first to discuss improvements.

📜 License

This project is licensed under the MIT License – see the LICENSE
 file for details.
