## TEXT CLASSIFICATION USING BERT FOR LARGE DOCUMENTS - NLP APPLICATION
This project explores techniques to utilize the pre-trained neural network model, Bidirectional Encoder Representations from Transformers (BERT) for large document classification. Since BERT’s maximum input length is 512 tokens, this project presents a solution for classifying large documents by dividing them into chunks of sizes appropriate for BERT. The contextualized word embeddings of the chunks are extracted from BERT, and the embeddings belonging to the same input are combined using statistical methods like mean and variance, or dimensionality-reduction methods like autoencoders. The final input embeddings are then classified with LSTM or transformer architectures and performances were compared for the different combining techniques.

## DATASETS
The datasets need to have lengthy data points to satisfy the criteria of being a large document(>512 words). The following datasets are from various domains and offer the model with a range of contexts to learn from.

1. Consumer Complaints - This dataset contains the financial complaints given by different consumers. This dataset had a maximum of 900 words in a datapoint.
2. Textacy - This dataset contains United States Supreme Court Decisions for a specific period of time. This dataset has large data points that have close to 40000 words.

From these datasets, multiple test datasets were created based on sizes of the data points and the corresponding number of chunks. The “Count_4” implies that the training dataset consists of data points of all sizes except data points with 4 chunks which is the test dataset.

## DIFFERENT COMBINING TECHNIQUES
After obtaining the contextualized word embeddings from BERT, the following combining techniques were implemented:-

1. Stacking chunks
2. Mean of chunks
3. Head and Tail Truncate
4. Covariance of chunks
5. Autoencoders
6. Principal Component Analysis (PCA)

## DEEP NEURAL NETWORK MODELS FOR CLASSIFICATION
The combined embeddings were given as input to the following neural networks to perform the downstream task:-

1. Long Short Term Memory(LSTM)
2. Transformer

## PERFORMANCE EVALUATION
Accuracy and the misclassification error are the evaluation metrics used in this project to compare the performance of different combining techniques.




