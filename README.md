# 🃏 Trading Card Translator (AI-Powered Proxy Generator)

[![Python 3.10+](https://img.shields.io/badge/python-3.10+-blue.svg)](https://www.python.org/)
[![Google Gemini API](https://img.shields.io/badge/API-Google%20Gemini-orange.svg)](https://ai.google.dev/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

An automated translation and typesetting pipeline built with **Google Gemini Vision LLMs** and **Python (PIL)**. This tool takes social media card reveal graphics (containing original card photos and Japanese/English translations in the description text) and automatically crops, masks, and overlays styled English text directly onto card proxies for play-testing.

---

## 💡 Key Technical Features

- **Zero-OCR Multimodal Architecture:** Direct extraction of structured card data and layout bounding boxes using vision LLMs rather than traditional OCR pipelines.
- **Cost-Optimized Model Tiering:**
  - `gemini-3.5-flash-lite`: Used for structured text extraction from post descriptions to minimize API cost on deterministic parsing tasks.
  - `gemini-3.6-flash`: Used for spatial segmentation to predict precise normalized bounding box coordinates (`name`, `type`, `effects`).
- **Dynamic Masking & Typesetting:** Auto-samples background colors to mask original foreign text, calculates contrast ratios, and wraps/scales translated text inside target visual bounding boxes using Pillow (PIL).

---

## 🔮 Future Roadmap

- [ ] **Icon Embedding:** Automatically detect and re-insert gameplay symbols/icons into translated text frames.
- [ ] **TCG-Agnostic Engine:** Generalize spatial detection to support any Trading Card Game out-of-the-box.
- [ ] **Language Translation Agnosticity:** Support dynamic translation between any arbitrary source and target language pairs.

---

## ⚙️ Quickstart & Usage

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/mike-1-1-1/Trading-Card-translator.git](https://github.com/mike-1-1-1/Trading-Card-translator.git)
   cd Trading-Card-translator
