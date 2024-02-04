# Medical-ChatBot

# 1. Introduction
The Intelligent Medical Chatbot project aims to create an advanced conversational agent that leverages document retrieval techniques to provide accurate and timely information to users. By extracting data from medical PDFs, splitting the text into manageable chunks, and utilizing state-of-the-art language models and vector stores, the chatbot can deliver intelligent responses to user queries.

# 2. Technologies and Libraries Used
langchain: A library for building natural language processing pipelines.
Hugging Face Transformers: Provides pre-trained language models and embeddings.
Pinecone: A scalable vector database for storing and retrieving embeddings.
# 3. Data Extraction
The project utilizes the PyPDFLoader and DirectoryLoader from langchain to extract relevant medical information from PDF files. The load_pdf function processes a directory of PDFs, extracting data for further analysis.

# 4. Text Chunking
The text extraction is followed by a text chunking process using the RecursiveCharacterTextSplitter. This helps in breaking down the extracted text into manageable chunks, ensuring efficient processing and retrieval.

# 5. Embedding Model
The project downloads a Hugging Face Embeddings model (sentence-transformers/all-MiniLM-L6-v2) for encoding text into embeddings. These embeddings capture semantic relationships in the medical text data.

# 6. Pinecone Initialization
Pinecone is initialized with the provided API key and environment information. An index named "medical-chatbot" is created to store embeddings for efficient retrieval.

# 7. Creating and Loading Embeddings
The embeddings for each text chunk are created using the Hugging Face embeddings model and stored in Pinecone. Existing indexes can also be loaded for efficient retrieval.

# 8. Question-Answering Setup
A prompt template is defined using the PromptTemplate class, guiding the chatbot on how to answer user queries based on context and questions.

# 9. Retrieval-Based Question-Answering
The CTransformers language model is employed for generating responses, and the RetrievalQA system from langchain integrates document retrieval using Pinecone as a vector store.

# 10. Conclusion
The Intelligent Medical Chatbot project showcases the successful integration of document retrieval techniques and advanced language models. The chatbot effectively assists users with medical queries and presents a promising avenue for further development.
