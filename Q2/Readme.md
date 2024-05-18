# Q2. Chatbot Using RAG and Attention Mechanism

Developed a RAG system which answers questions regarding Tamilnadu government budget estimate for the year 2024-2025. I have chosen this document because the information regarding budget estimate is very recent and can not be included in any model training dataset. Here due to resource constraints, I have used only single document with 26 pages as knowledge base for RAG application. This RAG application from building till evaluation is completely open source and does not involve any paid API key usage. Also, it is easy to run in any local system and understand the basic building blocks of RAG application.

Two main RAG application blocks:
1. Retriever : Best RAG application has bert-base-uncased as embedding model.
2. Generator : Phi3 as generator.

### RAG evaluation block:
Any developed RAG application is evaluated using GPT 4 model but due to cost constraint, I have used llama3 model. It is the most capable openly available LLM to date by the meta AI team. It is quite bigger and perform better than phi3 model which we used as generation model in our RAG application.

I have created my own test dataset. 10 short answer questions are prepared from the knowledge base document using online free AI tool. RAG model is evaluated based on answering of those 10 questions.

Evaluation criterion:
1. Appropriateness 
2. Relevance
3. Hallucination

A single score is given based on above criterion by llama3 model. 
One feedback about response of the model and one feedback about hallucination of the model response is also given. 

These evaluation results is stored in separate csv file for reference.

### About two version of file in repository:

Two main RAG application blocks:
1. Retriever
2. Generator

Here a good retriever make significant role. So in initial RAG model, I have used same phi3 model embedding as my embedding model for retriever. But the performance of the model is quite low. So I have used bert-base-uncased as my embedding for retriever, which significantly improved the performance. bert-base-uncased is trained on large amount of English data and produce embedding with good inner representation. 

Score:
1. With phi3 embedding: 0.45/1
2. With bert-base-uncased embedding : 0.65/1

Other ways to improve RAG application performance:
1. Changing chunking size of the document.
2. Reranking -  In re-ranking the documents are rearranged and filtered so that the most relevant ones are ranked highest.
3.Query transformation


## Steps to run the file in local machine:

1. Download ollama from https://ollama.com/ and install in the laptop.
2. Follow the instruction mentioned in the https://ollama.com/ for successful installation. 
3. Download the model of interest from ollama model repository. 
4. Here I have downloaded phi3 for RAG system and llama3 for evaluation of RAG system.
5. run requirements.txt file for installing necessary libraries. 
6. Now run the demo_rag.ipynb file to test the rag model. The file contain default question, change the question of your interest to test the rag model.





