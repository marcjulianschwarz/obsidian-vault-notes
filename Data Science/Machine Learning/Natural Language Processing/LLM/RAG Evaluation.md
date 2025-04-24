# RAG Evaluation

- Context Retrieval
	- An optimal combination of:
		- chunking
		- embedding model
		- search algorithm
		


- Content Generation
	- Given most relevant retrieved knowledge and question, do we generate reasonable answers?
		- Faithfulness
		- Relevancy
		- Hallucination

- Business Logic
	- Intent verification
	- output length
	- rule compliance
	- 



We need a test set of about 50-100 test cases that we can automatically evaluate with the pipeline. We should save all of the results from that test cases.


AzureML Model Evaluation

https://huggingface.co/learn/cookbook/en/rag_evaluation
https://arxiv.org/pdf/2405.07437


## RAGAS

- Faithfulness
	- grounded in given context
	- context is justification for generated text
	- how does it work
		- given question and answer, create individual statements from the answer and verify that every single one of them can be inferred from the sources and question
		- calculate score based on how many were able to be inferred
- Answer Relevance
	- answer should actually address the question
	- how does it work
		- generate n questions given the answer
		- calculate embedding similarities between the generated questions and the original question and average them
- Context Relevance
	- less but more concentrated information in the context relevant to the question
	- penalize inclusion of redundant information or irrelevant information to the question
	- how does it work
		- extract relevant sentences from the context and calculate percentage of it compared to total number of sentences 
	- 

All of these methods have way higher agreement with human annotators compared to GPT Score or GPT Ranking.