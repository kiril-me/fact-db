# Fact DB

The idea is to create the database as described in Reading Wikipedia to Answer Open-Domain Questions (Danqi Chen) [https://arxiv.org/pdf/1704.00051.pdf] . The Document Retriever component. 

Store knowledge as paragraphs of preprocessed text, that after can be used with ML algorithms. The approach combines a search component based on bigram hashing and TF-IDF matching. The machine read the text and stored it as a knowledge. This improves the speed of answering by narrow the search space and focus on reading only articles that are likely to be relevant. These articles are sent it to machine learning algorithm to identify the answer spans from those articles. We can encode each paragraph once and concentrate on ML algorithm. Paragraph encoding can contain word embeddings, part-of-speech,  named entity recognition tags and term frequency.

The database should be elastically extended to any kind of NLP structures. How to represent the knowledge I leave this decision to ML researchers. The database should be simple (no SQL only NLP) and allow easy to use with any ML tools.

# Publications
Reading Wikipedia to Answer Open-Domain Questions (Danqi Chen) [https://arxiv.org/pdf/1704.00051.pdf]
Distributed Representations of Sentences and Documents (Quoc Le and Tomas Mikolov) [https://cs.stanford.edu/~quocle/paragraph_vector.pdf]
https://github.com/facebookresearch/Starspace

# Plan

1. Find correct wait of processing and store text data. Posible Spark with Lucene combination.
2. Prepare dataset and make simple test how it possible can work.
3. Design extensible system.
4. Implement connectors to DeepLearning tools.
5. Document and release product.

