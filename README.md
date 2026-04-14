# 🔐 Environment Configuration Manager

Manage, validate, and generate secure environment configurations locally.

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://python.org)
[![Ollama](https://img.shields.io/badge/Ollama-Compatible-green.svg)](https://ollama.com)
[![Gemma 3](https://img.shields.io/badge/Gemma-3-orange.svg)](https://ollama.com)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Privacy First](https://img.shields.io/badge/Privacy-First-red.svg)](#why-local)

## What It Does

- **Generates .env files** with intelligent defaults for your application
- **Validates environment variables** against schema requirements
- **Manages multiple environments** (dev, staging, production) from one template
- **Secrets stay local** — never exposed to external services

## Tech Stack

- **Python 3.8+** — Core management engine
- **Gemma 3** (via Ollama) — Configuration intelligence
- **python-dotenv** — Environment variable handling
- **Pydantic** — Configuration validation

## Quick Start

`ash
# Clone the repository
git clone https://github.com/kennedyraju55/env-config-manager.git
cd env-config-manager

# Install dependencies
pip install -r requirements.txt

# Pull Gemma 3 model locally
ollama pull gemma3:4b

# Generate environment config
python manager.py --template app-config.yml --environment production
`

## Architecture

`
config schema + requirements
    ↓
[Gemma 3 LLM Processing] ← offline, local
    ↓
validation rules
    ↓
.env file (with secure handling)
`

## Why Local?

- **Security**: Sensitive environment variables never transmitted or stored in the cloud
- **Privacy**: Full control over configuration data — no third-party access
- **Compliance**: Meet regulations requiring local secret management
- **Speed**: Instant configuration without external API calls

## Contributing

Contributions welcome! Please fork, create a feature branch, and submit a pull request.

## License

MIT License — see [LICENSE](LICENSE) for details.

---

*Part of 114+ privacy-first AI tools by Nrk Raju*