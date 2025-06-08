
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


## Build a search engine, not a vector db

Building a good RAG system relies on having a great retrieval step. Make sure that the retrieval step is not only a vector db semantic similarity search but a proper search engine. 

This also allows for a clear separation of the search and generate part of RAG. You will have **two great products**, a search engine and a chat interface to your data.

- https://blog.elicit.com/search-vs-vector-db/
- https://saeedesmaili.com/notes/build-a-search-engine-not-a-vector-db/
