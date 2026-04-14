# ⚙️ env-config-manager

Generate secure environment configs intelligently — zero exposure of sensitive settings

[![Python 3.8+](https://img.shields.io/badge/Python-3.8%2B-blue)](https://www.python.org)
[![Ollama](https://img.shields.io/badge/Ollama-Local%20LLM-green)](https://ollama.com)
[![Gemma 3](https://img.shields.io/badge/Gemma%203-Language%20Model-orange)](https://ollama.com/library/gemma2)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow)](./LICENSE)
[![Privacy First](https://img.shields.io/badge/Privacy-First-darkgreen)](#why-local)

## 🎯 What it does

- Create properly structured .env and environment config files from requirements
- Suggests best practices for secrets management, database connections, API keys
- Generates configs for different environments: dev, staging, production
- All sensitive data generation happens locally on your machine

## 🛠️ Tech Stack

- Streamlit (Web UI)
- FastAPI (Backend API)
- Ollama (Local LLM inference)
- Gemma 3 (Language model)
- Python 3.8+

## ⚡ Quick Start

1. **Clone the repository**
   \\\ash
   git clone https://github.com/kennedyraju55/env-config-manager.git
   cd env-config-manager
   \\\

2. **Install dependencies**
   \\\ash
   pip install -r requirements.txt
   \\\

3. **Download and start Ollama**
   - Download from [ollama.com](https://ollama.com)
   - Start Ollama service:
   \\\ash
   ollama serve
   \\\
   - In another terminal, pull Gemma 3:
   \\\ash
   ollama pull gemma2
   \\\

4. **Run the application**
   \\\ash
   streamlit run app.py
   \\\

Access the app at: http://localhost:8501

## 🏗️ Architecture

\\\
User specifies config requirements → Streamlit UI → FastAPI processes request → Ollama generates config using Gemma 3 → Returns secure templates → Save locally
\\\

All processing happens locally on your machine. No data is sent to external services.

## 🔒 Why Local?

Environment configs contain database passwords, API keys, service tokens, and deployment secrets. Generating these locally ensures your sensitive configuration never transmitted to external servers.

## 📦 Environment Variables

Create a \.env\ file in the project root:

\\\nv
OLLAMA_BASE_URL=http://localhost:11434
MODEL_NAME=gemma2
LOG_LEVEL=INFO
\\\

## 🤝 Contributing

We love contributions! Here's how to help:

1. Fork the repository
2. Create a feature branch: \git checkout -b feature/your-feature\
3. Make your changes and commit: \git commit -am 'Add feature'\
4. Push to the branch: \git push origin feature/your-feature\
5. Submit a Pull Request

Please ensure:
- Code follows PEP 8 style guidelines
- Changes include appropriate comments
- Updates to documentation are included

## 📄 License

This project is licensed under the MIT License — see [LICENSE](./LICENSE) for details.

---

**Part of 114+ privacy-first AI tools by [Nrk Raju](https://github.com/kennedyraju55)**