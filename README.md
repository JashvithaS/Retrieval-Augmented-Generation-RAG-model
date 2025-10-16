# Retrieval-Augmented-Generation-RAG-model
This project implements (RAG) model that combines information retrieval and generative AI to provide contextually relevant and accurate answers.The system retrieves relevant documents or text chunks from a knowledge base using similarity search and then passes this context to a large language model (LLM) to generate human-like responses.

**Features**
 Upload and process multiple TXT, PDF, or DOCX documents
- Vector storage with ChromaDB
- Automatic chunking and embedding of document text
- Retrieve top N relevant chunks for each query
- Offline AI responses using Ollama (no external API needed)
-Clean chat-style interface built with Streamlit
-Dark theme with contextual expansion for sources

 **Tech Stack**
Component	Technology
Interface	Streamlit
LLM	Ollama (local LLMs like mistral, llama2, gpt-oss)
Vector Store	ChromaDB
Embeddings	SentenceTransformers (all-MiniLM-L6-v2)
File Parsing	PyPDF2, python-docx
Language	Python 3.x

**Installation**
1️⃣ Clone the Repository
git clone https://github.com/JashvithaS/EchoAI-your-words-echoed-with-AI-insight.git
cd EchoAI-your-words-echoed-with-AI-insight

2️⃣ Install Required Libraries
pip install streamlit ollama chromadb sentence-transformers pypdf python-docx

3️⃣ Run Ollama
Make sure Ollama is installed and running:
ollama serve
You can check available models:
ollama list
Or pull a new one:
ollama pull gpt-oss:20b-cloud
4️⃣ Run the Streamlit App
streamlit run app.py

**📁 Folder Structure**
EchoAI-your-words-echoed-with-AI-insight/
│
├── app.py                 # Main Streamlit app
├── chroma_db/             # Vector database folder
├── output_images/         # Screenshots or sample outputs
└── README.md

 **How It Works**

Upload one or more documents
The app splits them into overlapping text chunks
Each chunk is embedded and stored in ChromaDB
When you ask a question:
It searches for the most relevant chunks
Creates a context-aware prompt
Sends it to Ollama for response generation
The retrieved sources and answers are displayed in chat

 **Author**

Srinamam Jashvitha
📍 Hyderabad, India
📧 srinamamjashvitha@gmail.com

🌐 GitHub – JashvithaS
