# ai-knowledge-workbench-GRAPHrag
llm-wiki-graphrag-workbench. Local-first GraphRAG knowledge workbench — private wiki +  live web search + gap detection + multi-agent reasoning.  Built for federal mission environments.  Auditable, Zero Trust, human-in-loop.

# 🧠 LLM + Wiki + GraphRAG Knowledge Workbench

> A local-first, privacy-safe AI knowledge engine combining 
> private wiki knowledge, live web search, GraphRAG 
> relationship mapping, and multi-agent reasoning.
> Built for federal mission environments where data 
> security, auditability, and human oversight matter.

---

## 🎯 What This Does

This system gives knowledge workers one interface to:
- Search private institutional documents semantically
- Find relationships between documents, entities, and topics
- Detect what evidence is MISSING (Science Gap Map)
- Challenge AI answers from multiple perspectives
- All with full audit trail and human review gates

---

## 📸 Screenshots

### Main Interface — Ask LLM + Six Intelligence Modes
[INSERT SCREENSHOT: main page with all 7 buttons]

### Document Knowledge Graph
> Wiki cross-reference visualization — shows which 
> documents connect and which are isolated orphans
[INSERT SCREENSHOT: document graph vis.js]

### Entity Graph (Fast)
> Real-time keyword entity extraction across full corpus
[INSERT SCREENSHOT: entity graph]

### Live AI Entity Graph
> Deep LLM semantic entity extraction with relationships
[INSERT SCREENSHOT: live AI graph]

### Science Gap Map ⭐
> Domain classification + gap risk scoring
> Red nodes = topics AI tools are systematically missing
> Orange diamonds = evidence gaps requiring attention
[INSERT SCREENSHOT: science gap map]

### Devil's Advocate Mode
> Three parallel perspectives on one question:
> Mainstream consensus | Contrarian evidence | Frontier gaps
[INSERT SCREENSHOT: three-column devil's advocate]

### Creative Connections
> Cross-document novel synthesis — finds non-obvious 
> connections between unrelated documents
[INSERT SCREENSHOT: creative connections output]

### Answer Output — Cited + Auditable
> Every answer cites exact source documents
> Full audit trail: query → docs retrieved → answer → reviewer
[INSERT SCREENSHOT: answer with citations]

---

---

## ⭐ Key Features

| Feature | Description |
|---|---|
| **Local-first** | Private data never leaves your machine |
| **Zero Trust** | Private wiki and public search are separated at architecture level |
| **Science Gap Map** | Finds what evidence is MISSING — not just what exists |
| **GraphRAG** | Relationships between documents are queryable data |
| **Devil's Advocate** | Mainstream + Contrarian + Frontier perspectives |
| **Auditable** | Every output reconstructable: query, docs, model version, answer, reviewer |
| **Token efficient** | Wiki index retrieves 2-5 chunks — 99% token reduction |
| **Human-in-loop** | Expert review gate before any consequential use |

---

## 🚀 Proven Results (CDC Deployment)

- 📄 80,000+ documents indexed and searchable
- 🎯 95% search accuracy
- ⚡ 10x research speed improvement
- 💰 Identified $22M in savings through portfolio gap detection
- 🔒 Zero security violations in production

---

## 🛠️ Tech Stack

- **Backend**: Python, Synthadoc (Kapache-LLM wiki engine)
- **Search**: Tavily (LLM-optimized web search)
- **Orchestration**: LangGraph multi-agent coordination
- **Visualization**: vis.js interactive graph rendering
- **LLM**: GPT-5.5 via Azure Government
- **Deployment**: Local Python — no cloud dependency for private data

---

## 📋 Use Cases

- Federal agency document research (EDIS, SOPs, investigation records)
- Systematic literature review (finds gaps in evidence base)
- Policy analysis (Devil's Advocate surfaces hidden assumptions)
- Knowledge management (distills institutional expertise)
- AI governance (Science Gap Map identifies under-studied areas)

---

## 🔒 Security Controls

- CBI/PII detection and redaction before LLM processing
- Prompt injection isolation (document text = DATA not INSTRUCTION)
- Immutable audit logging of all AI interactions
- Role-based workspace permissions
- Human review gate before any consequential output

---

## 📬 Contact

David Zhang, Ph.D.
[linkedin.com/in/david-zhang-d](https://linkedin.com/in/david-zhang-d)

Quick Setup — Four Things to Do
1. Create repo named: llm-wiki-graphrag-workbench

2. Create README.md — paste the above

3. Add screenshots folder:
   /screenshots/
     01_main_interface.png
     02_document_graph.png
     03_entity_graph.png
     04_science_gap_map.png
     05_devils_advocate.png
     06_creative_connections.png
     07_answer_output.png

4. Replace [INSERT SCREENSHOT] markers 
   with actual image links like:
   ![Main Interface](screenshots/01_main_interface.png)

*Built for federal mission environments. 
All data used in screenshots is dummy/public data.*

## 🏗️ Architecture
