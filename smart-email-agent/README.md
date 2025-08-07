# 🤖 Smart Email Agent using n8n + OpenAI + Pinecone

This project is a **context-aware email-sending agent** built using [n8n](https://n8n.io/). It uses OpenAI for chat response, Google Docs as the data source, and Pinecone for semantic search.

> 🟢 **Live Chat Demo**:  
> 👉 [Click here to try the agent](https://my-ai-projects.duckdns.org/webhook/7443ed66-3662-4f4e-bc20-ea2642bb0184/chat)

---

## 🧠 What It Does

- Reads customer information from Google Docs.
- Extracts and indexes data into Pinecone using embeddings.
- Answers user queries contextually via OpenAI.
- Sends personalized emails when requested by the user.

---

## ⚙️ Architecture Overview

This project is composed of **3 main workflows** in n8n:

### 1. 🧠 AI Agent Flow

Handles incoming chat messages, uses OpenAI to understand user input, pulls context from Pinecone, and responds intelligently.

![Agent Workflow](docs/agent_workflow.png)

---

### 2. 📩 Send Email Flow

Triggered when the AI agent decides to send an email. It uses pre-defined parameters such as `To`, `Subject`, `Message`, etc., and includes the sender’s name.

![Send Email Workflow](docs/send_email_workflow.png)

---

### 3. 📄 Pinecone Vector Setup

Parses Google Docs, generates embeddings, and stores them into a Pinecone vector store. Used to build the knowledge base for the AI agent.

![Pinecone Workflow](docs/pinecone_workflow.png)

---

## 🔐 No Code Shared

This project only shares **workflow images** and a live working example. The source logic and credentials are kept private.

---

## 📄 License

MIT License — feel free to fork and build your own based on the idea.

---

## 🙋‍♂️ Author

Made with 💡 by [Rishav Gairola](https://github.com/rishav2307)
