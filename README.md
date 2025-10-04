# Intro to Langsmith

## Module 0

The code was written in accordance with OpenAI libraries and commands in python. I have changed everything to work with groq, the model provider that i am familiar with already.

### rag_application.ipynb

[https://github.com/MAT496-Monsoon2025-SNU/DJ-22-langsmith-MAT496/blob/main/notebooks/module_0/rag_application.ipynb]()

* Changed client to **Groq()**
* Changed model provider to **groq**
* Changed model to **openai/gpt-oss-20b**
* Changed the question in the prompt

### utils.py

[https://github.com/MAT496-Monsoon2025-SNU/DJ-22-langsmith-MAT496/blob/main/notebooks/module_0/utils.py]()

* Changed embedder to **HuggingFaceEmbeddings** using **sentence-transformers/all-MiniLM-L6-v2 model**

### requirements.txt

[https://github.com/MAT496-Monsoon2025-SNU/DJ-22-langsmith-MAT496/blob/main/requirements.txt]()

Added

* **langchain-groq**
* **groq**
* **sentence-transformers**

## Module 1

### Video 1: Tracing Basics

[https://github.com/MAT496-Monsoon2025-SNU/DJ-22-langsmith-MAT496/blob/main/notebooks/module_1/tracing_basics.ipynb]()

Learnt how **@traceable** decorator works and how it makes it simple to log traces. It makes it easier to add metadata. The step-by-step breakdown makes debugging easier and adding metadata makes filtering and grouping simpler. 

* Made a simple **chat_bot()** to ask questions.
* Added **metadata** to ask questions related to chess
