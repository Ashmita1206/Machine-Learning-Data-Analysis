🎤 Speech Recognition & Classification using Whisper
🚀 Overview
This project is an end-to-end Speech Recognition system that:

Converts speech → text using OpenAI Whisper (local model)

Performs keyword classification (Yes/No)

Provides a web interface (Flask) for real-time interaction

✨ Features
🎙️ Audio upload / recording support

🧠 Speech-to-text using Whisper (no API key required)

📊 MFCC-based preprocessing

🤖 Deep Learning model for classification

🌐 Interactive frontend (HTML, CSS, JS)

⚡ Fast local inference

🧠 Tech Stack
Python

Flask

OpenAI Whisper (local)

Librosa (audio processing)

TensorFlow / Keras

JavaScript (frontend)

📂 Project Structure
SPEECH RECOGNITION/
│
├── app.py                # Flask backend
├── requirements.txt     # Dependencies
├── README.md
│
├── model/
│   ├── model.py
│   ├── speech_model.keras
│   └── label_map.json
│
├── utils/
│   ├── audio_processing.py
│   ├── dataset.py
│   └── predict.py
│
├── static/
│   ├── script.js
│   ├── style.css
│   ├── uploads/
│   └── spectrograms/
│
├── templates/
│   └── index.html
│
├── data/                # Training data
├── uploads/             # Runtime uploads
⚙️ Installation
1️⃣ Clone Repo
git clone <your-repo-link>
cd speech-recognition
2️⃣ Create Virtual Environment
python -m venv venv
venv\Scripts\activate   # Windows
3️⃣ Install Dependencies
pip install -r requirements.txt
▶️ Run the App
python app.py
Open in browser:

http://127.0.0.1:5000
🧠 How It Works
🔹 Step 1: Audio Input
User uploads or records audio

🔹 Step 2: Preprocessing
Convert to 16kHz mono WAV

Extract MFCC features

🔹 Step 3: Whisper Transcription
whisper_model = whisper.load_model("base")
result = whisper_model.transcribe(audio_path)
🔹 Step 4: Classification
Process MFCC features

Predict label (Yes / No)

🔹 Step 5: Output
Transcribed text

Predicted label

Confidence score

⚠️ Important Notes
Whisper model loads at runtime:

Loading Whisper model (base)...
👉 This is normal (first run takes time)

Flask debug mode runs app twice → model loads twice

Use debug=False to avoid double loading

📊 Model Details
Input: MFCC features

Architecture: Neural Network (Keras)

Output: Binary classification (Yes / No)

🧪 Sample Commands
Test preprocessing:

python test.py
🚧 Future Improvements
🔊 Real-time microphone streaming

🌍 Multi-language support

📈 More dataset for better accuracy

🚀 Deployment (AWS / Render)

👩‍💻 Author
Ashmita Goyal

💡 Final Note
This project combines:

Speech Recognition (Whisper)

Machine Learning Classification

Full Stack Development (Flask + JS)

