# Sentiment Analysis on IMDB Reviews using Simple RNN 🎬🧠

## 📖 Project Overview
This project is an end-to-end deep learning pipeline built with **Keras** and **TensorFlow** to classify IMDB movie reviews as **positive** or **negative**.  
The model leverages a **Simple RNN (Recurrent Neural Network)** architecture to capture sequential dependencies in text data, making it suitable for sentiment analysis tasks.

---

## ⚙️ Dataset
- **Source**: IMDB dataset provided by Keras  
- **Size**: 50,000 movie reviews (25,000 training, 25,000 testing)  
- **Labels**:  
  - `0` → Negative review  
  - `1` → Positive review  
- **Preprocessing**:  
  - Reviews are encoded as sequences of integers (word IDs)  
  - Vocabulary limited to the **top 10,000 most frequent words** (`num_words=10000`)  
  - Sequences padded to a fixed length for uniform input  

---

## 🏗️ Model Architecture
```python
model = Sequential(
)
model.add(Embedding(max_size,128))
model.add(SimpleRNN(128,activation='relu'))
model.add(Dense(1,activation='sigmoid'))
model.build(input_shape=(None, max_len))
model.compile(optimizer='adam',loss='binary_crossentropy',metrics=['accuracy'])
