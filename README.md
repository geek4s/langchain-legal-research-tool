# Legal Research tool using Langchain RAG

An AI-powered Legal Research Assistant built using **LangChain**, **Retrieval-Augmented Generation (RAG)**, **Chroma Vector Database**, **HuggingFace Embeddings**, **Groq LLM**, and **Gradio**.

This application enables users to perform legal research by querying a knowledge base of legal documents, case law, and regulatory information. The system retrieves the most relevant legal document chunks using semantic similarity search and generates accurate, context-aware responses using a Large Language Model.

---

## 🚀 Features

- 📄 Document ingestion from **PDF**, **DOCX**, and **TXT**
- ✂️ Automatic document chunking using Recursive Character Text Splitter
- 🧠 Semantic embeddings using HuggingFace Sentence Transformers
- 🗄️ Chroma Vector Database for efficient storage and retrieval
- 🔍 Retrieval-Augmented Generation (RAG)
- ⚖️ Three Legal Assistant Modes:
  - Legal Query
  - Regulatory Analysis
  - Legal Brief Generation
- 🤖 Groq LLM integration for fast AI responses
- 💬 Interactive Gradio web interface

---

## 🏗️ RAG Architecture

```
Legal Documents
       │
       ▼
Document Loading
       │
       ▼
Text Chunking
       │
       ▼
Embedding Generation
(HuggingFace Embeddings)
       │
       ▼
Chroma Vector Database
       │
       ▼
User Query
       │
       ▼
Query Embedding
       │
       ▼
Similarity Search
       │
       ▼
Top-K Relevant Chunks
       │
       ▼
Prompt Template
       │
       ▼
Groq LLM
       │
       ▼
Generated Legal Response
```

---

## 🛠️ Tech Stack

| Technology | Purpose |
|------------|---------|
| Python | Programming Language |
| LangChain | RAG Pipeline |
| ChromaDB | Vector Database |
| HuggingFace Embeddings | Text Embeddings |
| Groq LLM | Large Language Model |
| Gradio | Web Interface |
| Google Colab | Development Environment |
| PyPDF | PDF Processing |
| python-docx | DOCX Processing |

---

## 📂 Project Structure

```
langchain-legal-research-tool/
│
├── README.md
├── langchain_legalresearchtool.ipynb
├── employment_discrimination.txt
├── gdpr_compliance.txt
├── roe_v_wade.txt
├── sec_ruling_2024.txt
├── legaldoc.pdf
└── legaldoc1.docx
```

---

## 📚 Dataset

The project uses a collection of legal reference documents including:

- Employment Discrimination Law
- GDPR Compliance
- Roe v. Wade
- SEC Regulatory Updates
- Legal PDF Documents
- Legal DOCX Documents

These documents are ingested into the Chroma Vector Database after chunking and embedding.

---

## ⚙️ How It Works

### Step 1: Document Loading

Legal documents are loaded from PDF, DOCX, and TXT files.

### Step 2: Chunking

Documents are split into smaller chunks using:

- RecursiveCharacterTextSplitter
- Chunk Size: 500
- Chunk Overlap: 100

### Step 3: Embedding Generation

Each chunk is converted into vector embeddings using:

- all-MiniLM-L6-v2

### Step 4: Vector Storage

Embeddings are stored in Chroma Vector Database.

### Step 5: Retrieval

When a user asks a question:

- Query is converted into an embedding
- Semantic similarity search is performed
- Top-K relevant chunks are retrieved

### Step 6: Generation

The retrieved chunks are passed to the Groq LLM along with a prompt template to generate the final legal response.

---

## 💻 Installation

Clone the repository

```bash
git clone https://github.com/<your-username>/langchain-legal-research-tool.git

cd langchain-legal-research-tool
```

Install dependencies

```bash
pip install langchain
pip install langchain-community
pip install langchain-core
pip install langchain-groq
pip install langchain-text-splitters
pip install chromadb
pip install sentence-transformers
pip install gradio
pip install python-docx
pip install pypdf
```

---

## ▶️ Running the Project

Open the notebook in Google Colab or Jupyter Notebook.

Run all cells.

Launch the Gradio interface:

```python
demo.launch(share=True)
```

Open the generated Gradio URL in your browser.

---

## 📸 Demo

> Add screenshots of your Gradio interface here.

Example:

- Home Screen
- Legal Query Mode
- Regulatory Analysis
- Legal Brief Generation

---

## 🔮 Future Improvements

- Multi-document upload
- Hybrid Search (BM25 + Vector Search)
- Metadata Filtering
- Persistent Chroma Database
- Source Citation with Similarity Scores
- Conversation Memory
- Streamlit Deployment
- Cloud Deployment (HuggingFace Spaces / Render / AWS)

---

## 👩‍💻 Author

**Nishitha Sathish**

Computer Science Engineering Student

Interested in:
- Artificial Intelligence
- Machine Learning
- Large Language Models (LLMs)
- Retrieval-Augmented Generation (RAG)
- Legal AI

GitHub: https://github.com/<your-username>

---

## ⭐ Acknowledgements

- LangChain
- ChromaDB
- HuggingFace
- Groq
- Gradio
- Google Colab

---

## 📄 License

This project is intended for educational and research purposes.
