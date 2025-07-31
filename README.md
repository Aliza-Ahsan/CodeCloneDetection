# CodeCloneDetection
**In large-scale software development, it is common for developers to copy and reuse existing pieces of code. While this practice may accelerate development, it also introduces the problem of code cloning—the presence of duplicated or highly similar code segments within or across software systems. 
Cloned code fragments can lead to several issues: 
- Bug Propagation: A bug in the original code is likely to be present in all its clones. 
- Maintenance Overhead: Any update to a cloned segment must be replicated consistently. 
- Code Bloat: Duplicated code increases the overall size and complexity of the codebase.

To address these issues, this research proposes a deep learning-based framework that integrates transformer-based embeddings with sequence modeling and attention mechanisms. The goal is to overcome the semantic limitations of traditional token-based methods, reduce the complexity of  tree-based approaches, and eliminate the practicality issues of graph-based models. By combining CodeBERT and Word2Vec embeddings with attention and BiLSTM layers, the 
proposed system offers a more accurate, scalable, and semantically aware solution for detecting all types of code clones.**



Our code clone detection system follows a structured deep learning pipeline composed of five main layers. 
Each layer plays a specific role in transforming raw code into meaningful predictions. 
### 1. Input Layer: Accepts two sequences of tokens (e.g., tokenized Java methods). 
These inputs represent the two functions whose similarity (clone or not) we want to predict. Both inputs are padded to a fixed maximum length for uniformity. 
### 2. Embedding Layer: Converts tokens into dense vector representations. 
Each token is mapped to a high-dimensional vector which helps the model understand semantic relationships between code tokens. 
### 3. Fusion Layer: Combines information from both code inputs to capture relationships. 
This fusion step is critical for learning how similar two code snippets are. 
### 4. Classification Layer (BiLSTM + Dense): Learns contextual patterns across token sequences. 
### 5. Output Layer (Sigmoid): Produces the final prediction. 

We have created a BiLSTM neural network that leverages the use of different embedding generation techniques and attention mechanisms, to determine the best way of detecting cloned  codes among two code snippets. Word2Vec and CodBERT are the two methods we have used to generate embeddings, on comparing which we determine which approach was the best.  

### We have developed 4 models of ours:  
### 1. Word2Vec + Dot-product + BiLSTM + Sigmoid 
### 2. Word2Vec + Self-Attention + BiLSTM + Sigmoid 
### 3. Word2Vec + Cross-Attention + BiLSTM + Sigmoid 
### 4. CodeBERT + Dot-Product + BiLSTM + Sigmoid 


## Results 
![image](https://github.com/user-attachments/assets/24f8ffd7-3677-4ddf-a842-30f91e0314d7)
