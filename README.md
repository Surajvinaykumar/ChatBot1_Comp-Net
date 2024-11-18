#NVIDIA-NIM Chatbot with FAISS and LangChain Integration

##Overview:
The NVIDIA-NIM Chatbot is a Streamlit-based application designed to enable advanced question-answering using NVIDIA's Llama 3.1 Nemotron-70B model. This project integrates LangChain for seamless document processing, FAISS for efficient vector storage and retrieval, and NVIDIA embeddings for high-performance vectorization.

The chatbot processes PDF documents, builds a searchable vector database, and delivers accurate responses based on the provided context. It also includes a feature for displaying document similarity, making it a valuable tool for research, education, and enterprise-level document analysis.
In this project I have added a book on CCNA guide, therefore this helps me in clearing my querries in  computer networks

##Features:
* NVIDIA Embeddings: Utilizes NVIDIA's advanced embeddings for vectorization.
* FAISS Vector Store: Efficiently indexes and retrieves relevant document chunks.
* Document Loader: Automatically processes and parses PDF documents from a directory.
* Custom Text Splitting: Handles long documents with chunking and overlap strategies for optimal retrieval.
* Interactive Chatbot Interface: Streamlit-powered interface for a user-friendly experience.
* Context-Based Responses: Provides answers strictly within the provided context.
* Document Similarity Search: Displays related document sections for enhanced transparency.

##Getting Started:

##Prerequisites
* Python 3.8 or higher
* Dependencies: Install using the provided requirements.txt file.
* NVIDIA API Key: Obtain an API key from NVIDIA's AI endpoints.

##Code Structure:

* app.py: Main Streamlit application.
* books/: Directory for storing PDF files to be processed.
* requirements.txt: List of dependencies required for the project.
* .env: Configuration file for environment variables (API key).

##How It Works:

--Document Embedding:
Loads PDFs from the ./books directory.
Splits documents into smaller chunks using LangChain's RecursiveCharacterTextSplitter.
Embeds the chunks using NVIDIA's embeddings and stores them in a FAISS vector database.

--Retrieval Chain:
Retrieves relevant document chunks using FAISS.
Feeds the chunks into a LangChain stuff document chain.
Uses NVIDIA's Llama 3.1 model to generate a response based on the context.

--Interactive Q&A:
Users input questions through the Streamlit interface.
The application retrieves the most relevant context and generates an answer.

##Customization:

* Modify the chunk_size and chunk_overlap in the RecursiveCharacterTextSplitter configuration for different document types.
* Adjust the LangChain prompt template in the ChatPromptTemplate for specific use cases.
* Add additional preprocessing steps for documents if required.

##Future Enhancements:

* Add support for additional file formats (e.g., DOCX, TXT).
* Enhance scalability for larger datasets using distributed FAISS.
* Implement user authentication and role-based access.
* Add GPU acceleration for faster embeddings and inference.

Contributing:
Contributions are welcome! Please open an issue or submit a pull request with detailed information about your changes.

License:
This project is licensed under the MIT License.

Acknowledgments:
NVIDIA for their Llama 3.1 Nemotron-70B model and embeddings.
LangChain for its robust document processing tools.
FAISS for efficient vector search capabilities.
Streamlit for an intuitive UI framework.


