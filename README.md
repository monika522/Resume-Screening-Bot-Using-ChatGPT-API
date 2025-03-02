# Resume-Screening-Bot-Using-ChatGPT-API

Project Description: AI-Powered Resume Screening and Job Matching Chatbot Overview This project is a Proof of Concept (PoC) for an AI-based resume screening and job matching chatbot. It utilizes a local embedding model and a vector database to store and retrieve relevant resumes based on job descriptions. The system operates fully offline except for the optional use of the ChatGPT API, where users need to provide their own API key. Key Features

Resume Uploading: o Users upload multiple resumes in PDF format. o Extracts text from uploaded PDFs using pdfplumber.
Text Embedding & Vector Storage: o Uses SentenceTransformers (all-MiniLM-L6-v2) to generate embeddings for each resume. o Stores the embeddings in ChromaDB (a local vector database). o Users must provide their own OpenAI API key if they wish to use ChatGPT for additional processing.
Resume Search & Matching: o Accepts a job description as input. o Converts the job description into an embedding. o Queries the vector database for the top 3 most relevant resumes.
Optional ChatGPT Integration: o The project initializes OpenAI’s ChatGPT API but does not actively use it. o Users can integrate it for job description parsing, chatbot interaction, or enhanced text processing. Tech Stack • Vector Database: ChromaDB • Embedding Model: SentenceTransformers (all-MiniLM-L6-v2) • PDF Processing: pdfplumber • Programming Language: Python • Framework: Jupyter Notebook • Optional: OpenAI ChatGPT API (User must provide their own API key) Workflow
User uploads resumes.
Text is extracted from the resumes.
Embeddings are generated and stored in the vector database.
User inputs a job description.
The system finds the most relevant resumes using similarity search.
The top matching resumes are displayed.
(Optional) ChatGPT can be integrated for advanced resume/job description processing.

