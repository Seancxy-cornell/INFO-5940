# INFO 5940 
I have completed and tested the code for the assignment in Codespace provide by my instructor, and it meets all requirements. However, my original Codespace is no longer accessible now. After consulting with my instructor and receiving approval, I am submitting the assignment using my personal Codespace. The primary code is in the chat_with_pdf.py file, while the other required contents are in the readme.md and ref-log.md files.

## Project Overview
A Retrieval-Augmented Generation (RAG) application built with LangChain and Streamlit that enables users to upload text and pdf documents and chat with their content.

## Quick Start

### Installation
```bash
pip install -r requirements.txt
pip install "numpy<2.0" # Because this version offers excellent compatibility.
export API_KEY="your-api-key"
streamlit run chat_with_pdf.py
```

**Usage**
Upload .txt/.pdf files in sidebar
Click "Process Documents"
Start chatting in the main interface
View sources in expandable sections

**Technical Details**
Features Implemented
Core RAG Pipeline (Based on Instructor's Code)
Document chunking with RecursiveCharacterTextSplitter 
ChromaDB vector store with OpenAI embeddings
Similarity search retrieving k=5 document chunks
openai.GPT-4o generation via Cornell API endpoint

Extended Functionality (My Original Work)
Complete Streamlit web interface with chat components
Multi-file upload system supporting .txt and .pdf
Real-time streaming responses
Session state management for multi-turn conversations
Expandable source document display
Comprehensive error handling and user feedback

**Code Integration**
Instructor's Code Patterns Used
Document loading with TextLoader/PyPDFLoader
RecursiveCharacterTextSplitter parameters 
ChromaDB vector store configuration
Basic RAG similarity search approach

My Original Extensions
Full Streamlit UI implementation beyond basic template
Multi-document batch processing system
Real-time response streaming with st.write_stream()
Chat history persistence and management
User interface enhancements and error handling

**Design Choices**
chunk_size=200, chunk_overlap=0: Follows instructor's notebook specification
temperature=0.2: Follows instructor's notebook specification
k=5: Follows instructor's notebook specification
Streaming responses: Implemented for better user experience

**Key Dependencies**
Streamlit (UI framework)
LangChain (RAG pipeline)
OpenAI (Cornell endpoint)
ChromaDB (vector store)

**Configuration**
Used original requirements.txt unchanged provided by my instructor
Added numpy<2.0 for compatibility
All core parameters from instructor's notebook

**Troubleshooting**
1.Ensure API_KEY is set:
To get started，this app requires an API Key. This key acts like a unique token to prove who you are and grant you permission to proceed.
2.Use supported file formats (.txt, .pdf):
The application is specifically designed to read and interpret plain text files (.txt) and Adobe PDF files (.pdf).
3.Large files automatically chunked:
Don't worry about file size. If a document is too large, the system automatically cuts it into smaller chunks, so it can process everything smoothly. You don't need to do anything.





