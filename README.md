# 🤖 RAG-Based Project Knowledge Assistant
### Built with n8n | Google Drive | Pinecone | OpenAI | Cohere Reranker
 📌 Project Overview
An end-to-end **Retrieval-Augmented Generation (RAG)** system 
built using n8n agentic workflows.

Enables project team members — QA Engineers, Developers, and 
Business Analysts — to instantly query project documents 
(requirements, POCs, specs) through a conversational chat 
interface.

> No more searching through SharePoint or scattered folders — 
> just ask a question and get an instant, accurate answer 
> from your project knowledge base!

## 🏗️ Architecture — Two Separate Workflows

### Workflow 1: Document Ingestion Pipeline
Automatically ingests project documents from Google Drive 
into Pinecone Vector Database.

![Ingestion Workflow](screenshots/ingestion_workflow.png)

**Flow:**
Google Drive (Search Files)
→ Download File
→ Default Data Loader
→ Recursive Character Text Splitter
→ OpenAI Embeddings
→ Pinecone Vector Store

### Workflow 2: AI Chat Assistant
Handles user queries and retrieves answers from 
the indexed knowledge base.

![Agent Workflow](screenshots/agent_workflow.png)

**Flow:**
Chat Message Received
→ AI Agent
→ Pinecone Vector Index (semantic search)
→ Cohere Reranker (result refinement)
→ OpenAI Chat Model (answer generation)
→ Response returned with memory context

---

## 🛠️ Tools & Technologies

| Tool | Purpose |
|------|---------|
| **n8n** | Agentic workflow orchestration |
| **Google Drive** | Source document repository |
| **OpenAI Embeddings** | Document vectorisation |
| **Pinecone Vector Store** | Vector database & semantic search |
| **Cohere Reranker** | Result reranking for accuracy |
| **OpenAI Chat Model (GPT)** | Answer generation |
| **Simple Memory** | Multi-turn conversation context |
| **Recursive Text Splitter** | Intelligent document chunking |

---

## 💬 Live Output Example

Real query answered by the assistant from uploaded 
project documents:

![Chat Output](screenshots/chat_output 1.png)
![Chat Output](screenshots/chat_output 2.png)
**Query asked:** *"What is the auto renewal process?"*

**Answer retrieved:**
- Auto renewal continues eligible policies into next term
- Renewal batch selects policies 90 days before expiration
- Eligibility rules — active, renewal-eligible, not flagged 
  as Do Not Renew
- Blocking underwriting referrals excluded until resolved

---

## 💡 Real-World Use Case

Designed for **P&C Insurance project teams** working on 
Duck Creek Policy implementations:

| Team Member | Example Query |
|-------------|--------------|
| QA Engineer | "What are the test scenarios for OOS transactions?" |
| Business Analyst | "What are the eligibility rules for renewal?" |
| Developer | "What is the reissue process flow?" |
| New Joinee | "Explain the policy lifecycle end to end" |

Instead of searching multiple SharePoint folders, 
team members get **instant accurate answers** from 
the centralised knowledge base.

---

## 🎯 Key Technical Highlights

- ✅ **Dual workflow architecture** — separate ingestion 
  and retrieval pipelines
- ✅ **Google Drive integration** — automatic document 
  ingestion from shared drives
- ✅ **Semantic search** — finds contextually relevant 
  content, not just keyword matches
- ✅ **Cohere Reranker** — advanced reranking for 
  improved answer accuracy
- ✅ **Multi-turn memory** — remembers conversation 
  context across queries
- ✅ **Insurance domain tested** — validated with real 
  P&C insurance project documents

---

## 🚀 Built As Part Of
**IK — Generative AI Training Program**

Combining 12+ years of P&C Insurance QA expertise 
with Generative AI to build practical,  AI solutions.

---

## 📁 Repository Structure
RAG-Project-Knowledge-Assistant/
│
├── README.md
├── screenshots/
│ ├── ingestion_workflow.png
│ ├── agent_workflow.png
│ └-- chat_output 1.png
  L__ chat_output 2.png

