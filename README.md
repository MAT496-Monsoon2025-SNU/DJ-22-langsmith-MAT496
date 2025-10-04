# Intro to Langsmith

## Module 0

The code was written in accordance with OpenAI libraries and commands in python. I have changed everything to work with groq, the model provider that i am familiar with already.

### rag_application.ipynb

* Changed client to **Groq()**
* Changed model provider to **groq**

* Changed model to **openai/gpt-oss-20b**

* Changed the question in the prompt

### utils.py

* Changed embedder to **HuggingFaceEmbeddings** using **sentence-transformers/all-MiniLM-L6-v2 model**

### requirements.txt

Added

* **langchain-groq**
* **groq**
* **sentence-transformers**
