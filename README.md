# 🧠 LLM + Wiki + GraphRAG Knowledge Workbench

> A local-first, privacy-safe AI knowledge engine combining private wiki knowledge, live web search, GraphRAG relationship mapping, and multi-agent reasoning.  
> Built for federal mission environments where data security, auditability, and human oversight matter. Note: dummy/public/synthetic data only used in this project.

---

## 🎯 What This Does

This system gives knowledge workers **one interface** to:

- Search private institutional documents **semantically** — not just by keyword
- Find **relationships** between documents, entities, and topics
- Detect what evidence is **MISSING** (Science Gap Map)
- Challenge AI answers from **multiple perspectives** (Devil's Advocate)
- All with **full audit trail** and **human review gates**

---

## 📸 Screenshots

### 1. Main Interface — Ask LLM + Six Intelligence Modes

> One search box. Seven capabilities. Private wiki + live web search combined.
<img width="1405" height="615" alt="image" src="https://github.com/user-attachments/assets/8041b6d3-68f2-4294-99d9-f38bef7021c7" />
<img width="1044" height="992" alt="image" src="https://github.com/user-attachments/assets/123586b5-6ac6-489d-88eb-c975899292bd" />


---

### 2. Document Knowledge Graph

> Wiki cross-reference visualization — shows which documents connect and which are isolated orphans (knowledge gaps).

<img width="1568" height="970" alt="image" src="https://github.com/user-attachments/assets/204c1967-5f97-413e-b130-5431bca722fa" />


---

### 3. Entity Graph (Fast)

> Real-time keyword entity extraction across the full document corpus.

<img width="1720" height="991" alt="image" src="https://github.com/user-attachments/assets/2c393ad5-fc84-4aef-b9ac-a6069661293e" />
<img width="1044" height="992" alt="image" src="https://github.com/user-attachments/assets/5c53c9b4-fe96-4711-aa65-33fe14d476f2" />


---

### 4. Live AI Entity Graph

> Deep LLM semantic entity extraction with relationship mapping.
<img width="1720" height="991" alt="image" src="https://github.com/user-attachments/assets/e0744fd8-807e-44d1-bfc4-94a17e6f3aa7" />



---

### 5. Science Gap Map ⭐

> Domain classification + gap risk scoring.  
> 🔴 Red nodes = topics AI tools are systematically missing.  
> 🔶 Orange diamonds = evidence gaps requiring human attention.

<img width="846" height="941" alt="image" src="https://github.com/user-attachments/assets/b084e7fc-9111-4fb0-91d6-daa1342fbd33" />


---

### 6. Devil's Advocate Mode

> Three parallel agent perspectives on the same question:  
> **Mainstream consensus** | **Contrarian evidence** | **Frontier gaps**
<img width="1063" height="738" alt="image" src="https://github.com/user-attachments/assets/f8834cb0-d62c-4d19-b343-3230fe9e7bac" />



---

### 7. Creative Connections

> Cross-document novel synthesis — finds non-obvious connections between unrelated documents and generates new research questions.

<img width="813" height="949" alt="image" src="https://github.com/user-attachments/assets/6ac8f0aa-675c-40b2-b2c9-db53bb49f561" />


---

### 8. Answer Output — Cited + Auditable

> Every answer cites exact source documents.  
> Full audit trail: query → docs retrieved → answer → reviewer → decision.

![Answer Output](screenshots/08_answer_output.png)

---

## 🏗️ Architecture

```
User input (voice or text)
         │
         ▼
Token budget management (128k context window)
         │
         ▼
Security gate (PII / CBI redaction + prompt injection isolation)
         │
         ▼
Context engine ──────────────────────────────────────────────────
│  ③ RAG          local wiki — 2-5 chunks only, not whole DB   │
│  ④ MCP tools    Tavily live web search (public only)          │
│  ⑦ Memory       semantic + episodic + procedural              │
──────────────────────────────────────────────────────────────────
         │
         ▼
Agent layer (LangGraph orchestration) ───────────────────────────
│  Router agent          decides which agents activate           │
│  Wiki agent            local private docs (Zero Trust)         │
│  Web search agent      public sources only — separated         │
│  Gap map agent         finds missing evidence nodes            │
│  Devil's Advocate      3 parallel sub-agents simultaneously    │
│  Synthesis agent       merges all agent outputs                │
│  Evaluation agent      checks all other agents                 │
──────────────────────────────────────────────────────────────────
         │
         ▼
Harness validation (schema + citations + confidence threshold)
         │
         ▼
Human review gate (expert validates before consequential use)
         │
         ▼
Answer + citations + immutable audit log
```

---

## ⭐ Key Features

| Feature | Description |
|---|---|
| **Local-first** | Private data never leaves your machine |
| **Zero Trust** | Private wiki and public search separated at architecture level |
| **Science Gap Map** | Finds what evidence is MISSING — not just what exists |
| **GraphRAG** | Relationships between documents are queryable data |
| **Devil's Advocate** | Mainstream + Contrarian + Frontier perspectives in parallel |
| **Auditable** | Every output reconstructable: query, docs, model version, answer, reviewer |
| **Token efficient** | Wiki index retrieves 2-5 chunks — 99% token reduction vs naive RAG |
| **Human-in-loop** | Expert review gate before any consequential use |
| **Multimodal** | Handles text, images, tables, and mixed PDFs |
| **Security hardened** | Prompt injection isolation, tool poisoning defense, red team tested |

---

## 🚀 Proven Results (CDC Production Deployment)

| Metric | Result |
|---|---|
| Documents indexed | 80,000+ publications and SOPs |
| Search accuracy | 95% |
| Research speed | 10x improvement |
| Cost savings identified | ~$22M/year (44 overlapping AI projects found) |
| Pipeline failure reduction | 22% → 1% (5,500+ pipelines) |
| Security violations | Zero in production across 30 AI projects |

---

## 🛠️ Tech Stack

| Component | Technology |
|---|---|
| Backend | Python — local deployment |
| Wiki engine | Synthadoc (Kapache-LLM compiled wiki) |
| Web search | Tavily (LLM-optimized search API) |
| Agent orchestration | LangGraph multi-agent coordination |
| Graph visualization | vis.js interactive graph rendering |
| LLM | GPT-5.5 via Azure Government |
| Security | Local Python — private data never crosses external boundary |

---

## 📋 Use Cases

- **Federal legal research** — EDIS filings, SOPs, investigation records
- **Trade analysis** — connecting parties, patents, HTS codes, countries
- **Systematic literature review** — finds gaps in evidence base
- **Policy analysis** — Devil's Advocate surfaces hidden assumptions
- **Knowledge management** — distills institutional expertise into searchable wiki
- **AI governance** — Science Gap Map identifies under-studied investment areas

---

## 🔒 Security Controls

- ✅ CBI / PII detection and redaction before LLM processing
- ✅ Prompt injection isolation — document text treated as DATA not INSTRUCTION
- ✅ Tool response validation — defends against tool poisoning
- ✅ Immutable audit logging of all AI interactions
- ✅ Role-based workspace permissions per project
- ✅ Zero Trust architecture — private and public data pipelines separated
- ✅ Human review gate before any consequential output
- ✅ Red team tested before production deployment

---

## 📁 Repository Structure

```
ai-knowledge-workbench-graphrag/
│
├── web_ui.py              # Flask UI — all routes and graph rendering
├── export_graphs.py       # Standalone graph export tool
├── requirements.txt       # Python dependencies
│
├── screenshots/           # All demo screenshots
│   ├── 01_main_interface.png
│   ├── 02_document_graph.png
│   ├── 03_entity_graph.png
│   ├── 04_live_ai_graph.png
│   ├── 05_science_gap_map.png
│   ├── 06_devils_advocate.png
│   ├── 07_creative_connections.png
│   └── 08_answer_output.png
│
└── README.md              # This file
```

---

## ⚠️ Important Note on Screenshots

> All data shown in screenshots is **dummy public data** for demonstration purposes only.  
> No real CDC, FEC, or agency data is included in this repository.  
> Production deployment uses fully private local data with Zero Trust controls.

---

## 📬 Contact

**David Zhang, Ph.D.**  
GS-14 Data Scientist | Enterprise AI Architect  
Centers for Disease Control and Prevention  

[![LinkedIn](https://img.shields.io/badge/LinkedIn-david--zhang--d-blue)](https://linkedin.com/in/david-zhang-d)
[![GitHub](https://img.shields.io/badge/GitHub-daviddata--cloud-black)](https://github.com/daviddata-cloud)

---

*Built for federal mission environments where AI must be useful for users, controlled for security, traceable for legal review, and clear for policymakers.*
