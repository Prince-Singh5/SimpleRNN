Sentiment Analysis on IMDB Reviews using Simple RNN 🎬🧠

📖 Project Overview
This project is an end-to-end deep learning pipeline built with Keras and TensorFlow to classify IMDB movie reviews as positive or negative.
The model leverages a Simple RNN (Recurrent Neural Network) architecture to capture sequential dependencies in text data, making it suitable for sentiment analysis tasks.


Dataset
  Source: IMDB dataset from Keras.
  Size: 50,000 reviews (25k train, 25k test).

Labels:  
  0 → Negative review
  1 → Positive review

Preprocessing:
  Vocabulary limited to top 10,000 words (num_words=10000).
  Sequences padded to fixed length.

Model Architecture
  model = Sequential()
  model.add(Embedding(input_dim=10000, output_dim=128))
  model.add(SimpleRNN(64))
  model.add(Dense(1, activation='sigmoid'))
  
Training
  Optimizer: Adam
  Loss: Binary Crossentropy
  Metrics: Accuracy
