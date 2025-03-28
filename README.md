# 🧠 OpenWebUI_Qdrant_Docker

This project sets up a local Retrieval-Augmented Generation (RAG) environment using:

- **OpenWebUI** – clean, chat-based interface for interacting with LLMs
- **Qdrant** – vector database for storing document embeddings
- **Ollama** – runs local language models like LLaMA3, Mistral, Phi-3, etc.

---

## 🧩 Components

| Service     | Port        | Description                              |
|-------------|-------------|------------------------------------------|
| OpenWebUI   | `http://localhost:3000` | Chat UI connected to Ollama + Qdrant |
| Qdrant      | `http://localhost:6333` | Vector database API (REST)           |
| Ollama      | `http://localhost:11434`| Local LLM server (e.g. llama3)        |

---

## 🚀 Getting Started

### 1. Clone the repo

```bash
git clone https://github.com/yourusername/OpenWebUI_Qdrant_Docker.git
cd OpenWebUI_Qdrant_Docker
