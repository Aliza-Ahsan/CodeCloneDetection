# CodeCloneDetection

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


## Results 
![image](https://github.com/user-attachments/assets/24f8ffd7-3677-4ddf-a842-30f91e0314d7)
