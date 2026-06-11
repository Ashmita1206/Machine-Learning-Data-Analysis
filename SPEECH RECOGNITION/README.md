# 🎙️ Speech Recognition System using Deep Learning

A deep learning based **Speech Recognition Web Application** that classifies spoken audio into predefined categories using an RNN/LSTM based neural network model.

The application allows users to upload or record audio, processes the speech signal, extracts meaningful audio features, and predicts the recognized word using a trained deep learning model.

---

## 🚀 Project Overview

Speech Recognition is a technology that enables computers to understand and interpret human speech.

This project implements a complete end-to-end pipeline:

1. Audio Collection
2. Audio Preprocessing
3. Feature Extraction
4. Deep Learning Model Training
5. Model Deployment
6. Real-time Prediction through Web Interface

The system takes an audio input and predicts the spoken command.

---

## ✨ Features

✅ Upload audio files  
✅ Record audio from browser  
✅ Convert audio into machine-readable features  
✅ Deep learning based speech classification  
✅ Real-time prediction  
✅ Interactive web interface  
✅ Model based inference  
✅ Audio visualization using spectrograms

---

## 🛠️ Technologies Used

### Programming Language

- Python

### Deep Learning

- TensorFlow
- Keras
- RNN / LSTM Neural Network

### Audio Processing

- Librosa
- NumPy
- SoundFile

### Backend

- Flask

### Frontend

- HTML
- CSS
- JavaScript

### Data Handling

- Pandas

---

## 📂 Project Structure

SPEECH RECOGNITION/

│
├── app.py
│ └── Flask application entry point
│
├── model/
│ ├── model.py
│ ├── speech_model.keras
│ └── label_map.json
│
├── utils/
│ ├── audio_processing.py
│ ├── dataset.py
│ └── predict.py
│
├── templates/
│ └── index.html
│
├── static/
│ ├── style.css
│ ├── script.js
│ ├── uploads/
│ └── spectrograms/
│
├── data/
│ ├── yes/
│ └── no/
│
├── requirements.txt
│
├── test.py
│
└── README.md

---

# 🧠 Machine Learning Workflow

## 1. Audio Input

User provides an audio sample:

Example:
yes.wav
no.wav

---

## 2. Audio Preprocessing

The audio is processed before feeding into the model.

Steps:

- Load audio file
- Convert sampling rate
- Normalize audio signal
- Remove unwanted noise
- Prepare fixed length input

---

## 3. Feature Extraction

Raw audio cannot directly be understood by neural networks.

The project converts audio into meaningful features:

### MFCC (Mel Frequency Cepstral Coefficients)

MFCC captures important characteristics of human speech.

Pipeline:
Audio Waveform
|
↓
MFCC Extraction
|
↓
Feature Matrix
|
↓
Neural Network

---

# 🤖 Deep Learning Model

The model uses a Recurrent Neural Network architecture.

## Why RNN/LSTM?

Speech is sequential data.

Example:
Sound1 → Sound2 → Sound3 → Word

RNN remembers previous information while processing the sequence.

---

## Model Architecture

Example:
Input Layer

↓
LSTM Layer

↓
Dense Layer

↓
Softmax Output

↓
Prediction

---

# 📊 Model Output

The model predicts classes:

Example:

Input:
audio.wav

Output:
Prediction: YES
Confidence: 96%

---

# ⚙️ Installation

## 1. Clone Repository

```bash
git clone <repository-url>
2. Move into Project Directory
cd SPEECH RECOGNITION
3. Create Virtual Environment
python -m venv venv
Activate:

Windows:

venv\Scripts\activate
Linux/Mac:

source venv/bin/activate
4. Install Dependencies
pip install -r requirements.txt
▶️ Running the Application
Start Flask server:

python app.py
Open browser:

http://127.0.0.1:5000
🎤 How To Use
Open the application

Upload an audio file OR record audio

Click Predict

Wait for processing

View prediction result

📌 Dataset
The project uses speech samples for training.

Current classes:

yes
no
Dataset structure:

data/

 ├── yes/
 │    ├── yes1.wav
 │    └── yes2.wav

 └── no/
      ├── no1.wav
      └── no2.wav
🔮 Future Improvements
Add more speech commands

Increase dataset size

Improve accuracy

Add noise cancellation

Deploy on cloud

Add multilingual speech recognition

Implement Transformer based models

📈 Performance
The model performance depends on:

Dataset quality

Number of training samples

Audio preprocessing

Model architecture

👩‍💻 Author
Ashmita

Machine Learning / Deep Learning Project

📜 License
This project is created for educational purposes.
```
