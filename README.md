# word_embeddings

Load pre-trained GloVe word embeddings for use in a recurrent neural network.
External libraries used include numpy,nltk

Training data is read and an embedding matrix is constructed out to the most common word tokens. Embeddings are pre-trained vectors of 50,100,200, or 300 dimensions from Stanford's Global Vectors for Word Representation, GloVe. https://nlp.stanford.edu/projects/glove/

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
       
Note this is run with a small vocabulary and low similarity theshold. Typically we only want to replace more obscure, more similar words.


Special thanks for GloVe: Jeffrey Pennington and Richard Socher and Christopher D. Manning. 2014 
