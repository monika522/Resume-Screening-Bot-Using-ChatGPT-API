Project Description: AI-Powered Resume Screening and Job Matching Chatbot Overview This project is a Proof of Concept (PoC) for an AI-based resume screening and job matching chatbot. It utilizes a local embedding model and a vector database to store and retrieve relevant resumes based on job descriptions. The system operates fully offline except for the optional use of the ChatGPT API, where users need to provide their own API key. Key Features

1. Resume Uploading: Users upload multiple resumes in PDF format.
                     Extracts text from uploaded PDFs using pdfplumber.
2. Text Embedding & Vector Storage: Uses SentenceTransformers (all-MiniLM-L6-v2) to generate embeddings for each resume.
                                   Stores the embeddings in ChromaDB (a local vector database).
                                   Users must provide their own OpenAI API key if they wish to use ChatGPT for additional processing.
4. Resume Search & Matching: Accepts a job description as input.
                             Converts the job description into an embedding.
                             Queries the vector database for the top 3 most relevant resumes.
6. Optional ChatGPT Integration: The project initializes OpenAI’s ChatGPT API but does not actively use it.
                                Users can integrate it for job description parsing, chatbot interaction, or enhanced text processing.
                                Tech Stack• Vector Database: ChromaDB
                                          • Embedding Model: SentenceTransformers (all-MiniLM-L6-v2)
                                          • PDF Processing: pdfplumber
                                          • Programming Language: Python
                                          • Framework: Colab Notebook
                                          • Optional: OpenAI ChatGPT API (User must provide their own API key) Workflow
8. User uploads resumes.
9. Text is extracted from the resumes.
10. Embeddings are generated and stored in the vector database.
11. User inputs a job description.
12. The system finds the most relevant resumes using similarity search.
13. The top matching resumes are displayed.
14.  ChatGPT can be integrated for advanced resume/job description processing.
