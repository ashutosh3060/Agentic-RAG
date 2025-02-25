# This file contains running note for RAG Learning


Notebook to follow: [1]_rag_setup_overview.ipynb
https://github.com/ashutosh3060/bRAG-langchain/blob/main/notebooks/%5B1%5D_rag_setup_overview.ipynb  

RAG Quickstart:   
https://python.langchain.com/docs/tutorials/rag/   

2 Main components:
  Indexing: Load, Split, Embed, Store
  Retrieval & Generation: Retrieve & Generate
Load: from langchain_community.document_loaders import WebBaseLoader
Split: from langchain.text_splitter import RecursiveCharacterTextSplitter (for unstructure data)
Embed: from langchain_openai import OpenAIEmbeddings
Store: from langchain_community.vectorstores import PineCone

Retrieval: 
-- # Index
from langchain_community.vectorstores import PineCone
from langchain_openai import OpenAIEmbeddings
retriever = vectorstore.as_retriever(search_kwargs:{"k":1})
Generation:
from langchain_openai import OpenAI
-- Define LLM, prompt, output parsers and then  create chain using prompt | llm | outputparser ("|" passes the output of step1 to step2 and so on) The pipe symbol "|" is used to chain together the functions in the agent dictionary. The output of the first function becomes the input to the next function in the chain


New Libraries to check:
tiktoken: Tiktoken is a free, open-source Python library that tokenizes text. It was developed by OpenAI to work with their large language model.

 
