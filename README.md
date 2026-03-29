# ScanLocal — Browser-Native OCR

🔍 **Extract text from images entirely in your browser** — no upload, no API keys, no privacy concerns.

🎙️ **Try it now** → https://naklitechie.github.io/ScanLocal/

---

## Features

- **Four OCR engines** in one tool:
  - 📜 **Default (Tesseract)** — Most reliable browser path, broad language support
  - 🚀 **Fast (PaddleOCR)** — Printed text path via Paddle models
  - ✍️ **Handwriting (TrOCR)** — SOTA for handwritten text, ~500 MB
  - 🧠 **Smart OCR** — Transformer fallback for printed text, no boxes

- **100% client-side** — Your images never leave your device
- **No dependencies** — Single HTML file, no npm, no bundler
- **Offline-ready** — Models cached after first load
- **Privacy-first** — No tracking, no analytics, no data collection

---

## Use Cases

- Receipts and invoices
- Scanned documents
- Business cards
- Screenshots with text
- Handwritten notes
- Historical documents

---

## How to Use

1. **Open** the app in your browser
2. **Choose an engine**:
   - **Default** for the safest first try in-browser
   - **Fast** for receipts, documents, screenshots
   - **Handwriting** for handwritten notes
   - **Smart** for an alternate transformer-based read on printed text
3. **Drop an image** or click to upload
4. **Wait** for text extraction
5. **Copy** the extracted text

---

## Running Locally

### Option 1: Direct file open
```bash
# Just open index.html in your browser
open ScanLocal/index.html
```

### Option 2: Local server (recommended)
```bash
cd ScanLocal
python3 -m http.server 8000
# Open http://localhost:8000
```

### Option 3: GitHub Pages
The app is automatically deployed to:  
https://naklitechie.github.io/ScanLocal/

---

## Tech Stack

| Component | Technology |
|---|---|
| **Framework** | Vanilla JS (zero dependencies) |
| **OCR Engine 1** | PaddleOCR (PP-OCRv5) via Paddle.js |
| **OCR Engine 2** | TrOCR via Transformers.js |
| **OCR Engine 3** | Tesseract.js v5 |
| **OCR Engine 4** | Printed-text transformer OCR via Transformers.js |
| **UI** | Custom CSS (NakliTechie design system) |
| **Hosting** | GitHub Pages |

---

## Model Sizes & Performance

| Engine | Size | First Load | Cached | Best For |
|---|---|---|---|---|
| Tesseract | ~25 MB/lang | 5-10 sec | Instant | Default browser OCR, broad language support |
| PaddleOCR | ~20 MB | 2-5 sec | Instant | Printed text |
| TrOCR | ~500 MB | 30-60 sec | Instant | Handwriting |
| Smart OCR | ~300-500 MB | 20-60 sec | Instant | Alternate printed-text extraction |

---

## Supported Formats

- **Images:** PNG, JPG/JPEG, WebP
- **Max size:** 10 MB per image
- **Languages:** 100+ (varies by engine)

---

## Privacy

**ScanLocal** is part of the **NakliTechie** series — browser-native tools that keep your data on your device.

- ❌ No server uploads
- ❌ No API keys
- ❌ No tracking
- ❌ No analytics
- ✅ All processing happens in your browser
- ✅ Models cached locally after first load

---

## License

MIT License — see [LICENSE](LICENSE) file.

---

## Part of NakliTechie Series

ScanLocal follows the same blueprint as:

- [BabelLocal](https://github.com/NakliTechie/BabelLocal) — Browser translator (200 languages)
- [StripLocal](https://github.com/NakliTechie/StripLocal) — EXIF metadata stripper
- [GambitLocal](https://github.com/NakliTechie/GambitLocal) — Chess vs Stockfish
- [VoiceVault](https://github.com/NakliTechie/VoiceVault) — Audio transcription
- [KingMe](https://github.com/NakliTechie/KingMe) — Checkers vs AI
- [SnipLocal](https://github.com/NakliTechie/SnipLocal) — Background remover

All single-file, zero-dependency, browser-native apps.

---

## Development

### Project Structure

```
ScanLocal/
├── index.html          # The entire app (shipped)
├── README.md           # This file (shipped)
├── LICENSE             # MIT license (shipped)
├── .gitignore          # Git ignore rules
└── PLAN.md             # Planning notes (not shipped)
```

### Build Commands

None! Just edit `index.html` and refresh your browser.

### Deploy to GitHub Pages

```bash
# Enable GitHub Pages on the repository
# Settings → Pages → Source: main branch → /root
# Push to main branch
git push origin main
```

---

## Contributing

Issues and PRs welcome! Please read [IDEAS.md](../IDEAS.md) for the series guidelines before contributing.

---

## Author

**Chirag Patnaik**  
[NakliTechie](https://github.com/NakliTechie)

---

## TODOs (Roadmap)

See [PLAN.md](PLAN.md) for detailed implementation plan.

**Phase 1 (Current):** Core infrastructure ✅
- [x] Base HTML skeleton
- [x] Engine selector UI (4 engines)
- [x] Dropzone + preview
- [x] PaddleOCR integration
- [x] TrOCR integration
- [x] Tesseract.js integration
- [x] Smart OCR integration

**Phase 2:** Engine integration
**Phase 3:** UI polish
**Phase 4:** Testing
**Phase 5:** Launch
