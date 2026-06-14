🎤 Speech Recognition System (Yes/No Classifier + Whisper)
📌 Overview
This project is an end-to-end Speech Recognition System that can:

🎙️ Take voice input from user

🔊 Convert audio into text using Whisper

🤖 Classify speech into "Yes" or "No" using a trained ML model

📊 Generate spectrograms for visualization

🚀 Features
🎤 Real-time audio recording (browser)

🔄 Audio format conversion (WebM → WAV)

🧠 Speech-to-text using Whisper

🤖 Custom trained classification model (Yes/No)

📊 Spectrogram generation

🌐 Flask-based web app

🏗️ Project Structure
SPEECH-RECOGNITION/
│
├── app.py                      # Main Flask app
├── requirements.txt           # Dependencies
├── test.py                    # Model testing
│
├── data/
│   ├── yes/
│   └── no/
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
│   ├── uploads/
│   ├── spectrograms/
│   ├── script.js
│   └── style.css
│
├── templates/
│   └── index.html
⚙️ Tech Stack
Python

Flask

TensorFlow / Keras

Librosa

Whisper (OpenAI)

JavaScript (Frontend)

HTML/CSS

🧠 How It Works
🔹 Step 1: Audio Input
User records audio from browser

File saved as .webm

🔹 Step 2: Conversion
Audio converted to .wav using FFmpeg

🔹 Step 3: Feature Extraction
MFCC features extracted using Librosa

🔹 Step 4: Prediction
Model predicts: Yes / No

🔹 Step 5: Whisper
Converts speech → text

🔹 Step 6: Output
Shows:

Prediction

Transcribed text

Spectrogram

🧪 Model Details
Input: Audio (WAV)

Features: MFCC

Model: Neural Network (Keras)

Output: Binary classification (Yes / No)

💻 Installation & Setup
1️⃣ Clone repo
git clone <your-repo-link>
cd SPEECH-RECOGNITION
2️⃣ Create virtual environment
python -m venv .venv
3️⃣ Activate environment
# Windows
.venv\Scripts\activate
4️⃣ Install dependencies
pip install -r requirements.txt
▶️ Run the App
python app.py
👉 Open browser:

http://127.0.0.1:5000
⚠️ Common Issues
❌ Whisper loading every time
Due to Flask debug mode restart

Fix:

app.run(debug=False)
❌ FFmpeg error
Ensure FFmpeg is installed or auto-detected

❌ Audio not working
Check proper WAV conversion

Avoid renaming files manually

📊 Output Example
✔ Prediction: YES / NO

✔ Transcribed text

✔ Spectrogram image

🔥 Future Improvements
Multi-word recognition

More dataset training

Better UI

Deployment (Render / AWS)

🙌 Author
Ashmita Goyal

⭐ If you like this project
Give it a ⭐ on GitHub!
