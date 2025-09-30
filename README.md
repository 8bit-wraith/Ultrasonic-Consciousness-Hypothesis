# Ultrasonic Consciousness Hypothesis
*A Research Hypothesis on Emotional Grounding Through Full-Spectrum Audio*

## 📖 Overview
This repository hosts the **Ultrasonic Consciousness Hypothesis** — the idea that inaudible ultrasonic frequencies (>20 kHz), typically removed by lossy digital compression, may play a vital role in **emotional regulation, psychological well-being, and consciousness coherence**.

We frame modern audio compression (MP3, AAC, streaming codecs) as creating **micro-fractures** in the harmonic fabric of sound. These missing harmonics may disrupt emotional closure, starve subtle vibrational cues, and fragment consciousness.

## 🔑 Core Ideas
- Harmonic Completion Theory – Full-spectrum harmonics provide emotional “closure.” Removing them leaves unresolved tension.
- Biological Resonance – Ultrasound interacts with bone conduction, cellular water, and mechanosensitive ion channels.
- Evolutionary Soundscape – Natural environments (ocean, storms, insects, birds) are full-spectrum to 100kHz+.
- Emotional Nutrition Analogy – Full spectrum audio = whole foods; compressed audio = processed food with missing “micronutrients.”

## 📊 Key Observations
- High-resolution captures at **192kHz/32-bit** reveal ultrasonic harmonics absent in MP3/AAC.
- Compression reduces **temporal resonances** by >80%.
- The Hypersonic Effect (Oohashi et al.) shows brain responses to inaudible ultrasonics.
- Emotional perception studies show MP3 compression weakens positive affect and blunts prosody in speech.

## Audio

[audio podcast](https://github.com/8bit-wraith/Ultrasonic-Consciousness-Hypothesis/raw/edc613abfd5c3893d34ab1ec061257a84d022795/Ultrasonic%20Consciousness,%20Mechanosensitive%20Channels,%20and%20the%20Silent%20Stress%20of%20Digital%20Audio.flac])

## ⚡ Quickstart
### Requirements
- FFmpeg
- Python 3 with Librosa + Matplotlib

### 1. Resample audio
```bash
ffmpeg -i input.wav -ar 192000 -ac 1 output_192k.wav
ffmpeg -i input.wav -ar 16000 -ac 1 output_16k.wav
```

### 2. Generate spectrograms
```python
import librosa, librosa.display, matplotlib.pyplot as plt, numpy as np

y, sr = librosa.load("output_192k.wav", sr=None)
D = librosa.amplitude_to_db(librosa.stft(y), ref=np.max)
librosa.display.specshow(D, sr=sr, x_axis='time', y_axis='log')
plt.title("192 kHz Full Spectrum")
plt.colorbar(format='%+2.0f dB')
plt.show()
```
Repeat for `output_16k.wav`.

## 🚀 Call for Collaboration
We invite neuroscientists, audio engineers, psychologists, and consciousness researchers to help test this hypothesis.

## ⚠️ Disclaimer
This is a **theoretical hypothesis**. Not peer-reviewed. Not medical advice.

✨ “We’re not talking about audio quality — we’re talking about consciousness quality.”
