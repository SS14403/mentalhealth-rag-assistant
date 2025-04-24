# MentalHealth-RAG-Assistant 🧠🤖

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
```
Usage 🚀
Add your DSM-5 PDF to the /data folder

Create a .env file and add the following:
```bash
GEMINI_API_KEY="your_api_key"
PDF_PATH="data/dsm5.pdf"
```

Example Queries 💡

```python
"What are the diagnostic criteria for PTSD?"
"Explain the difference between bipolar I and II"
"List autism spectrum disorder symptoms in adults"
```

Project Structure 📂
```bash
mentalhealth-rag-assistant/
├── data/               # PDF storage
├── main.py             # Main pipeline
├── requirements.txt    # Dependencies
└── README.md
```


## 🛠 Troubleshooting

Common issues and solutions:

| Issue | Solution |
|-------|----------|
| **Gemini API errors** | Verify your API key at [Google AI Studio](https://aistudio.google.com/) and ensure you're using the correct model name (`gemini-pro` or `gemini-1.5-pro-latest`) |
| **PDF extraction fails** | Replace `PyPDF2` with `pdfplumber`:<br>`pip uninstall PyPDF2`<br>`pip install pdfplumber` |
| **Memory issues** | Reduce `CHUNK_SIZE` in `config.py` (try 200-300 words) and restart the application |
| **FAISS loading errors** | Rebuild the vector store:<br>`rm dsm5_faiss.index`<br>Then rerun `main.py` |
| **No responses from Gemini** | Check the prompt length (max 30K tokens for `gemini-pro`). Split long contexts into smaller chunks |
| **Missing dependencies** | Ensure all packages are installed:<br>`pip install -r requirements.txt` |



💡 **Pro Tip**: Always check the error logs for detailed messages. Common fixes are often highlighted there.


Disclaimer ⚠️<br>
This tool provides informational content only and is not a substitute for professional medical advice.

License 🪪<br>
Feel free to use this code as open source, however don't forget to star the repo

