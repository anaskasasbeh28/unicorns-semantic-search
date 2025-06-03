# 🦄 Unicorn Companies Embedding & Semantic Search 🚀

This project demonstrates how to create text embeddings from a dataset of unicorn companies, store them, and perform semantic search using OpenAI's embedding and GPT-3.5 Turbo models.

---

## 📋 Project Overview

The dataset contains information about unicorn companies worldwide. This project performs the following:

- 🔍 Load and explore the dataset.
- 📝 Generate textual summaries for each company.
- 🧮 Calculate token counts and estimate embedding costs.
- 📊 Create vector embeddings using OpenAI's `text-embedding-ada-002` model.
- 🔎 Perform semantic search using cosine similarity on embeddings.
- 🤖 Query the GPT-3.5 Turbo model with context-aware prompts.

---

## ⚙️ Setup and Requirements

- Python 3.x
- OpenAI Python library
- pandas
- numpy
- scikit-learn
- tiktoken

Install dependencies using:

```bash
pip install openai pandas numpy scikit-learn tiktoken
````

---

## 🛠️ Usage

### 1️⃣ Load Data and Explore

Load the CSV file containing unicorn company data, inspect columns, and preview records.

### 2️⃣ Generate Company Summaries

Create readable summaries by extracting and formatting key company details including investors.

### 3️⃣ Token Counting & Cost Estimation

Use OpenAI's tokenizer (`tiktoken`) to count tokens per summary and estimate embedding costs.

### 4️⃣ Generate Embeddings

Create vector embeddings for all company summaries using OpenAI's embedding API.

### 5️⃣ Semantic Search

* 💬 Input a natural language query.
* 🧠 Generate the query's embedding.
* 📈 Calculate cosine similarity between query and all summaries.
* 🏆 Retrieve the closest matching company summary.

### 6️⃣ Contextual Question Answering

Send the most relevant summary as context to GPT-3.5 Turbo and ask specific questions with high confidence.

---

## 💡 Code Highlights

* ⚡ Efficient use of `apply()` for DataFrame transformations.
* 🔒 Usage of `ast.literal_eval` for safe parsing of stringified lists.
* 🔢 Integration of `tiktoken` for accurate token counting.
* 📐 Cosine similarity to find nearest neighbors in embedding space.
* 🎯 Low temperature setting for deterministic GPT responses.

---

## 🔍 Example Prompt and Output

```python
prompt = "What does the company Minio do and where is the HQ?"
# After embedding and similarity search, GPT provides detailed, fact-based answers.
```

---

## ⚠️ Notes

* 🔑 Remember to securely store your OpenAI API key as an environment variable.
* 💸 Embedding generation and API usage may incur costs depending on token usage.
* 📂 Dataset (`unicorns.csv`) should be placed in the working directory.

---

## 🌐 License

MIT License. Free to use, modify, and share.
