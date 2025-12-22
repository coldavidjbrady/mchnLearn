## How the HuggingFace and PyTorch RAG Labs Align

Both labs teach **Retrieval-Augmented Generation (RAG)** workflows. They focus on combining:
- a **retriever** that converts text into embeddings, and  
- a **generator** that consumes those embeddings to answer questions,  

with the shared goal of building an **end-to-end, QA-style pipeline**.

Each lab relies on the **Hugging Face ecosystem running on PyTorch**—installing `transformers` and `torch`, and using Hugging Face tokenizers and models directly inside PyTorch code cells.

Both also introduce **similarity-based retrieval** as the bridge between embeddings and generation:
- the **PyTorch lab** explicitly encourages experimenting with similarity metrics (dot product vs. cosine),  
- the **HuggingFace lab** uses **FAISS** as the similarity-search backend.

---

## How They Differ

### Retriever Design

- **HuggingFace lab**  
  Centers on the **Dense Passage Retriever (DPR)** from `transformers` for both question and context encoding, paired with **FAISS indexing** for fast nearest-neighbor search.

- **PyTorch lab**  
  Builds embeddings with `bert-base-uncased` using Hugging Face tokenizers, but relies on **manual similarity calculations** and PyTorch-style loading—explicitly inviting you to swap dot product for cosine similarity.

### Generator Component

- **HuggingFace lab**  
  Pairs the DPR retriever with a **GPT-2 generator**, demonstrating retrieval-conditioned generation and comparing outputs **with and without retrieved context**.

- **PyTorch lab**  
  Stays firmly on the **embedding and retrieval side**, emphasizing **embedding visualization (t-SNE)** and similarity scoring rather than full text generation.

### Learning Goals and Time

- **HuggingFace lab**  
  Shorter (≈30 minutes) and focused on applying **DPR + GPT-2** to HR policy QA, highlighting how retrieval improves generation.

- **PyTorch lab**  
  Longer (≈60 minutes) and framed as a **child-safety content classifier**, stressing embedding mechanics, visualization, and hands-on experimentation with similarity metrics to evaluate retrieval quality.

---

## Quick Takeaway

Both labs use **Hugging Face models inside PyTorch**, but:
- the **HuggingFace lab** gives you a turnkey **DPR → FAISS → GPT-2** RAG stack,  
- the **PyTorch lab** is a deeper dive into **building and analyzing embeddings** (with BERT) and similarity-search mechanics before you ever plug in a generator.

In short: one’s a ready-made sports car, the other teaches you how the engine works. 🚗🔧
