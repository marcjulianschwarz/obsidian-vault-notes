---
aliases:
  - LLM
  - LLMs
  - Large Language Models
---


- [[In-Context Learning]]
- https://github.com/nomic-ai/gpt4all
- https://github.com/h2oai/h2ogpt
- Fine-tuning with[[Low-Rank Adaptation|LoRA]]




## RAG, or anything similar

- RRF (Reciprocal Rank Fusion)
	- send user query to multiple retrievers 
	- get rankings from all retrievers
	- fuse rankings and create final ranking based on RRF scores


> Last but not least, simply throwing the documents into the ingestion pipeline will not be sufficient. You need a careful strategy and probably need to "segment" the documents into logical groups (Determined by your use-case/Content type) and use a "smart query router" to route it to the right Vector DB.


- Enrichment of chunks
	- add metadata to the chunk (for example title, document name, etc.)
	- can be quite creative with this
	- contextualizing chunks (otherwise it is really hard to choose the correct chunk)
- Post-Retrieval bm25 / reranking





