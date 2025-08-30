# ChatBot


## Complete RAG Flow from Dataset to Response

### Phase 1

```
1. Raw Dataset (PDFs, docs, websites, etc.)
   ↓
2. Document Loader
   • Loads and reads different file formats
   • Extracts raw text content
   ↓
3. Text Splitter  
   • Breaks documents into manageable chunks
   • Handles overlaps to maintain context
   ↓
4. Embedding Model
   • Converts text chunks into vector embeddings
   • Each chunk becomes a numerical vector
   ↓
5. Vector Database
   • Stores embeddings with metadata
   • Creates searchable index

```

### Phase 2

```
6. User Query
   • User asks a question
   ↓
7. Chain (Orchestrator)
   • Coordinates the entire process
   • Manages the flow between components
   ↓
8. Retriever
   • Takes user query
   • Converts query to embeddings
   • Performs similarity search in vector DB
   • Returns top-k most relevant chunks
   ↓
9. Prompt Template
   • Takes retrieved chunks + user query
   • Formats them into a structured prompt
   • Adds instructions for the LLM
   ↓
10. Large Language Model (LLM)
    • Receives the formatted prompt
    • Generates answer based on retrieved context
    ↓
11. Response Processing
    • Chain may post-process the response
    • Returns final answer to user
    
```