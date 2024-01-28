# RAG PDF QA

## Introduction

This repository contains the code for the RAG PDF QA project.
The project contains two notebooks that create the rag retriever.
Specifically, one uses llamaIndex and the other Langchain.

Both notebooks use mistral-7b as the language model, that is running locally on a GPU, pulled from Ollama.

### LlamaIndex

The notebook `llamaindex.ipynb` contains the code for the retriever that uses llamaIndex.
It reads the 50-page pdf file and creates a retriever that can be used to retrieve the most relevant page for a given
question.

### Langchain

The notebook `ollama_langchain.ipynb` contains the code for the retriever that uses Langchain.
For a vectorstore ChromaDB is used, which is created from the 50-page pdf file.

This notebook also makes evaluation of the retriever possible, using the QARetrieval Chain more specifically,
generating relative question-answer pairs from the pdf file and retrieving the most relevant answer for a given question
from the rag retriever and the QARetrieval Chain evaluates the retrieved answer.
