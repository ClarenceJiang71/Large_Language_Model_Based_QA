# Large_Language_Model_Based_QA

Large Language Models (LLM) like GPT-4 and PaLM are nowadays really "overpowered", acting as an excellent knowledge base that accurately answers user questions. However, LLM lacks the latest data and private company data. The goal is to explore how LLM, like GPT-4, could help answer user questions about MD.ai, which clearly requires detailed MD.ai documentation that is not included in the training data. Also besides general conceptual questions, we want to make GPT-4 able to give information and metadata for a specific user. Finally, another goal is to make GPT-4 generate code that really works with the MD.ai cloud platform application.  

There are 3 methods: 

1. Prompt engineering. Using pure prompt engineering to solve everything is not realistic since there is always the token limit issue, but prompt engineering is an indispensable part of all other methods; LLM serves more like a black box, and you cannot control the output programmatically, so prompt engineering becomes so important.
2. A pure Google-Cloud-based QA system using Matching Engine as a vector database. Using a vector database helps solve the token limit issue, but causes extra storage cost and cost that uses Google vertex AI. Also, the PaLM model does not follow instructions well as compared to GPT-4. 
3. Using the external URL read function in MD.ai chat to manually input the related context

There is an extra function related to code generation. I wrote an external function that takes code as input and outputs a valid Colab notebook link that contains that code input. The goal is not only to provide the code but also an environment for users to run their required codes. 
