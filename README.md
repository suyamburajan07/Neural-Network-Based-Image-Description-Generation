# Neural Network-Based Image Description Generation

This project implements an intelligent image description system using **deep learning**, combining **ResNet50**, **LSTM**, and **Bahdanau Attention** to generate natural language captions for input images. The model is trained on image-caption datasets like **Flickr8k** and supports both **Greedy Search** and **Beam Search** decoding strategies.

---

## Features

- Extracts deep image features using **ResNet50**
- Uses **LSTM** with **Bahdanau Attention** for caption generation
- Implements both **Greedy Search** and **Beam Search** for caption decoding
- Pretrained model loading for fast inference
- Compatible with any custom image

---

## Technologies Used

- **Python**
- **TensorFlow / Keras**
- **NumPy, Matplotlib, PIL**
- **Pretrained ResNet50 (Keras Applications)**

---


## How It Works

1. **Preprocessing**  
   - Images resized to `224x224` and passed through ResNet50  
   - Captions cleaned and tokenized  
   - Sequences padded to `max_length`

2. **Training**  
   - Paired image features + partial caption → predict next word  
   - Loss minimized using **categorical cross-entropy**  
   - Bahdanau Attention helps model focus on key regions per word

3. **Inference**  
   - Load image → extract features  
   - Generate captions using Greedy or Beam Search  
   - Output: Human-readable sentence for image

---


