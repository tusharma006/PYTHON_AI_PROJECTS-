# 🎵 AI Semantic Song Recommendation System

An AI-powered Song Recommendation System that recommends songs using **Semantic Search** instead of traditional keyword matching.

Rather than searching for exact words, this project understands the **meaning** of the user's query by converting both songs and user queries into vector embeddings. It then retrieves the most relevant songs using vector similarity search with **ChromaDB**.

---

## 🚀 Features

- 🎶 Semantic Song Search
- 🤖 AI Embeddings using Sentence Transformers
- 📚 LangChain Document Processing
- 🗄️ ChromaDB Vector Database
- 🔍 Top-K Similarity Search
- 📈 Relevance Score for every recommendation
---

## 🛠️ Technologies Used

- Python
- Google Colab
- LangChain
- ChromaDB
- HuggingFace Embeddings
- Sentence Transformers
- JSON
---

## 📂 Project Structure

```
AI-Semantic-Song-Recommendation-System/
│
├── Song_Recommendation_System.ipynb
├── songs.json
├── README.md
├── requirements.txt
└── .gitignore
```

---

# 📊 Dataset

The project uses a JSON dataset where every song contains metadata such as:

- Song Name
- Artist
- Genre
- Mood
- Tempo
- Language
- Release Year
- Keywords
- Description

Example

```json
{
  "song_name":"Believer",
  "artist":"Imagine Dragons",
  "genre":"Rock",
  "mood":"Motivational",
  "tempo":"Fast",
  "language":"English",
  "description":"An energetic song about overcoming struggles."
}
```

---

# ⚙️ Installation

```bash
pip install langchain
pip install langchain-community
pip install langchain-huggingface
pip install langchain-chroma
pip install chromadb
pip install sentence-transformers
```

---

# 🧠 How the System Works

```
songs.json
      │
      ▼
Load Dataset
      │
      ▼
Convert Songs into LangChain Documents
      │
      ▼
Generate Embeddings
      │
      ▼
Store Embeddings in ChromaDB
      │
      ▼
User Query
      │
      ▼
Generate Query Embedding
      │
      ▼
Similarity Search
      │
      ▼
Top Matching Songs
```

---

# 📄 Document Creation

Each song is converted into a LangChain **Document**.

The **page_content** contains all important song information combined into a single text, for example:

```
Song Name: Believer
Artist: Imagine Dragons
Genre: Rock
Mood: Motivational
Language: English
Tempo: Fast
Description: An energetic song about overcoming struggles.
```

The embedding model generates embeddings using this **page_content**, allowing it to capture the semantic meaning of the entire song rather than individual fields.

---

# 🤖 Embedding Model

This project uses:

```
sentence-transformers/all-MiniLM-L6-v2
```

The model converts:

- Song page_content
- User Query

into **384-dimensional dense vector embeddings**.

These embeddings are stored in **ChromaDB** for fast semantic retrieval.

---

# 🔍 Semantic Search

When the user enters a query such as

```
I want motivational workout songs.
```

the system

1. Converts the query into an embedding.
2. Searches ChromaDB.
3. Finds the closest song embeddings.
4. Returns the Top-K most relevant songs.

---

# 📈 Similarity Score

The notebook uses

```python
similarity_search_with_score()
```

to retrieve the most relevant songs.

Example

| Song | Similarity Score |
|------|-----------------|
| Believer | 0.18 |
| Hall of Fame | 0.24 |
| Stronger | 0.31 |

Lower similarity scores indicate that the retrieved song is closer to the user's query in the embedding space.

---

# 📊 Relevance Ranking

Songs are ranked according to their semantic similarity.

The recommendation includes:

- Song Name
- Artist
- Genre
- Mood
- Description
- Similarity Score
- Rank

---

# 💬 Example Queries

```
Happy English songs
```

```
Romantic Bollywood songs
```

```
Songs for studying
```

```
Workout songs
```

```
Sad breakup songs
```

```
Calm relaxing music
```

---

# ❓ Frequently Asked Questions

### 1. On what basis are songs recommended?

Songs are recommended based on **semantic similarity** between the user's query and the song's page_content embedding, not simple keyword matching.

---

### 2. What does the similarity score mean?

The similarity score represents the vector distance between the query embedding and the song embedding.

A **lower score** means the song is more semantically similar to the user's query.

---

### 3. Which embedding model is used?

This project uses

```
sentence-transformers/all-MiniLM-L6-v2
```

to generate embeddings for both songs and user queries.

---

### 4. What text is embedded?

The embedding model generates embeddings using the **page_content** of each LangChain Document.

The page_content combines:

- Song Name
- Artist
- Genre
- Mood
- Language
- Tempo
- Description

into one semantic document.

---

### 5. Why use Semantic Search instead of Keyword Search?

Keyword search only finds exact words.

Semantic Search understands the **meaning** of the query.

Example:

Query

```
Energetic songs for gym
```

can successfully retrieve

```
Believer
```

even if the word "gym" does not appear in the dataset.

---

# 🚀 Future Improvements

- 🎤 Voice Search
- 🎧 Spotify API Integration
- 🤖 LLM-generated Recommendation Explanation
- 📱 Gradio Web Interface
- ❤️ Personalized Recommendations
- 🎼 Playlist Generation
- 🌐 Multilingual Search
- 🔎 Hybrid Search (Metadata + Semantic Search)

---

# 👨‍💻 Author

**Tushar Sharma**

B.Tech Computer Science Engineering

Artificial Intelligence | Machine Learning | LLM | RAG | Python

