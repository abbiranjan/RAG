# RAG FLOW
    - User input the query
    - Query will go to framework called Langchain
    - Langchain will be responsible for all the fetching, all of the LLM coordination & all the communication with user.
    - Langchain will do semantic search in Vector Database
    - Vector database will take Contextual data from Original Context and/or new context, if available and update the database and send the data to framework.
    - Now Langchain will create prompt with user query and contextual data and send it to LLM.
    - Now LLM have more contextual data, LLM it process the data with it. 
    - The response from LLM is now more realistic, grounded with factual information.
    - The response now send to framework (Langchain), framework now do some post-processing and send it to user.