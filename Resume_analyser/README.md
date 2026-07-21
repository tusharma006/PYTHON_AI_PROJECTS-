# Resume Search System

A simple AI-powered Resume Search System built using LangChain, Hugging Face Embeddings, ChromaDB, and OpenAI/OpenRouter.

## Features

- Load resumes from PDF and TXT files
- Split resumes into text chunks
- Generate embeddings using Hugging Face
- Store embeddings in ChromaDB
- Perform semantic search based on a job description
- Rank resumes by similarity
- Generate an AI explanation for why a resume matches the job requirements

## Technologies Used

- Python
- LangChain
- ChromaDB
- Hugging Face Embeddings
- OpenAI / OpenRouter
- PyPDF

## Project Structure

```
Resume-Search-System/
│
├── resume_search.ipynb
├── README.md
└── sample_resumes/
```

## How to Run

1. Install the required libraries.
2. Open the notebook in Google Colab or Jupyter Notebook.
3. Upload your resumes.
4. Enter a job description.
5. Run the notebook to find the most relevant resumes.

## Output

The system returns:

- Ranked resumes based on similarity
- Similarity scores
- AI-generated explanation for each matched resume

## Author

Tushar Sharma
