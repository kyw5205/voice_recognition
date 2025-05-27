# Whisper Voice Recognition Web Application

This project is a simple voice-to-text web application powered by [Whisper](https://github.com/openai/whisper), an automatic speech recognition (ASR) model developed by OpenAI. The application consists of a **FastAPI-based backend** and a **React (vanilla JSX + Material UI) frontend**. Users can record their voice directly from the browser and get real-time transcription results powered by Whisper.

---

## 🔧 Features

- 🎤 Record voice using browser microphone
- 🔁 Send recorded audio to FastAPI server
- 🧠 Transcribe speech to text using Whisper
- 📄 Display transcription on screen

---

## 🗂️ Project Structure

```
.
├── app.py                  # FastAPI backend server
├── run_server.py           # Colab integration to run server and expose via ngrok
├── www/
│   └── index.html          # Frontend HTML + React code
```

---

## 🚀 How to Run (in Google Colab)

1. Install dependencies:
   ```python
   !pip install fastapi uvicorn python-multipart pyngrok openai-whisper
   ```

2. Set your ngrok token (you must sign up at [ngrok.com](https://dashboard.ngrok.com)):
   ```python
   !ngrok config add-authtoken YOUR_NGROK_TOKEN
   ```

3. Write `app.py`:
   ```python
   %%writefile app.py
   # your FastAPI + Whisper code here
   ```

4. Write `www/index.html`:
   ```python
   %%writefile www/index.html
   <!-- your frontend code here -->
   ```

5. Launch the server:
   ```python
   !python run_server.py
   ```

6. Click the generated `ngrok` URL and test it!

---

## ⚙️ Tech Stack

- **Backend**: FastAPI, Whisper, Uvicorn
- **Frontend**: React (via CDN), Material UI, HTML/CSS
- **Others**: pyngrok for exposing Colab ports

---

## 📌 Notes

- The audio is recorded in `.webm` format using the `MediaRecorder` API.
- Whisper model used is `"base"` for a balance of speed and accuracy.
- The app is ideal for prototyping, not optimized for production.

---
![음성인식1](https://github.com/user-attachments/assets/9acf4587-fa4c-4711-bdd4-3be3fdb3461a)

## 📜 License

This project is for academic/demo purposes and follows the MIT License. Whisper model is © OpenAI.
