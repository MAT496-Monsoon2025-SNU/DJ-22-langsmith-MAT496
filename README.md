# Intro to Langsmith

## Module 0

The code was written in accordance with OpenAI libraries and commands in python. I have changed everything to work with groq, the model provider that i am familiar with already.

### rag_application.ipynb

[https://github.com/MAT496-Monsoon2025-SNU/DJ-22-langsmith-MAT496/blob/main/notebooks/module_0/rag_application.ipynb]()

Changes:

* Changed client to **Groq()**
* Changed model provider to **groq**
* Changed model to **openai/gpt-oss-20b**
* Changed the question in the prompt

### utils.py

[https://github.com/MAT496-Monsoon2025-SNU/DJ-22-langsmith-MAT496/blob/main/notebooks/module_0/utils.py]()

Changes:

* Changed embedder to **HuggingFaceEmbeddings** using **sentence-transformers/all-MiniLM-L6-v2 model**

### requirements.txt

[https://github.com/MAT496-Monsoon2025-SNU/DJ-22-langsmith-MAT496/blob/main/requirements.txt]()

Changes:

* **langchain-groq**
* **groq**
* **sentence-transformers**

## Module 1

### Video 1: Tracing Basics

[https://github.com/MAT496-Monsoon2025-SNU/DJ-22-langsmith-MAT496/blob/main/notebooks/module_1/tracing_basics.ipynb]()

Learnt how **@traceable** decorator works and how it makes it simple to log traces. It makes it easier to add metadata. The step-by-step breakdown makes debugging easier and adding metadata makes filtering and grouping simpler.

Changes:

* Made a simple **chat_bot()** to ask questions.
* Added **metadata** to ask questions related to chess

### Video 2: Types of Runs

[https://github.com/MAT496-Monsoon2025-SNU/DJ-22-langsmith-MAT496/blob/main/notebooks/module_1/types_of_runs.ipynb]()

Learnt how to **trace** using **LangSmith**. It is more efficient than logging as in logging it is more difficult to find root cause of the error.

Different types of runs provided by LangSmith:

* **LLM**: Invokes an LLM
* **Retriever**: Retrieves documents from databases or other sources
* **Tool**: Executes actions with function calls
* **Chain**: Default type; combines multiple Runs into a larger process
* **Prompt**: Hydrates a prompt to be used with an LLM

Changes:

* Made the **chat_model** into a Beef Wellington recipe provider
* Made the **my_streaming_chat_model** into an Australian bartender
* Made **retrieve_docs** into a retreiver for available drinks in a bar
* Made the **ask_about_the_weather** consult Reynold Wolf for the temperature
* Made a **new model** that decides chess strategems in medieval theme

### Video 3: Alternative Ways to Trace

[https://github.com/MAT496-Monsoon2025-SNU/DJ-22-langsmith-MAT496/blob/main/notebooks/module_1/alternative_tracing_methods.ipynb]()

Learnt alternative ways to trace function call in LangSmith. **wrap_openai()** uses **OpenAI SDK** directly to trace all openai calls, so any calls made to it will automatically be traced to LangSmith.

Changes:

* Made my earlier **chat_bot** from **tracing_basics.ipynb** using **wrap_openai()**

### Video 4: Conversational Threads

[https://github.com/MAT496-Monsoon2025-SNU/DJ-22-langsmith-MAT496/blob/main/notebooks/module_1/conversational_threads.ipynb]()

Learnt how to create and execute tasks in a their own threads. By passing **uuid** as a pair value in the metadata using **langchain_extra** field, we can create threads.

Changes:

* Made my earlier **chat_bot** from **tracing_basics.ipynb** to trace all the prompts provided by the user by creating a new **uuid** whenever chatbot is called. It tracks all the traces related to any particular conversation between the user and the llm.

## Module 2

### Video 1: Datasets

[https://github.com/MAT496-Monsoon2025-SNU/DJ-22-langsmith-MAT496/blob/main/notebooks/module_2/dataset_upload.ipynb]()

Learnt that **datasets** are a mainly a list of **examples** used to evaluate the llm application. **Tagging** a particular version of a dataset helps in testing our llm application as we can go back and see what changed between particular tags.

Changes:

* Made a **new dataset** based on FC Barcelona's historical 2009 Sextuple run
