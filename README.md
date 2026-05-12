<p align = "center" draggable="false" ><img src="https://github.com/AI-Maker-Space/LLM-Dev-101/assets/37101144/d1343317-fa2f-41e1-8af1-1dbb18399719"
     width="200px"
     height="auto"/>
</p>

<h1 align="center" id="heading">Session 2: Dense Vector Retrieval</h1>

### [Quicklinks]()

| 📰 Session Sheet | ⏺️ Recording | 🖼️ Slides | 👨‍💻 Repo | 📁 Feedback |
|:-----------------|:-------------|:----------|:----------|:------------|
| | | | | |

## ⚡ Lightning Session Overview

This lightning session introduces dense vector retrieval by building a small RAG pipeline with LangChain v1, OpenAI embeddings, and Qdrant.

The main notebook is:

```text
01_Cat_Health_Vector_RAG_LangChain_Qdrant.ipynb
```

The notebook uses the bundled cat health guideline PDF in `data/cat_health_guidelines.pdf`.

## 🛠️ Setup

From this folder, install the environment with uv:

```bash
uv sync
```

Then open the notebook in Cursor or VS Code and select the Python/Jupyter environment created by uv.

You will also need an OpenAI API key available when running the notebook.

---

## 🏗️ Activity #1: Embedding Similarity

Run the embedding similarity primer in the notebook.

You will compare embeddings for terms like:

- `king`
- `queen`
- `banana`
- `cat`
- `veterinarian`
- `cat health guidelines`

#### ❓Discussion Prompt

Why is cosine similarity useful for dense vector retrieval?

---

## 🏗️ Activity #2: Build the Vector RAG Pipeline

Run the notebook sections that:

1. Load the PDF into LangChain `Document` objects
2. Split the document into chunks
3. Embed the chunks
4. Store the chunk embeddings in in-memory Qdrant
5. Retrieve relevant chunks with similarity scores
6. Generate an answer grounded in retrieved context

#### ❓Discussion Prompts

- Why is metadata important for a RAG application?
- What tradeoff do we make when choosing chunk size and chunk overlap?
- What does a similarity score help you understand, and what does it not prove by itself?

---

## 🏗️ Activity #3: Vibe Check Retrieval Quality

Run the notebook's vibe check queries and inspect both:

- The retrieved context
- The generated answer

#### ❓Discussion Prompt

For the vibe check queries, did the retrieved context seem relevant before generation? Why or why not?

---

## 🏗️ Activity #4: Tune Retrieval

Improve retrieval quality by changing one or more of:

- Chunk size
- Chunk overlap
- Retrieval `k`
- Query wording

Document what changed and whether retrieval improved.

---

## 🚧 Optional Extensions

Extend the notebook in one meaningful way.

Suggestions:

- Compare similarity search with MMR retrieval
- Add metadata filtering
- Try a different embedding model
- Persist Qdrant locally instead of using in-memory Qdrant
- Add a second PDF and compare retrieval quality
