# PDF Query & Summarization (RAG + NLP)
<p align="left">
<img alt="Static Badge" src="https://img.shields.io/badge/license-MIT-MIT">
 <img alt="Issues" src=https://img.shields.io/github/issues/romisadeh/AskPDF>
 <img alt="last commit" src=https://img.shields.io/github/last-commit/romisadeh/AskPDF>
</p>

## Overview
This project enables users to upload a PDF file and ask questions about its content. The system uses **Retrieval-Augmented Generation (RAG)** and **Natural Language Processing (NLP)** techniques to extract relevant information, generate answers, and summarize the document. Additionally, it interacts with the **Gemini API** to enhance responses.

## Features
- **PDF Upload & Processing**: Extracts text from the uploaded PDF.
- **Summarization**: Generates a concise summary of the document.
- **Question-Answering System**: Uses **RAG** and **sentence embeddings** to find relevant content and answer user queries.
- **Gemini API Integration**: Enhances answers using Google's Gemini model.

## Technologies & Libraries Used
- **Python** (Jupyter Notebook)
- `pymupdf` – For extracting text from PDFs.
- `nltk` – For tokenization and text processing.
- `sentence-transformers` – For embedding-based similarity search.
- `spacy` – For Named Entity Recognition (NER) and text processing.
- `Google Gemini API` – For AI-powered answers.

## Example Usage
### 1. Uploading and Summarizing a PDF
#### **Uploaded PDF:** *Artificial Intelligence and Its Applications*
#### **Generated Summary:**
```plaintext
Artificial intelligence (AI) aims to create machines that mimic human intelligence.
Machine learning (ML), a key branch of AI, allows computers to learn from data and improve without explicit programming.
Explainable AI (XAI) focuses on making AI models transparent and understandable.
```

### 2. Asking a Question
#### **User Query:** "What are the types of machine learning?"
#### **Generated Answer:**
```plaintext
The three primary types of machine learning are:

1. Supervised Learning
2. Unsupervised Learning
3. Reinforcement Learning
```

## How It Works
1. The PDF is uploaded and processed using `pymupdf`.
2. The text is tokenized and embedded using `sentence-transformers`.
3. A similarity search finds the most relevant passage.
4. `spacy` is used for Named Entity Recognition (NER) to extract key entities.
5. The **Gemini API** refines and generates final answers.

## Installation & Setup
1. Clone the repository:
   ```sh
   git clone https://github.com/your-username/pdf-query-rag.git
   cd pdf-query-rag
   ```
2. Install dependencies:
   ```sh
   pip install pymupdf nltk sentence-transformers spacy
   ```
3. Download NLTK data:
   ```python
   import nltk
   nltk.download('punkt')
   ```
4. Load the **SpaCy** model:
   ```python
   import spacy
   nlp = spacy.load("en_core_web_sm")
   ```

## Future Improvements
- Expand entity extraction and contextual understanding.
- Support multiple document formats.
- Enhance query response with additional AI models.

