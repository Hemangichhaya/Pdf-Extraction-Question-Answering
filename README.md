# 📄 PDF Question-Answer Extraction using RAG and DeepSeek LLM

This project demonstrates a lightweight Retrieval-Augmented Generation (RAG) pipeline implemented in a Jupyter Notebook to extract context-aware question–answer (Q&A) pairs from PDF documents using the **DeepSeek** LLM via **Ollama**.

---

## 🔍 Features

- 📘 Load and parse PDF documents
- ✂️ Chunk content into meaningful text blocks
- 🧠 Use DeepSeek LLM (via Ollama) to generate Q&A pairs per chunk
- 🔁 Loop through content and display all extracted Q&A
- 💡 Built and tested inside a Jupyter Notebook

---

## 📁 File

- `PDF_Extraction_Question_&_Answer.ipynb` – the complete notebook for PDF parsing, chunking, and question-answer generation

---

## ⚙️ Setup Instructions

### 1. Install and run Ollama
```
# Install Ollama
curl -fsSL https://ollama.com/install.sh | sh

# Download and run the DeepSeek model
ollama run deepseek
```

**2. Clone the repository**
```
git clone https://github.com/your-username/pdf-qa-rag-notebook.git
cd pdf-qa-rag-notebook
```

**3. Set up the environment**
```
python -m venv venv
./venv/script/activate
pip install -r requirements.txt
```

**🧠 How It Works (Notebook Logic)**
Step	Description
1.	Load PDF and extract text using PyMuPDF (fitz)
2.	Clean and chunk the content into logical sections
3.	Define a prompt and send each chunk to the local LLM using subprocess or API call
4.	Extract question-answer pairs and display them in the notebook

**🧪 Sample Prompt**
```
Given the following text from a PDF document, generate relevant question–answer pairs:
---
[PDF chunk text here]
---
Return only clean Q&A pairs.
```

**💻 Run the Notebook**
Launch Jupyter Notebook:
```
jupyter notebook
```
Then open PDF_Extraction_Question_&_Answer.ipynb and run the cells step-by-step.

**🛠 Requirements**
* Python 3.8+
* Ollama
* DeepSeek model
* PyMuPDF

**Install using:**
```
pip install pymupdf tqdm
```
Or use the provided:
```
requirements.txt
```

**📚 Acknowledgements**
* Ollama – for running local LLMs
* DeepSeek – LLM for QA generation
* PyMuPDF – PDF text extraction










