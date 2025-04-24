# MentalHealth-RAG-Assistant 🧠🤖

![RAG Pipeline](https://miro.medium.com/v2/resize:fit:1400/1*5ZLci3SuR0zM_QlZOADv8Q.png)

A Retrieval-Augmented Generation (RAG) chatbot powered by Google Gemini, providing DSM-5 based mental health information with source-grounded responses.

## Features ✨

- 📄 **PDF Processing**: Extract text from DSM-5 PDFs
- 🧹 **Text Cleaning**: Remove artifacts and normalize text
- ✂️ **Semantic Chunking**: 200-500 word context-aware segments
- 🔍 **Vector Search**: FAISS with `all-MiniLM-L6-v2` embeddings
- 🤖 **Gemini Integration**: Latest Google LLM for generation
- 🏥 **Clinical Focus**: Specialized for mental health queries

## Installation ⚙️

```bash
git clone https://github.com/yourusername/mentalhealth-rag-assistant.git
cd mentalhealth-rag-assistant
pip install -r requirements.txt
