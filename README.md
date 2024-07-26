# Multi-Modal-Reasoning

This notebook shows implementation of multimodal RAG (mRAG) using an academic article that is specific to the healthcare domain. 

The main difference between RAG and mRAG is that 
- Text based RAG: takes only text as an input to the retriever
- mRAG: uses images/videos and other media format in addition to text as an input

## Advantages of mRAG:
- Richer and more comperehensive knowledge as it processses both text and vidual infomration
- Improve reasoning capability: Including visual clues can bmake the model more informrmed to infer accrss different data modalities

## Multimodal embeddings:
Vector for the iniput data. The inout data can be text, image and video data. For example a possible use cases could be video content moderation or image classification

## Limitations:
- Data dependency: Needs high-quality paired text and visuals.
- Computationally demanding: Processing multimodal data is resource-intensive.
- Domain specific: Models trained on general data may not shine in specialized fields like medicine.
- lack box: Understanding how these models work can be tricky, hindering trust and adoption.
