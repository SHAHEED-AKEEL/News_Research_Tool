# News Research Tool (NRT) 📈
This project is a streamlit app that enables users to perform question answering and research over news articles by leveraging the capabilities of the LangChain framework, OpenAI language models, and FAISS vector stores for semantic search.

## Features
URL-based News Data Loading: Users can input up to three news article URLs, which the tool loads and processes using the UnstructuredURLLoader from LangChain.

Text Chunking: Large article texts are split into manageable chunks using configurable text splitting strategies (RecursiveCharacterTextSplitter), respecting LLM token limits and enabling more efficient retrieval.

Embeddings & Semantic Search: Chunks are embedded using OpenAI embeddings, and stored in a local FAISS vector store to enable fast, semantically aware document retrieval.

Retrieval-Augmented Generation: Given a user query, relevant article content is semantically retrieved and passed to an OpenAI language model (via LangChain’s RetrievalQAWithSourcesChain) to provide accurate, contextually grounded answers with supporting sources.

User Interface with Streamlit: The app provides a streamlined interface for URL entry, question input, and display of both generated answers and referenced sources.

 
## Usage:
Environment Setup:    
Requires Python and the following packages: streamlit, langchain, faiss-cpu, openai, sentence-transformers, dotenv, and their dependencies.      
Store your OpenAI API key in a .env file.

Start the App:         
Run the Streamlit app (main.py).         
Enter up to 3 news article URLs in the sidebar.         
Click “Process URLs” to load and process news content.        

Ask Questions:
Type your research question in the main interface.           
The tool retrieves the relevant text from the indexed articles and generates an answer using the latest LLM.            

Review Sources:     
Each answer includes references to the sourced articles for transparency.      

## Technical Highlights:      
Document Loading: Utilizes loaders for plain text, CSV, and unstructured URL content with metadata support.    

Text Splitting: Demonstrates both manual and automated chunking, including character-based and recursive splitting for robust adaptation to LLM context limits.       

Vector Indexing & Retrieval: Leverages FAISS for scalable similarity search; saves and loads indices using pickle.     

Extensible: Code structure and comments allow easy adaptation for more file types, new prompt designs, and additional LLM backends.      

## Example Technologies Shown
LangChain’s TextLoader, CSVLoader, UnstructuredURLLoader     

Text splitting techniques (CharacterTextSplitter, RecursiveCharacterTextSplitter)      

OpenAI embeddings & FAISS similarity search      

Streamlit interactive UI          

### This project is ideal for learning or demonstration of retrieval-augmented generation techniques, with special emphasis on practical applications in news analytics and research.

