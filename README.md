## Word Embeddings for Deep Learning 

This notebook loads pre-trained GloVe word embeddings for use in a recurrent neural network.<br>
External libraries used include numpy,nltk<br><br>

Training data is read and an embedding matrix is constructed out to the most common word tokens. Embeddings are pre-trained vectors of 50,100,200, or 300 dimensions from Stanford's Global Vectors for Word Representation,<a href=https://nlp.stanford.edu/projects/glove/> GloVe.</a><br><br>

Optionally we can replace some less frequent words with more frequent ones to decrease our models vocabulary size with less loss of data.<br>
Words in the training data set, but outside our vocabulary (outside words) are compared to words inside the set (inside words) via cosine similarity.
Any outside words that are above a similarity threshold are replaced by their similar inside word. 

  Some examples of word replacements on a small dataset: 

    Replacing contemporary with classical
    Replacing scientists with researchers
    Replacing optimisation with optimization
    Replacing vital with essential
    Replacing emphasis with importance
    Replacing epidemic with disease
    Replacing boost with increase
    Replacing albeit with somewhat
    Replacing aid with help
       
Note this is run with a small vocabulary and low similarity threshold. Typically we only want to replace more obscure, more similar words. Cosine similarity is a simple metric to compare words and utilizing a more sophisticated method of comparing words will increase performance.


Special thanks for GloVe: Jeffrey Pennington and Richard Socher and Christopher D. Manning. 2014 
