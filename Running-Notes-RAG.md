# This file contains running note for RAG Learning


Notebook to follow: [1]_rag_setup_overview.ipynb
https://github.com/ashutosh3060/bRAG-langchain/blob/main/notebooks/%5B1%5D_rag_setup_overview.ipynb  

RAG Quickstart:   
https://python.langchain.com/docs/tutorials/rag/   

2 Main components:
  Indexing: Load, Split, Embed, Store
  Retrieval & Generation: Retrieve & Generate
1. Indexing >
Load: from langchain_community.document_loaders import WebBaseLoader
Split: from langchain.text_splitter import RecursiveCharacterTextSplitter (for unstructure data)
Embed: from langchain_openai import OpenAIEmbeddings
Store: from langchain_community.vectorstores import PineCone

2. Retrieval & Generation >
Retrieval: 
-- # Index
from langchain_community.vectorstores import PineCone
from langchain_openai import OpenAIEmbeddings
retriever = vectorstore.as_retriever(search_kwargs:{"k":1})
Generation:
from langchain_openai import OpenAI
-- Define LLM, prompt, output parsers and then  create chain using prompt | llm | outputparser ("|" passes the output of step1 to step2 and so on) The pipe symbol "|" is used to chain together the functions in the agent dictionary. The output of the first function becomes the input to the next function in the chain

Orchestration platform for retrieval & generation: **LangGraph** 
Check how not to use LangGraph and stiil achieve it by using LangChain !

What is invocation mode ?   
* The specific method used to trigger the retrieval process and feed relevant information to the LLM when generating a response to a user query.
* Essentially, it determines how the LLM accesses and utilizes external data sources to enrich its response based on the current context of the query.   
Different types of invocation mode:
1. Batched calls: Sending multiple queries to the language model at once to be processed together.
2. Async calls: allow sending multiple requests without waiting for each response individually
3. Streaming: receiving the model's output in chunks as it generates it, allowing for near-real-time feedback.
   Essentially, batching improves efficiency by grouping requests, async allows parallel processing, and streaming provides continuous output as the model generates it.

To use LangGraph, we need to define three things:
  The state of our application
  The nodes of our application (i.e., application steps);
  The "control flow" of our application (e.g., the ordering of the steps)


New Libraries to check:
tiktoken: Tiktoken is a free, open-source Python library that tokenizes text. It was developed by OpenAI to work with their large language model.

 
