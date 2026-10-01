# RAG-Project-Knowledge-Assistant
RAG-based document assistant built using n8n, Vector DB and AI Agent for project knowledge retrieval
# RAG-Based Project Knowledge Assistant
### n8n | Pinecone | OpenAI | Cohere Reranker | AI Agent

## 🔍 Project Overview
An end-to-end Retrieval-Augmented Generation (RAG) agentic 
workflow built in n8n — enabling project teams (QA, Developers, 
BAs) to query uploaded project documents through a conversational 
chat interface.

No more searching SharePoint or scattered folders — just ask a 
question and get an instant answer from your project knowledge base!

## 🛠️ Tools & Technologies Used
| Tool | Purpose |
|------|---------|
| **n8n** | Agentic workflow orchestration |
| **OpenAI Chat Model** | LLM for generating answers |
| **OpenAI Embeddings** | Converting documents to vector embeddings |
| **Pinecone Vector Index** | Storing and retrieving indexed documents |
| **Cohere Reranker** | Reranking retrieved results for accuracy |
| **Simple Memory** | Maintaining conversation context |

## 🏗️ Workflow Architecture
1. 📄 Documents uploaded → chunked → embedded via OpenAI
2. 🗄️ Embeddings stored in Pinecone Vector Index (1024 items)
3. 💬 User sends chat message → AI Agent triggered
4. 🔍 Semantic search on Pinecone → top documents retrieved
5. 🎯 Cohere Reranker refines results for accuracy
6. 🤖 OpenAI Chat Model generates answer with memory context
7. ✅ Relevant answer returned to user via chat

## 💡 Real-World Use Case
Designed for insurance/software project teams where:
- QA testers can query test requirements and business rules
- BAs can retrieve project specs and acceptance criteria
- Developers can access technical documentation instantly
- Eliminates need to search across multiple SharePoint folders

## 📸 Workflow Screenshot


## 🎯 Key Highlights
- ✅ Advanced Reranking using Cohere for improved accuracy
- ✅ Persistent vector storage with Pinecone
- ✅ Conversational memory for multi-turn queries
- ✅ Production-ready agentic architecture
- ✅ Built as part of Interview Kickstart AI Training Program
