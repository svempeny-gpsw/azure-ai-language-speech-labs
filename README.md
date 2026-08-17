# Azure AI Language & Speech Labs

Personal study repo for working through Microsoft Learn's **[Develop AI Language and Speech solutions on Azure](https://microsoftlearning.github.io/mslearn-ai-language/)** module, using **Microsoft Foundry** (Azure AI Foundry) and the underlying **Azure AI Language**, **Azure AI Speech**, and **Azure Translator** services.

## 🎯 What this repo covers

| # | Exercise | Focus | Link |
|---|----------|-------|------|
| 02 | Develop a text analysis agent | Building a Foundry Agent that uses the **Azure Language in Foundry Tools MCP server** to detect PII, extract named entities, and analyze sentiment via a Python client (`AIProjectClient` + OpenAI-style `responses` API) | [Instructions](https://microsoftlearning.github.io/mslearn-ai-language/Instructions/Exercises/02-language-agent.html) |
| 07 | Translate text and speech | Using the **Azure Translator** and **Azure Speech** SDKs to build a text-translation console app and a speech-to-speech translation app (English → French/Spanish/Hindi) | [Instructions](https://microsoftlearning.github.io/mslearn-ai-language/Instructions/Exercises/07-translation.html) |

## 🧰 Tech stack

- **Microsoft Foundry** (Azure AI Foundry) project + resource
- **Azure AI Language** (PII redaction, entity recognition, sentiment analysis) via MCP tool
- **Azure AI Translator** — text translation SDK
- **Azure AI Speech** — speech-to-text translation + speech synthesis
- **Python 3.13**, `azure-identity`, `azure-ai-translation-text`, `azure-cognitiveservices-speech`, `azure-ai-projects`
- **Azure CLI** (`az login`) for authentication via `DefaultAzureCredential`

## 📁 Structure

```
.
├── 02-language-agent/
│   └── text-agent/
│       ├── .env
│       ├── requirements.txt
│       └── text-agent.py
├── 07-translation/
│   └── translators/
│       ├── .env
│       ├── requirements.txt
│       ├── translate-text.py
│       └── translate-speech.py
└── README.md
```

> Base lab files originate from the official [`microsoftlearning/mslearn-ai-language`](https://github.com/microsoftlearning/mslearn-ai-language) repo; this repo contains my own completed/annotated versions as I work through the exercises.

## 🚀 Setup notes

1. Create a Microsoft Foundry project and resource (`{project_name}-resource`).
2. Copy the Foundry endpoint (`https://{resource}.cognitiveservices.azure.com/`) into each exercise's `.env` file.
3. Create/activate a Python virtual environment, then `pip install -r requirements.txt` per exercise.
4. Authenticate with `az login` before running any script (auth uses `DefaultAzureCredential`).
5. Remember to delete Azure resources after each lab to avoid ongoing costs.

## 📝 Learning log

- [x] Exercise 02 — Text analysis agent (PII redaction, entity extraction, sentiment via MCP tool)
- [x] Exercise 07 — Text & speech translation apps

## 📚 Reference

- [Module home: Develop AI Language and Speech solutions on Azure](https://microsoftlearning.github.io/mslearn-ai-language/)
- [Azure AI Language docs](https://learn.microsoft.com/azure/ai-services/language-service/)
- [Azure AI Translator docs](https://learn.microsoft.com/azure/ai-services/translator/)
- [Azure AI Speech docs](https://learn.microsoft.com/azure/ai-services/speech-service/)
