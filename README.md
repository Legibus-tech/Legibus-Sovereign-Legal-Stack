# LEGAL-RAG Stack

**Federated Document Storage & Retrieval Infrastructure for AI-Powered Legal Research**

![LEGAL-RAG Stack Architecture]([[https://via.placeholder.com/800x400?text=LEGAL-RAG+Architecture+Diagram](https://placehold.co/800x400/transparent/000?text=LEGAL-RAG+Architecture+Diagram)](https://placehold.co/800x400/transparent/000?text=LEGAL-RAG+Architecture+Diagram))
*Privacy-preserving AI for legal professionals*

---

## 📌 Overview

The LEGAL-RAG Stack is an open-source, self-hostable solution designed to empower legal professionals with AI-assisted research capabilities while maintaining strict compliance with privacy regulations (GDPR, professional secrecy). 

This project combines:
- **Document federation** (Nextcloud/S3)
- **Open-source AI** (Mistral, LlamaIndex)
- **Legal-specific tooling** (Légifrance/DILA connectors)
- **Compliance-by-design** (audit logs, access controls)

Built for lawyers, NGOs, and public institutions needing sovereign AI infrastructure.

---

## 🧩 Key Components

| Component          | Technology       | Purpose                          |
|--------------------|------------------|----------------------------------|
| **Document Hub**   | Nextcloud        | Secure storage & sharing         |
| **Vector Store**   | Qdrant/Weaviate  | Legal document embeddings        |
| **RAG Engine**     | LlamaIndex       | Context-aware querying           |
| **AI Gateway**     | FastAPI          | LLM integration (Mistral/others) |
| **Compliance**     | OpenTelemetry    | Audit trails & access logs       |

---

## 🚀 Quick Start

### Prerequisites
- Docker 20.10+
- Python 3.10+
- 8GB+ RAM (for AI models)

### Deployment
```bash
git clone https://github.com/yourorg/legal-rag.git
cd legal-rag/deploy
docker-compose up -d
```
### Access:
- Nextcloud: http://localhost:8080
- RAG UI: http://localhost:5000

## 🌐 Use Cases
1. Cross-institution legal research
  - Query federated case law databases while preserving client confidentiality
2. NGO document analysis
  - Rapidly analyze human rights reports with cited legal precedents
3. Municipal compliance
  - Maintain searchable archives of local regulations with AI-assisted summaries

## 🔧 Customization
### Adding Legal Sources
Edit config/connectors.yml:

```yaml
legifrance:
  endpoint: https://api.legifrance.gouv.fr
  auth_type: oauth2
  document_types: [codes, directives]
```
### Model Configuration
Set AI preferences in **rag/config.py**:

```python
MODEL = "mistral-7b-instruct"
MAX_TOKENS = 4096
CACHE_DIR = "/data/vector_cache"
```

## 📜 License
- Core Stack: **AGPL-3.0**
- Documentation: **CC-BY-SA-4.0**
- Example Data: **Non-commercial use only**

## 🤝 Contributing
We welcome:
- Legal professionals for workflow validation
- Developers for:
  - New connector implementations
  - UI/UX improvements
  - Localization (FR/EN/ES)
See CONTRIBUTING.md for guidelines.

## 📚 Documentation
| Resource	| Link |
|-------------------|----------------------|
| Deployment Guide	| /docs/deployment.md |
| API Reference	| /docs/api.md |
| GDPR Compliance	| /docs/compliance.md 
| Troubleshooting	| /docs/troubleshooting.md |

## 📬 Contact
For legal deployment support:
contact@legibus.fr

_"Empowering justice with open infrastructure"_
