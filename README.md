# 🎥 AI Video Dubber & Translator

An interactive web app interface and architecture design for translating and dubbing YouTube videos into target languages (English, Hindi, Nepali, Spanish, Arabic, French, German) using AI workflows.

![License](https://img.shields.io/badge/license-MIT-blue)
![Tech Stack](https://img.shields.io/badge/tech-HTML5%20%7C%20TailwindCSS%20%7C%20JavaScript-violet)

---

## 🌟 Features
- **Interactive UI Dashboard:** Sleek, modern dark-mode aesthetic built for mobile and desktop screens.
- **Pipeline Progress Tracker:** Live visual simulation of backend status across 4 primary stages.
- **Multi-Language Support:** Preset configurations for English, Hindi, Nepali, Spanish, Arabic, French, and German.
- **API Key Manager:** Test drawer for configuring OpenAI and ElevenLabs keys directly in the browser preview.
- **Developer Code Viewers:** Built-in modal tabs with backend code for Next.js App Router and Python FastAPI execution scripts.

---

## 🚀 Live Demo
Try the live interactive webpage here:
👉 **[Launch AI Video Dubber Live Demo](https://YOUR_GITHUB_USERNAME.github.io/ai-video-dubber/)**

*(Replace `YOUR_GITHUB_USERNAME` above with your actual GitHub username)*

---

## 🏗️ How the Pipeline Works

1. **Media Extraction (`yt-dlp`):** Downloads raw video and audio streams from the provided YouTube URL.
2. **Speech-to-Text (OpenAI Whisper):** Transcribes audio into timestamped text segments.
3. **Translation (GPT-4o / DeepL):** Translates the transcribed text into the user's chosen target language.
4. **Voice Synthesis (ElevenLabs / Coqui XTTS):** Generates natural-sounding voiceovers synced to original video timing.
5. **Merging (`ffmpeg`):** Replaces the original audio track with the new multilingual voice track and outputs an MP4 file.

---

## ⚙️ Backend Setup & Environment Variables

To run the actual processing server locally:

### 1. System Requirements
Install `ffmpeg` and `yt-dlp` on your system:
```bash
# macOS
brew install ffmpeg yt-dlp

# Ubuntu / Debian
sudo apt update && sudo apt install ffmpeg yt-dlp
