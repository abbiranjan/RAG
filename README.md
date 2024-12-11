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

LLMs are AI models designed to understand and generate human-like text, playing a critical role in natural language processing (NLP) by enabling machines to interpret, analyze, and generate human language.

# Key capabilities of LLM
    - Text generatgion: Creating coherent and contextually relevant text from prompts.
    - Understanding: Comprehending and summarizing large text inputs.
    - Translation: Converting text between languages with high accuracy.

# GPT Generative Pre-trained Transformer
   - Introduced by OpenAI in 2018
   - First large-scale transformer-based language model. Used unsupervised learning on vast text data, followed by fine-tuning.

If problem involves processing of large amount of text and text keeps on changing based on user, then it will be more useful to use model with larger context window than <code>RAG</code> workflow because all the data keeps on changing based on user. So consistency and cost for storing data will be higher than sending entire text to these model and processing that text.

# Types of LLMs
    - Open Source
    - Closed Source

# Open-source model (Can be downloaded)
    Example - LLama 3.1 by Meta, Gemma by Google (Designed to perform smaller tasks). 
    Features - Large-scale model with extensive language capabilities.
    Capabilities - High accuracy in understanding and generating text.
    Use cases - NLP tasks, research and development.

# Closed-Source LLM
    These models are owned by companies and are usually available through paid APIs or services. The source code and underlying model architecture are typically not publicly disclosed.

# Advantages of RAG
    - Improved factual consistency
    - Enhancing domain-specific knowledge
    - Reducing hallucination

RAG enhances LLMs by integrating external information retrieval for more accurate responses.

# Steps
    1. **Query Genaration:**  The model creates a query from the input

    2. **Information Retrieval:** Relevant data is fetched from external sources.

    3. **Response Generation:** The LLMs uses this data to generate a fact-based response.

`Hallucination` refers to the generation of incorrect or fabricated information that the model produces, which is not based  on actual facts or reliable sources.

# Ways to reduce Hallicination
    **1. Contextual Validation**- Cross-checks data from multiple sources to improve accuracy and consistency.

    **2. Dynamic Querying** - Generates context specific queries to retrieve precise, relevant information.

    **3. Information Retrieval** - Fetches relevant data from external sources like Backend, reducing false information by grounding responses in factual content.

    **4. Post-Processing Checks** - Applies checks after response generation to correct inaccuracies before delivery.

# Other ways to train LLMs or domain specific knowledge aprat from RAG
    **1. FINE-TUNING**: Adapts the LLM to specialized knowledge by training it on domain-specific datasets (e.g., medical texts for healthcare queries).

    **2. PROMPT ENGINEERING**: Crafts detailed prompts to guide the LLM in generating accurate, field-specific responses(For example like giving entire legal or technical document).

    **3. DOMAIN-SPECIFIC-RETRIEVAL**: Integrates specialized knowledge bases (e.g. legal databases) for precise relevant information retrieval.
