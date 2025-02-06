# LlamaDoc_Q-A
A LangChain, FAISS, LlamaIndex powered chatbot that processes PDFs, TXT, and DOCX files to provide intelligent answers using Streamlit for an interactive UI.
Steps:
1. Loading Documents using LlamaIndex:
loaded the document from the PDF
extracted the text using the LlamaIndex reader.

2. Chunk and Embed Text using FAISS:
After extracting the text, the next task is to chunk it into smaller pieces using a text splitter, used langchain's RecursiveCharacterTextSplitter
Once chunked, the next step is to embed the text using FAISS for efficient similarity search.

3. Used LangChain for Q&A:
After chunking and embedding, used LangChain to link the document chunks with the GPT model. The LangChain query FAISS to find relevant chunks based on a user's input and pass them to the GPT model for answering.

4. Built a Streamlit App for User Interaction:
Once the backend (embedding, searching, and querying) is set up, we moved to Streamlit to create an interactive UI for the user to upload a document and ask questions about it.
