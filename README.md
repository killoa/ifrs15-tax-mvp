# IFRS15-Tax-MVP

A minimalist, one-week MVP that ingests IFRS 15 guidance and a P&L CSV to calculate Dutch corporate tax (NL C-corp) using free-tier Azure services and an open-source LLM.

---

## 🚀 Features

- **IFRS 15 Ingestion**: Parses IFRS 15 PDF into embedded snippets via Sentence-Transformers + FAISS.  
- **Retrieval & Prompting**: Retrieves top-k IFRS 15 guidance for each line item and constructs an LLM prompt.  
- **Tax Engine**: Applies NL corporate tax brackets (19 % up to €200 000; 25.8 % thereafter) to calculated profit.  
- **API**: HTTP-triggered Azure Function (Python) processes CSV → JSON tax report.  
- **Frontend**: Single-page static UI (React or plain HTML/JS) on Azure Static Web Apps.
