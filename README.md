# **Semantic Caching with Embedding Models**

## **Project Overview**
This project explores the impact of embedding models on semantic caching in large language models (LLMs). By implementing a modular caching solution, this research aims to reduce the redundant computations that arise from the stateless nature of LLMs like GPT-4o, Claude AI Sonnet, and Gemini 1.5. The approach leverages various embedding models for semantic similarity evaluation and integrates a two-layer caching mechanism to optimize performance.

The key components of the system include:

- **GPTCache**: An open-source Python library for caching responses from LLMs.
- **SQLite**: Used for efficient query caching.
- **FAISS**: A library designed to handle vector similarity search and embedding storage.
- **SbertCrossencoder**: A similarity evaluation model used to differentiate cache hits and misses based on a threshold of 0.7.

Through a series of experiments using the Quora Question-Paired dataset, the project demonstrates how caching can improve the efficiency of LLM-based systems, especially in real-world applications such as chatbots and knowledge-sharing systems.

## **Notebooks Overview**

1. **custom_semantic_caching_ranking.ipynb**  
   This notebook serves as the primary implementation for the ranking mechanism in semantic caching. It demonstrates how different embedding models impact the cache hit-and-miss ratios, response latency, and overall cost-efficiency. The notebook implements a two-layer caching system with both L1 and L2 embeddings to manage redundant queries and optimize performance.

2. **custom_semantic_caching_quora.ipynb**  
   In this notebook, the focus is on evaluating the performance of the caching system using the Quora Question-Paired dataset. The notebook contains the methodology for calculating cache hit rates, token savings, and other metrics relevant to measuring the system's effectiveness.

3. **custom_semantic_caching.ipynb**  
   This notebook contains the foundational code for the caching mechanism. It demonstrates how embedding models are integrated with the caching system, along with the necessary steps for storing and retrieving query-response pairs from the cache.

4. **Cached Embeddings and Results With Bert.ipynb**  
   This notebook explores the use of BERT embeddings for caching purposes. It evaluates the performance of BERT embeddings for different query pairs and compares them to other embedding models in terms of cache hit rates and efficiency.

5. **semantic caching with GPT cache.ipynb**  
   The final notebook highlights the use of GPTCache, integrating GPT-3/4 responses with semantic caching. The notebook demonstrates how to effectively combine embeddings, SQLite, and FAISS to build a highly efficient cache system that reduces redundant LLM computations and latency.

## **Key Findings**
- **Cache Hit and Miss Ratios**: By leveraging embeddings, we achieve significantly higher cache hit rates, especially when semantic similarity is high.
- **Token Savings**: Caching reduces the number of tokens sent to LLMs, leading to reduced costs and improved performance.
- **Cost Efficiency**: Through caching, both prompt and completion tokens are minimized, resulting in cost savings and lower computational overhead.

## **Future Work**
The system can be further optimized for even greater accuracy and efficiency. We plan to explore the following areas for future enhancement:
- Integrating more advanced eviction policies.
- Experimenting with additional embedding models.
- Scaling the system to handle larger datasets and more complex queries.

## **Repository Structure**
- `custom_semantic_caching_ranking.ipynb`: Core notebook for ranking and caching experiments.
- `custom_semantic_caching_quora.ipynb`: Evaluation using the Quora dataset.
- `custom_semantic_caching.ipynb`: Foundational caching code.
- `Cached Embeddings and Results With Bert.ipynb`: Experiment with BERT embeddings.
- `semantic caching with GPT cache.ipynb`: Integration with GPT-3/4 for semantic caching.

## Contributors

- **Shervin Ghaffari**: shervinghaffari79@gmail.com
- **Ali Noghabi**: a.noghabi2002@gmail.com
- **Maryam Sadeghabadi**: miryamsadeghi82@gmail.com
