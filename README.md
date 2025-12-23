# 🧠 OpenWebUI_Qdrant_Docker

[![Docker](https://img.shields.io/badge/Powered%20By-Docker-blue?logo=docker)](https://www.docker.com/)
[![Qdrant](https://img.shields.io/badge/Vector%20DB-Qdrant-purple?logo=data)](https://qdrant.tech/)
[![Ollama](https://img.shields.io/badge/LLMs-Ollama-brightgreen?logo=openai)](https://ollama.com)
[![Made by Stan](https://img.shields.io/badge/Created%20by-Stan-blueviolet)](#)

Docker Compose setup for **OpenWebUI + Qdrant**, designed to connect to **Ollama running on the host** for local LLM inference and RAG-style workflows.

---

## 📦 Stack

Component overview:

- 🗨️ OpenWebUI — frontend chat interface  
- 📚 Qdrant — vector database for embeddings  
- 🧠 Ollama — local LLM runner (runs on host, not in Docker)  
- 🐳 Docker — containerizes OpenWebUI and Qdrant  

---

## 🚀 Getting Started

### 1. Clone the repo

    git clone https://github.com/spenkov101/OpenWebUI_Qdrant_Docker.git
    cd OpenWebUI_Qdrant_Docker

### 2. Start Ollama (host machine)

Make sure Ollama is installed and running locally:

    ollama serve

Pull a model if needed:

    ollama pull llama3

Ollama is **not** part of docker-compose and must be running on the host.

### 3. Configure environment

Copy the example environment file:

    cp .env.example .env

Adjust values if needed (ports, Ollama base URL, etc.).

### 4. Start OpenWebUI + Qdrant

    docker compose up -d

Open WebUI in your browser:

    http://localhost:3000

---

## 🧩 Notes

- Ollama is intentionally kept outside Docker to:
  - avoid GPU passthrough complexity
  - reuse existing local Ollama setups
  - keep the compose stack lightweight
- OpenWebUI connects to Ollama via HTTP (OLLAMA_BASE_URL).

---

## 🎯 Scope

This repository focuses on:
- clean local setup
- reproducible infrastructure
- minimal, understandable configuration

It is intended as a practical base environment, not a production deployment.

---

## 📜 License

MIT
