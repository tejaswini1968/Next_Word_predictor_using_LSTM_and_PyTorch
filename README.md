Project Title: Next Word Predictor using LSTM and PyTorch
Step 1: Problem Statement
Developed a deep learning-based language model to predict the next word in a sequence using Long Short-Term Memory (LSTM) networks. The objective was to train a model that learns contextual relationships between words and generates the most probable next word for a given input sequence.
Step 2: Data Collection and Text Preprocessing
•	Used a sample essay containing approximately 2000 words as the training corpus.
•	Processed the text using the NLTK library.
•	Tokenized the text using word_tokenize to split the document into words.
•	Built a word-to-index vocabulary dictionary consisting of all unique words in the corpus.
•	The final vocabulary size was 622 unique words.
Step 3: Sequence Generation
•	Split the document into 99 sentences and converted each sentence into numerical form using the vocabulary dictionary.
•	Generated growing left-to-right sequences for next word prediction.
•	Created a total of 1574 input-output training sequences.
•	The maximum sequence length obtained was 39, where the first 38 words are used as input and the last word is used as the target output.
Step 4: Data Preparation
•	Applied zero pre-padding to ensure all sequences have a fixed length of 39.
•	Converted the padded sequences into PyTorch tensors.
•	Created input features X using all words except the final word in each sequence.
•	Created target labels y using the final word of each sequence.
•	Built PyTorch Dataset and DataLoader objects for efficient batch processing during training.
Step 5: LSTM Model Architecture
Designed and implemented an LSTM-based language model in PyTorch with the following architecture:
•	Embedding layer with embedding dimension of 100.
•	Two stacked LSTM layers with hidden size 150.
•	Dropout layer with dropout rate 0.3 to reduce overfitting.
•	Fully connected output layer with 622 output neurons, corresponding to the vocabulary size.
Step 6: Model Training
•	Trained the model using Google Colab GPU accelerator for faster computation.
•	Used Cross-Entropy Loss as the loss function.
•	Selected the Adam optimizer with a learning rate of 0.001.
•	Trained the model for 50 epochs.
•	Implemented a custom training loop to compute and monitor the average training loss for each epoch.
Step 7: Prediction and Text Generation
•	Created an index-to-word dictionary by reversing the word-to-index mapping.
•	Implemented a prediction function to generate the most probable next word for a given input text.
•	Developed an autoregressive text generation function that repeatedly predicts the next word to generate text sequences of arbitrary length.
Step 8: Results
•	Successfully trained the LSTM language model on the prepared corpus.
•	Achieved a training accuracy of 96.95% on the next word prediction task.
•	Demonstrated the model's capability to learn contextual word relationships and generate coherent word sequences using autoregressive prediction.

