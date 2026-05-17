# 📊 RAG Financial Report Analyzer

Ask plain-English questions against any annual report or 10-K PDF.  
Built with FAISS + sentence-transformers + OpenAI GPT-4o-mini.

## How It Works
1. PDF is extracted and split into overlapping chunks
2. Each chunk is embedded using `all-MiniLM-L6-v2` (384-dim vectors)
3. User query is embedded and matched against chunks via FAISS
4. Top-5 most relevant chunks are passed to GPT-4o-mini for answer generation

## Example Questions
- "What are the main business segments?"
- "What risks does the company mention?"
- "What was total revenue in 2023?"
- "What is the investment strategy?"

## Tech Stack
Python · sentence-transformers · FAISS · OpenAI API · pdfplumber · Jupyter

## How To Run
1. Clone this repo
2. Install dependencies: `pip install openai sentence-transformers faiss-cpu pdfplumber numpy scikit-learn`
3. Open `RAG_Financial_Analyzer.ipynb` in Jupyter
4. Add your OpenAI API key in Cell 2
5. Replace the PDF path in Cell 3 with your own financial report PDF
6. Run all cells
