# mathlens-tutor-chatbot
# MathLens Companion: Fractions & Decimals Tutor Bot (RAG)

A retrieval-augmented generation (RAG) chatbot built as teacher material for 
secondary-school students who are behind on fractions and decimals. Students 
ask plain-language questions and get short, step-by-step explanations grounded 
in real reference material — not the model's general knowledge.

## How it works
- Reference PDFs are loaded and split into chunks
- Chunks are embedded locally using a Hugging Face sentence-transformer model
- On a student question, the most relevant chunks are retrieved and passed to 
  an LLM (via Groq) along with a tutoring-style prompt
- The bot answers only from the retrieved material, and says so honestly if 
  the answer isn't in the reference text

## Running this notebook
1. Open in Google Colab
2. Add your own `GROQ_API_KEY` and `HF_TOKEN` as Colab secrets (key icon in 
   the left sidebar) — never hardcode these in the notebook
3. Upload your reference PDFs to `/content/data`
4. Run all cells in order

## Companion project
Built alongside [MathLens](link-to-your-other-repo) — a learner-profile 
dashboard using the same PISA 2022 dataset.
