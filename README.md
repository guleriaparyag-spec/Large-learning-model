# LLM Expert Assistant — Streamlit

A Streamlit version of your original Gemini-powered LLM Expert Assistant. It preserves your supplied LLM knowledge base and system prompt, and adds a browser chat interface with conversation history.

## 1. Install Python packages

```bash
python -m venv .venv
```

Activate the environment:

**Windows**
```bash
.venv\\Scripts\\activate
```

**macOS / Linux**
```bash
source .venv/bin/activate
```

Install dependencies:

```bash
pip install -r requirements.txt
```

## 2. Configure your Gemini API key

1. Open the `.streamlit` folder.
2. Rename `secrets.toml.example` to `secrets.toml`.
3. Open `secrets.toml` and replace `YOUR_GEMINI_API_KEY` with your Google AI Studio API key.

Example:

```toml
GEMINI_API_KEY = "paste_your_real_key_here"
GEMINI_MODEL = "gemini-3.5-flash-lite"
```

The real `secrets.toml` is ignored by Git so your key is not accidentally committed. Do not share it or upload it to GitHub.

If the model ID is unavailable for your account, change `GEMINI_MODEL` to a currently supported Gemini model ID.

## 3. Run the app

From the project folder:

```bash
streamlit run app.py
```

Streamlit will open the chatbot in your browser.

## Notes

- Your original knowledge base and system prompt are embedded in `app.py`.
- The app uses the official `google-genai` Python SDK.
- API keys are read from Streamlit's TOML secrets file; no key is hard-coded in the Python source.
- The model name is configurable in `.streamlit/secrets.toml` and in the sidebar.
