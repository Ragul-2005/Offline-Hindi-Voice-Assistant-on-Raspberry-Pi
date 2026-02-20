
<div align="center">

# 🎙️ Offline Hindi Voice Assistant on Raspberry Pi
### Privacy-Preserving Embedded Speech AI System


**A fully offline, low-latency Hindi voice assistant designed for ARM-based edge devices**

[📌 Overview](#-overview) • [🧠 Architecture](#-system-architecture) • [⚡ Performance](#-performance) • [🚀 Quick Start](#-quick-start)

</div>

---

## 📌 Overview

<p align="justify">
This project presents a <b>fully offline Hindi Voice Assistant</b> designed to run entirely on a Raspberry Pi without any cloud dependency. The system performs on-device speech recognition, intent processing, and text-to-speech synthesis, ensuring <b>user privacy, low latency, and edge-AI compatibility</b>.
</p>

<p align="justify">
The solution addresses challenges in regional language voice interfaces by supporting Hindi speech input and output, optimized for CPU-only ARM environments. The assistant is suitable for deployment in smart homes, assistive technologies, public kiosks, and rural or low-connectivity regions.
</p>

---

## 🧠 System Architecture

```text
🎤 Microphone (USB / Wired / Bluetooth)
        ↓
🎛️ Audio Capture (ALSA / PyAudio)
        ↓
🧠 Hindi Speech Recognition (Whisper ASR – Tiny / Base)
        ↓
🧹 Text Normalization
   • Noise Filtering
   • Language Cleanup
   • Token Correction
        ↓
🎯 Intent Recognition
   • Rule-based
   • LLM-assisted
        ↓
🤖 Response Generation
   • Local Logic
   • LLM (Gemma / Qwen / API)
        ↓
🔊 Hindi Text-to-Speech (Piper TTS – hi_IN)
        ↓
🎧 Speaker Output (Laptop / Bluetooth / Headphones)
```
---


---

## 🛠️ Hardware Requirements

| Component | Specification |
|---------|---------------|
| SBC | Raspberry Pi 4 / 5 (8GB recommended) |
| Microphone | USB Microphone (Tested: Shure MV7+) |
| Speaker | 3.5mm / HDMI / Bluetooth |
| Compute | CPU-only (No GPU / accelerator) |

---

## 💻 Software Stack

- 🐍 **Python 3.10 / 3.11**
- 🗣️ **Whisper ASR** (Tiny / Base)
- 🔊 **Piper TTS** (Hindi – pratham medium)
- 🎧 **ALSA / PyAudio**
- 📐 **NumPy**
- 🤖 **Optional LLM Integration** (Offline / Online)

---

## 🧠 Speech Recognition (ASR)

| Feature | Detail |
|------|------|
| Model | Whisper Base |
| Language | Hindi |
| Input | 48 kHz USB microphone |
| Processing | Resampled to 16 kHz |
| Execution | CPU-only |

---

## 🔊 Text-to-Speech (TTS)

| Feature | Detail |
|------|------|
| Engine | Piper TTS |
| Voice | hi_IN-pratham-medium |
| Output | WAV audio |
| Quality | Natural Hindi pronunciation |

---

## ⚡ Performance

| Component | Latency (Raspberry Pi 4) |
|--------|--------------------------|
| Whisper Tiny | ~2 seconds |
| Whisper Base | ~4 seconds |
| Piper TTS | ~1–2 seconds |
| End-to-End | ~5–8 seconds |

---

## 🚀 Quick Start

### 📋 Prerequisites

```bash
sudo apt update
sudo apt install -y python3 python3-venv portaudio19-dev ffmpeg
```
---

### 📦 Setup

```bash
git clone https://github.com/<your-username>/offline-hindi-voice-assistant.git
cd offline-hindi-voice-assistant

python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```
---
