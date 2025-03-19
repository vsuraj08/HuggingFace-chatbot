# Conversational RAG with PDF Uploads and Chat History

## Overview
This project implements a Conversational Retrieval-Augmented Generation (RAG) system that allows users to upload PDF files and engage in a chat with their content. The application utilizes Streamlit for the user interface, LangChain for managing document retrieval and chat history, and Groq API for LLM-powered responses.

## Features
- **PDF Uploads**: Users can upload multiple PDF files to extract and query their content.
- **Conversational RAG**: The system maintains chat history and uses it to provide context-aware responses.
- **Session Management**: Users can input a session ID to store and retrieve chat history for different interactions.
- **Embeddings and Vector Store**: Utilizes `HuggingFaceEmbeddings` to create vector representations of document chunks stored in Chroma DB.
- **Standalone Question Formulation**: Reformulates user queries into standalone questions when needed for better retrieval.
- **Concise and Contextual Answers**: Provides short, to-the-point responses based on the retrieved context.

## Technologies Used
- **Streamlit**: For building the interactive web UI.
- **LangChain**: For retrieval, chat history management, and LLM integration.
- **ChromaDB**: As a vector database to store document embeddings.
- **Groq API**: Provides LLM-based responses.
- **Hugging Face Embeddings**: Used for document embedding (`all-MiniLM-L6-v2`).
- **PyPDFLoader**: Extracts text from uploaded PDF documents.
- **RecursiveCharacterTextSplitter**: Splits documents into manageable chunks for vector storage.

## Installation & Setup
### Prerequisites
- Python 3.8+
- Pip
- A valid Groq API key
- A Hugging Face API token (HF_TOKEN)

### Installation Steps
1. Clone this repository:
   ```sh
   git clone https://github.com/vsuraj08/HuggingFace-chatbot.git
   cd conversational-rag
   ```
2. Create a virtual environment:
   ```sh
   python -m venv env
   source env/bin/activate   # On Windows use `env\Scripts\activate`
   ```
3. Install dependencies:
   ```sh
   pip install -r requirements.txt
   ```
4. Set up environment variables:
   Create a `.env` file in the root directory and add the following:
   ```ini
   HF_TOKEN=your_huggingface_token
   ```
5. Run the Streamlit application:
   ```sh
   streamlit run app.py
   ```

## Usage
1. Open the Streamlit web interface.
2. Enter your Groq API key.
3. Upload one or more PDF files.
4. Provide a session ID for chat history tracking.
5. Ask questions based on the uploaded PDFs and receive context-aware responses.

## Project Structure
```
├── app.py                     # Main Streamlit application
├── requirements.txt           # Required dependencies
├── .env                       # API keys (not included in repo)
├── temp.pdf                   # Temporary storage for uploaded PDFs
└── README.md                  # Project documentation
```

## Future Enhancements
- Implement multi-session persistence with a database.
- Support for additional file types (e.g., Word, TXT).
- Improve UI with enhanced visualization.
- Add summarization capabilities for uploaded documents.

## Contributing
Contributions are welcome! Feel free to fork the repository, open issues, and submit pull requests.

## License
This project is licensed under the MIT License.
