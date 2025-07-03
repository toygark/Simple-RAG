📚 Simple PDF-based RAG System with Ollama (LLaMA 3.2)
A minimal, local-first Retrieval-Augmented Generation (RAG) system powered by Ollama's LLaMA 3.2 model, capable of answering questions by retrieving contextually relevant content from PDF documents.

This project showcases how to load PDF documents, split them into searchable chunks, embed them into a vector database (ChromaDB), and perform query-time retrieval with augmented LLM responses using LangChain.

🚀 Features
🔥 Local LLaMA 3.2 model served via Ollama

📄 PDF ingestion and text chunking

🗂️ Vector embedding and storage via ChromaDB

💬 Multi-query retriever for improved document search accuracy

📖 Context-augmented query answering

🎛️ Interactive UI built with Streamlit

📦 Clean, extensible, lightweight codebase

📦 Tech Stack
Python 3.x

Ollama (for LLaMA 3.2 & text embeddings)

LangChain

ChromaDB

Streamlit

PyPDFLoader (LangChain Community)

RecursiveCharacterTextSplitter

MultiQueryRetriever

Sentence Transformers (embedding support)

🛠️ Setup & Installation
1️⃣ Install Ollama (if not already)
bash
Copy
Edit
curl -fsSL https://ollama.com/install.sh | sh
Start the Ollama service:

bash
Copy
Edit
ollama serve
2️⃣ Install Python dependencies
Create and activate a virtual environment:

bash
Copy
Edit
python3 -m venv venv
source venv/bin/activate
Then install the required packages:

bash
Copy
Edit
pip install -r requirements.txt
Note: You’ll need a PDF file at ./data/BOI.pdf or adjust DOC_PATH in app.py.

🎛️ How to Run
Start the Streamlit app:

bash
Copy
Edit
streamlit run app.py
Then open http://localhost:8501 in your browser.

✨ How It Works
📖 PDF loaded using PyPDFLoader.

📜 Text split into overlapping chunks via RecursiveCharacterTextSplitter.

🧠 Text chunks embedded with Ollama Embeddings using nomic-embed-text.

📊 Stored and retrieved from a Chroma vector database.

🔍 User queries are expanded into multiple variants with MultiQueryRetriever.

💬 Retrieved context + query passed to LLaMA 3.2 for answer generation.

🎛️ Interactive results displayed via Streamlit UI.

📄 Dependencies
Key dependencies:

css
Copy
Edit
ollama
chromadb
pdfplumber
langchain
langchain-core
langchain-ollama
langchain-community
langchain_text_splitters
unstructured
unstructured[all-docs]
fastembed
pikepdf
sentence-transformers
elevenlabs
📌 Project Structure
bash
Copy
Edit
.
├── app.py                # Streamlit app and RAG pipeline
├── data/
│   └── BOI.pdf           # Example PDF document
├── chroma_db/            # Persistent vector database directory
├── requirements.txt      # Python dependencies
└── README.md             # Project description
📖 Future Improvements
📚 Multi-PDF document support

📈 Vector store performance optimization

📝 Summarization and PDF metadata parsing

📊 Usage analytics and session history

📢 Credits
Built by Prazwal as a clean, local-first implementation of a PDF-based RAG system using Ollama and LangChain.

🔒 License
This project is open-source and available under the MIT License
