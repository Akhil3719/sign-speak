# sign-speak
SignSpeak is a real-time, browser-based accessibility tool that translates custom sign language into spoken words and converts speech into live text. Built entirely with on-device computer vision and k-NN machine learning—no LLMs, APIs, or expensive hardware required. It works both in-person and remotely via built-in WebRTC video calls.

# 🤟 SignSpeak

**Simple AI. Real People. Real Impact.**  
SignSpeak is a real-time accessibility tool that lets you train custom signs through your webcam, recognizes them instantly, and speaks them out loud. It bridges the communication gap between the Deaf/Hard-of-Hearing community and hearing individuals without requiring anyone to learn a new language, buy expensive hardware, or install native apps.

🌐 **Live Demo:** [Insert Your Deployed Link Here]

## 💡 The Problem
* **430M+ people** worldwide live with disabling hearing loss (WHO).
* **Most hearing people** never learn sign language, making spontaneous daily interactions difficult.
* **Human interpreters** cannot scale to every everyday moment (e.g., shops, hospitals, government counters).
* **Remote communication barriers:** Traditional remote video/phone calls lack integrated, real-time sign-to-speech translation without third-party services.

## 🚀 How SignSpeak Solves It
No special gloves. No depth sensors. Just a device with a camera and a web browser.

1. **Teach it a sign:** Pick a word, hold the sign in front of your camera, and capture a few samples. Takes seconds.
2. **It recognizes & speaks:** Sign it again. The app matches the sign against your training data and uses text-to-speech to say the word out loud.
3. **Take it to a call:** Share a link to start a two-way WebRTC video call. Signs become speech for the hearing person, and their speech becomes live text captions for the signing person.

## ✨ Core Features
* **Teachable Machine Learning:** Train custom static and moving signs live in the browser.
* **In-Person Mode:** Real-time sign-to-speech translation for face-to-face interactions.
* **Speech → Text:** Built-in dictation that converts what a hearing person says into large, readable text.
* **SignSpeak Connect (Video Calls):** Full two-way peer-to-peer video calling with integrated sign-to-speech and speech-to-text.
* **Pre-trained Gestures:** Immediately recognizes 7 universal hand gestures out-of-the-box using Google's pretrained models.
* **Privacy-First & Local:** Your trained signs are saved entirely in your browser's `localStorage`. Import and Export functionalities are available to back up or move your trained data.

## 🛠️ Tech Stack & AI Models
**Zero LLMs. Zero external API fees. Runs entirely in the browser.**

* **[MediaPipe Hand Landmarker](https://developers.google.com/mediapipe/solutions/vision/hand_landmarker) (Google):** Pretrained deep learning (CNN) computer vision model that detects 21 precise key points on each hand in real-time.
* **k-Nearest Neighbors (k-NN):** Our custom, lightweight machine learning classifier. It takes the spatial landmark points from MediaPipe and matches them to your trained data using mathematical similarity. Fast enough to run without a GPU.
* **Web Speech API (Speech Synthesis):** Built-in browser TTS to speak recognized words aloud instantly.
* **Web Speech API (Speech Recognition):** Built-in browser STT to convert the hearing user's speech into live captions.
* **[PeerJS](https://peerjs.com/) (WebRTC):** Handles the P2P connection for the low-latency two-way video calls.

## ⚙️ Running Locally

Because SignSpeak relies on browser-native APIs and client-side ML, you don't need a heavy backend to run it. 

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/yourusername/signspeak.git](https://github.com/yourusername/signspeak.git)
   cd signspeak
