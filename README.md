# ⚡ AdiFlash Pro

AdiFlash Pro is a highly responsive, high-performance web application designed to instantly generate custom study flashcard decks from user-pasted text, slide presentation documents, or multi-modal audio/video recordings. Leveraging Google's low-latency **Gemini 3.5 Flash Lite** model and structured JSON outputs, the application automatically handles text synthesis, topic classification, and contextual deck-title generation in real-time.

---

## ✨ Features

- 🤖 **Native Multimodal Parsing**: Directly upload lecture recordings or educational clips (`.mp3` / `.mp4`) via the Gemini Files API.
- 📊 **PowerPoint Presentation Support**: Extract structural text content directly out of slide layouts (`.ppt` / `.pptx`).
- 💬 **Chatbot-Style Session Management**: Persistent sidebar tracking allows users to seamlessly save, swap, and delete study history states.
- 🔄 **Fluid Interactive 3D Card Engine**: Clean CSS transform matrices deliver responsive tap-to-flip cards.
- 🎨 **Markdown Rendering Pipeline**: Full support for raw bullet configurations, tabular blocks, and stylized text layouts (`**bolding**`).
- 💾 **Local DB Infrastructure**: Completely self-contained SQLite integration handles high-speed batch data caching.

---

## 📁 System Architecture

```text
flashcard-app/
│
├── app.py                 # Core Flask backend server context
├── database.db            # Local self-contained SQLite cache container
├── uploads/               # Temporary landing pad directory for asset handling
├── requirements.txt       # Project python dependencies configuration
│
└── templates/
    ├── layout.html        # App layout, global stylesheet architecture, and sidebar navigation
    └── index.html         # Main dashboard, canvas interactive matrix modules, and forms
```

---

## 🛠️ Installation & Setup

1. **Clone the Repository** and navigate into your working directory path:
   ```bash
   cd flashcard-app
   ```

2. **Install Core System Dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

3. **Configure Environment Parameters**:
   Create a standard `.env` configuration template file inside the project base path root and add your Google AI Studio access key token:
   ```text
   GEMINI_API_KEY="your_actual_api_studio_secret_key_here"
   ```

4. **Launch the Application Server Engine**:
   ```bash
   python app.py
   ```
   Open your browser layout stream context mapping path pointing directly to `http://127.0.0.1:5000`.

---

## ⚙️ Core Configuration Variables

```python
# System-wide file pipeline mappings located in app.py
app.config["folder"] = "uploads"
app.config["SQLALCHEMY_DATABASE_URI"] = "sqlite:///database.db"
app.config["SQLALCHEMY_TRACK_MODIFICATIONS"] = False
```

---

## 📜 Technology Stack

- **Backend Context Engine**: Flask 3.x, Flask-SQLAlchemy 3.x
- **AI Processing Architecture**: Official Modern `google-genai` SDK
- **Target LLM Mapping Foundation**: `gemini-3.5-flash-lite`
- **Data Serialization Structures**: Strict JSON Schema Format Constraints
- **Document Processing Handlers**: `python-pptx`, `markdown` Core Extensions
- **Local Data Storage Tier**: SQLite
