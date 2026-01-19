# 🩺 AI Doctor Voice Bot (Vision + Speech)

An **AI-powered Doctor Assistant** that can:
- 🎙️ Listen to patient voice (Speech-to-Text)
- 🖼️ Analyze medical images (Vision LLM)
- 🧠 Generate doctor-like responses
- 🔊 Speak back with realistic voice (Text-to-Speech)
- 🌐 Run in a clean **Gradio Web UI**

> ⚠️ **Disclaimer**: This project is for **learning and research purposes only**.  
> It is **not a replacement for professional medical advice**.

---

## 🚀 Features

- **Speech-to-Text (STT)** using Groq Whisper (`whisper-large-v3`)
- **Vision-based medical reasoning** using LLaMA 4 Vision models via Groq
- **Text-to-Speech (TTS)** using ElevenLabs (realistic voices)
- **Cross-platform audio playback** (Windows / macOS / Linux)
- **Interactive Gradio UI**
- Modular and clean codebase

---

## 🧱 Project Structure

```bash
AI-Doctor-Voice-Bot/
│
├── app.py # Main Gradio application
├── brain_of_the_doctor.py # Vision LLM logic
├── voice_of_the_patient.py # Audio recording & STT
├── voice_of_the_doctor.py # TTS + audio playback
├── requirements.txt
├── .env # API keys (not committed)
└── README.md
```

---

## 🔐 Environment Variables

Create a `.env` file in the root directory:

```env
GROQ_API_KEY=your_groq_api_key
ELEVEN_API_KEY=your_elevenlabs_api_key
```

---

## 📦 Installation

1️⃣ Clone the Repository
```bash
git clone https://github.com/Chintan1545/AI-Doctor-Voice-Bot.git
cd AI-Doctor-Voice-Bot
```
2️⃣ Create Virtual Environment (Recommended)
```bash
python -m venv venv
venv\Scripts\activate     # Windows
source venv/bin/activate  # macOS/Linu
```
3️⃣ Install Python Dependencies
```bash
pip install -r requirements.txt
```

---

## ⚙️ System Dependencies (IMPORTANT)

🔹 FFmpeg (Required for audio playback)
Check:
```bash
ffmpeg -version
```
Install:

- Windows: https://ffmpeg.org/download.html (add to PATH)
- macOS:
```bash
brew install ffmpeg
```
- Linux:
```bash
sudo apt install ffmpeg
```

---

🔹 PyAudio (Microphone Support)
Windows (Recommended)
```bash
pip install pipwin
pipwin install pyaudio
```
macOS
```bash
brew install portaudio
pip install pyaudio
```
Linux
```bash
sudo apt install portaudio19-dev
pip install pyaudio
```

---

## ▶️ Run the Application
```bash
python app.py
```
Open in browser:
```bash
http://127.0.0.1:7860
```

---

## 🧠 How It Works

1. 🎤 User speaks → Whisper STT converts speech to text
2. 🖼️ User uploads image → Vision LLM analyzes medical context
3. 🧠 AI generates a doctor-style response
4. 🔊 ElevenLabs converts text → natural speech
5. 🌐 Gradio displays text + plays audio

---

##🛠️ Models Used 

| Task           | Model                                       |
|----------------|---------------------------------------------|
| Speech-to-Text | `whisper-large-v3`                           |
| Vision LLM     | `meta-llama/llama-4-scout-17b-16e-instruct`  |
| Text-to-Speech | `eleven_turbo_v2`                            |


---

## 📌 requirements.txt 
```bash
gradio
groq
SpeechRecognition
pyaudio
pydub
gTTS
elevenlabs
python-dotenv
```

---

## ⚠️ Known Limitations

- Requires stable internet connection
- ElevenLabs requires paid API for heavy usage
- Not a certified medical system
- Audio playback depends on FFmpeg availability

---

## 🧪 Future Improvements

- ✅ Streaming voice responses
- 🧠 Patient history memory
- 📱 Mobile-friendly UI
- 🐳 Docker support
- ☁️ Cloud deployment (EC2 / HuggingFace)

---

## 🤝 Contributing

1. Contributions are welcome!
2  Fork the repo
3. Create a feature branch
4. Commit changes
5. Open a Pull Request

---

## 📜 License

MIT License © 2026
Free to use for learning and research.

---

## ⭐ Support

If you find this project helpful:
- ⭐ Star the repository
- 🧑‍💻 Share with the community
