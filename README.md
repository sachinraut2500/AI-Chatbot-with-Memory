# AI Chatbot with Memory (single-file demo)

A demonstration chatbot that keeps an embedding-backed memory and uses a local causal language model to generate replies conditioned on retrieved memories.

This is a *prototype* and educational demo — not production-ready. It shows how to:
- embed user/assistant messages,
- store them in a vector index (FAISS or brute-force),
- retrieve the most relevant past messages,
- construct a context prompt from retrieved memories,
- generate a reply using a local generative model (GPT-2 by default).

## 🔧 Features
- Persistent memory (can save/load memory DB)
- Embedding-based retrieval (SentenceTransformers)
- FAISS-backed index for speed (optional)
- Generation via `transformers` pipeline (GPT-2 or another causal LM)
- CLI chat loop with simple commands:
  - `/exit` — quit
  - `/help` — show commands
  - `/memdump` — display recent memories
  - `/clear_mem` — clear memory
  - `/save PATH` — save memory to PATH
  - `/load PATH` — load memory from PATH

## 🧰 Requirements

Recommended (best experience):
```bash
pip install sentence-transformers faiss-cpu transformers torch pandas
