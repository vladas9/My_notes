---
Date: 2024-04-16
tags:
  - project
  - programming
  - python
  - AI
---
# Sort plan of action 
1. **Data Collection**: Gather a large dataset of programming code. This could be from open-source repositories or other sources. Ensure that the data is labeled, i.e., pairs of code snippets are marked as plagiarized or not.
    
2. **Preprocessing**: Preprocess the code to a format that can be fed into a neural network. This could involve tokenization (breaking the code into individual ‘tokens’ like keywords, identifiers, operators, etc.), removal of comments and white spaces, and normalization (like changing all variable names to a common token).
    
3. **Model Building**: Build a neural network model. A possible approach could be to use a Siamese network, which takes in two code snippets and outputs whether they are similar or not. Another approach could be to use a sequence-to-sequence model like a Transformer, which can understand the context of the code better.
    
4. **Training**: Train the model on preprocessed dataset. I might need to experiment with different architectures, hyperparameters, and optimization algorithms to get the best performance.
    
5. **Evaluation**: Evaluate the model on a separate test set to check its performance. Common metrics for this task could be accuracy, precision, recall, and F1 score.
    
6. **Deployment**: Once the model performance satisfies, it's time to deploy it to start checking for code plagiarism.

# Data collection 
### Ideas 
1. The main idea is to make a python script that will parse files with code from different GitHub repositories(by file extensions "py" or "cpp") and that to make a data set from this files

# Preprocessing
### Ideas 
1. To make a tokenizer for code
	- It will change all the key work by tokens that will express the meaning of them
	- It will tokenize all the variables by one type of token(To omit the change of name to hide the plagiarism)
	Using tokenizer can help to understand the main way how the code is working and to train the Model to understand how to compare the logic of the codes.


## References 
1. 