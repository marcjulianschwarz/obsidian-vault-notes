# Knowledge Base LLM 

Use a [[Vector Database]] to retrieve source knowledge from a [[Knowledge Base (Prolog)]] and let an [[Large Language Model|LLM]] use the source to generate answers. 

## Create Knowledge Base 

First we want to create a [[Knowledge Base (Prolog)]] that the [[Large Language Model|LLM]] can reference for answering questions.

It also helps to 
- Improve embedding accuracy for better results.
- Reduce text input to improve LLM efficiency.
- Provide precise information sources for users.
- Split long chunks of text that exceed context window.

## Step by Step 

1. [[Tokenization|Tokenize]] the text (e.g. with tiktoken).
2. Use langchains RecursiveCharacterTextSplitter to generate chunks of text 
3. Create [[Embedding|Embeddings]] for all chunks 
4. Initialize a [[Vector Database]] and store the vectors in there 
5. Use the RetrievalQA chain with a [[Large Language Model|LLM]] and the [[Vector Database]] to generate answers for questions 
6. We can also use the RetrievalQAWithSourcesChain to make the answers even more reliable.
