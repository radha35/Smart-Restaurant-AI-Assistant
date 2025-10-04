# 🍽️ Smart Restaurant AI Assistant

The **Smart Restaurant AI Assistant** is an intelligent chatbot that helps users explore restaurant menus for breakfast, lunch, and dinner.  
It integrates **Large Language Models (LLMs)**, **LangChain Agents**, and **custom tools** to dynamically respond to user requests with accurate menu information.

---

## 🚀 Overview

This project demonstrates how to connect an **LLM** with **LangChain Agents** and **custom-built tools** to perform decision-making and data retrieval tasks.

The system acts as:
- **LLM (Brain):** Understands user intent and generates natural language responses.  
- **Agent (Orchestrator):** Decides when and which tools to call.  
- **Tools (Capabilities):** Fetch real-time or structured data such as breakfast, lunch, and dinner menus.

---

## 🧠 How It Works

1. **User Query:** The user sends a request like “Show me the lunch menu.”  
2. **LLM Understanding:** The LLM (Gemini) processes the query and passes it to the LangChain agent.  
3. **Agent Decision:** The agent decides which tool to call — for example, `getMenuByCategory`.  
4. **Tool Execution:** The tool fetches the menu data for the requested category (validated with Zod).  
5. **Response Generation:** The agent combines tool output with the LLM to form a human-readable reply.  
6. **Frontend Display:** The message is displayed in a minimal web-based chat interface.

---

## 🧩 Architecture
User → Frontend → Express.js Server → LangChain Agent → Gemini LLM → Custom Tools


- **Frontend (HTML + JS):** Simple chat interface served from `public/index.html`.  
- **Backend (Express.js):** Handles `/api/chat` requests and connects to LangChain agent.  
- **LangChain Agent:** Manages reasoning and tool invocation flow.  
- **Gemini API:** Provides the LLM intelligence (text understanding and generation).  
- **Zod Validation:** Ensures tool inputs (e.g., “breakfast/lunch/dinner”) are valid.  

---

## 🧰 Technologies Used

| Category | Technology |
|-----------|-------------|
| **Programming Language** | JavaScript (Node.js, Express.js) |
| **LLM Provider** | Google Gemini (g2.5 Flash / Pro) |
| **Agent Framework** | LangChain |
| **Schema Validation** | Zod |
| **Frontend** | HTML, CSS, Vanilla JS |
| **Environment Variables** | dotenv |
| **Version Control** | Git & GitHub |

---

## ⚙️ Key Features

- 🧠 **LLM-Powered Understanding** — Handles natural language inputs.  
- 🔗 **LangChain Agent** — Makes intelligent decisions on when to use tools.  
- 🧩 **Dynamic Tools** — Custom-built tools to return menus by category.  
- 🧾 **Schema Validation** — Uses Zod to validate tool inputs.  
- 💬 **Minimal Chat UI** — Simple interface to interact with the AI assistant.  
- 🪲 **Error Handling** — Safe fallbacks and JSON responses for stability.  
- 🔍 **Debugging Support** — Verbose logging for tracing agent reasoning.  

---

## 🧪 Example Queries

- “What’s available for breakfast?”  
- “Show me the dinner options.”  
- “List today’s lunch menu.”  

---

## 🧩 Learnings & Insights

- How **Agents** use **tools** and make dynamic decisions.  
- How to integrate **Gemini API** with **LangChain**.  
- Managing **tool-call loops** using `maximumIterations`.  
- Using **intermediate steps** for stable fallback outputs.  
- Structuring a minimal but complete **LLM-powered web app**.  

---

## 🔑 Environment Setup

Create a `.env` file in your root directory:

GOOGLE_API_KEY=your_google_api_key

---

## 🧱 Project Setup

```bash
# Install dependencies
npm install

# Run the application
node server.js

