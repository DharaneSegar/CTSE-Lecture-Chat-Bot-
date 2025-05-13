
# 📘 README: CTSE Lecture-Based Chatbot using RAG and Gemini

## 📌 Project Title
**CTSE Lecture-Based Question Answering Chatbot using RAG and Google's Gemini**

## 🧠 Description
This chatbot project answers questions based on CTSE (Current Trends in Software Engineering) lecture materials using a **Retrieval-Augmented Generation (RAG)** strategy. It combines **semantic search with FAISS** and the **Gemini 1.5 Pro model** for contextually grounded, high-quality responses.

---

## 🎯 Features

- ✅ Answers questions using lecture notes (PDFs, PPTX)
- ✅ Semantic retrieval using FAISS
- ✅ Uses **Google's Gemini 2.0 Flash** for LLM responses
- ✅ Prompt management for token efficiency
- ✅ Fully functional in **Google Colab (Jupyter Notebook)**

---

## 🧱 Tech Stack

| Component        | Tool/Library                     |
|------------------|----------------------------------|
| LLM              | `Gemini 2.0 Flash` via Google API  |
| Embedding Model  | `all-MiniLM-L6-v2`               |
| Semantic Search  | `FAISS`                          |
| PDF Parsing      | `PyMuPDF`                        |
| PPTX Parsing     | `python-pptx`                    |
| Interface        | Google Colab                     |

---

## 🔧 Setup & Usage in Google Colab

### 1. Open in Google Colab
Upload or open the notebook file: `Chatbot.ipynb` in [Google Colab](https://colab.research.google.com)

### 2. Mount Google Drive
Mount your Drive to access lecture files:
```python
from google.colab import drive
drive.mount('/content/drive')
```

### 3. Organize Lecture Materials
Create a folder in your Drive and upload the notes:

```
My Drive/
└── CTSE_Lectures/
    ├── Lecture1.pdf
    ├── Lecture2.pptx
    └── ...
```

Update the notebook variable:
```python
PDF_FOLDER = "/content/drive/My Drive/CTSE_Lectures"
```

### 4. Install Required Libraries
Run this cell to install dependencies:
```python
!pip install faiss-cpu transformers sentence-transformers pymupdf python-pptx gradio google-generativeai
```

### 5. Add Gemini API Key
Create an API key via [Google AI Studio](https://makersuite.google.com/app/apikey)

Then set the API key in the notebook:
```python
import os
os.environ["GOOGLE_API_KEY"] = "your_gemini_api_key_here"
```


### 6. Run the Notebook
Execute all cells in order to:
- Parse and embed lecture content
- Build FAISS index
- Query Gemini with RAG context

---


## 🗂️ Lecture Notes via Google Drive

1. Go to [Google Drive](https://drive.google.com)
2. Create folder `CTSE_Lectures`
3. Upload all `.pdf` and `.pptx` lecture files
4. Share with "Anyone with the link"
5. Paste the link below:

📎 **Lecture Materials Drive Link**: [Insert Shareable Link]

---

## 🧪 Example Prompts

### Question:
> *"What is prompt engineering?"*

### Answer:
> *" Prompt engineering involves crafting prompts to direct what the LLM should focus on. Good prompts lead to better and more reliable outputs. It shapes LLM behavior dynamically through careful wording, like writing a mini-program through text. Techniques include system prompts, chain-of-thought prompting, few-shot prompting, zero-shot prompting, and tool-use prompting. Effective prompts should be clear, specific, provide context, define the output format, and give examples. Prompt quality directly impacts output quality; clear prompts reduce errors, hallucinations, and vague responses. Even small changes in wording order can drastically change results.
"*

---
