![Python version](https://img.shields.io/badge/python-3.9-blue.svg)
## Multi-Modal Reasoning

This notebook demonstrates the implementation of multimodal RAG (mRAG) using an academic article specific to the healthcare domain. mRAGs extract information not only from text but also from other modalities like images, videos, and audio. They are powerful because a significant amount of information can be hidden in images that might not be mentioned in the text.

The main difference between RAG and mRAG is:

* **Text-based RAG:** Takes only text as an input to the retriever. For RAG implementation, please see my repo on [Retrieval Augmentation Generation](https://github.com/necibeahat/Retrieval-Augmentation-Generation).
* **mRAG:** Uses images/videos and other media formats in addition to text as an input.

## mRAG Architecture
![Architecture](/images/AI%20in%20Healthcare.jpg)

## Advantages of mRAG:

* **Richer and more comprehensive knowledge:** Processes both text and visual information.
* **Improved reasoning capability:** Including visual clues can make the model more informed to infer across different data modalities.

## Multimodal Embeddings:

Vector for the input data. The input data can be text, image, and video data. For example, possible use cases could be video content moderation or image classification.

In this notebook I am using Google's Geimini 1.5 Pro LLM. 
### Why Gemini?
These LLMs are multimodal, which means that the models can process information from multiple modalities, including text, images, audio, and video. Reasoning is one of the tasks Gemini performs well in. Gemini is among the top 5 models by [LMSYS ranking](https://lmsys.org/blog/2023-05-25-leaderboard/)


## Limitations:

* **Data dependency:** Needs high-quality paired text and visuals.
* **Computationally demanding:** Processing multimodal data is resource-intensive.
* **Domain-specific:** Models trained on general data may not excel in specialized fields like medicine.
* **Lack of explainability:** Understanding how these models work can be tricky, hindering trust and adoption.

## Installation

This notebook uses Google Cloud Platform.

```bash
! pip3 install --upgrade --user google-cloud-aiplatform pymupdf rich
```

## Libraries

* **__Gemini LLM__:** [Gemini 1.5 Pro](https://console.cloud.google.com/vertex-ai/publishers/google/model-garden/gemini-1.5-pro-001?walkthrough_id=vertex_index&project=gcp-tech-innov-vertexai-6abe) is a foundation model that performs well at a variety of multimodal tasks such as visual understanding, classification, summarization, and creating content from image, audio, and video. It's adept at processing visual and text inputs such as photographs, documents, infographics, and screenshots.

## Data

I used a real-world study on breast cancer that was published in 2020. Here is the [link](https://bmccancer.biomedcentral.com/articles/10.1186/s12885-020-6527-y). The model works better with high-resolution images. I have also downloaded the chart used in the article to aid performance.
