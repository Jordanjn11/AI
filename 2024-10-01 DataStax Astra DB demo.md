# AI
AI projects &amp; research

- 2024-10-01 - GenAI 101: Getting Started with a Vector Database (DataStax)
- DataStax vector DB = Astra DB

# Summary
![image](https://github.com/user-attachments/assets/890a5f14-2f4f-408d-bc5c-ce3c70b3840c)

- What are vectors and how they represent data
- The challenges in GenAI with ttraditional databased vs. vector databases
- Embeddings and similarity searches important in GenAI app development
- How to use Astra DB as a vector database to get started w/ storing data as vector embeddings

![image](https://github.com/user-attachments/assets/0fb3e8d2-e3ac-472c-8682-ba33a47af155)
![image](https://github.com/user-attachments/assets/2571b0d7-2433-4dc5-bd18-e8aafba63412)

# Questions & Answers
- how does a model assign a vector to a flat panel display so that it appears as "similar" to the crt monitor shown in the example? 
- How much embedding impact a model response?
- I also want to ask how the number of dimensions affects the response (eg 1536 dimension vs whatever the Max is)
- is there a similarity score that gets returned on vector search where an end user knows if it is a 100% identical match or a 80% approximation
- Is Astra DB cassandra under the hood? If so, can the traditional DSE offering also have these vector capabilities ?
- A: Yes Astra DB is indeed Cassandra under-the-hood. And yes, the latest version of DSE (6.9) does have a Vector Search add-on.
- Q: Is LLM like ChatGPT retrieving data from vector DB? 
- A: LLMs are used to generate new content based on prompts and using an underlying generative model. ChatGPT is an LLM. Embeddings models are different - they create embeddings/vector representations based on the input, using an underlying model. When you store data in a vector DB you store both embeddings and data - when you run vector search and retrieve data you are using similarity between embeddings to retrieve it.
- yes there is a similarity score that is returned by the vector search. We often see that any similarity score above .75 is pretty accurate. The scores range from 0-1 (0 being the exact opposite, and 1 being an exact match).
- Q: Is there a way to update a vector or row if new data came about? 
- A: You can replace old/inaccurate data. Would just need an identifier to select the old/bad data

# Notes/Answers
- The models are already trained. You can use them to generate new embeddings for your data. It is not part of the model training

- you can define how many items to return when you run the vector search
- ector DB search tries to find the closest matching vectors and the associated data which can be exact. For example if your search query has a vector that exactly matches something in the DB you will get that back. 

# Resources
Resources: Sign up for Astra DB: https://bit.ly/3zJlQTj 
 DataStax AI PaaS: https://www.datastax.com/products/ai-platform-as-a-service-paas 
 DataStax Docs: https://docs.datastax.com/en/astra-db-serverless/get-started/quickstart.html 
