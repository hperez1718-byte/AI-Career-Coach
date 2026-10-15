# Setup Guide — AI Career Coach

Pick your platform below. You only need **Python** and a **free Gemini API key**.

---

## 🪟 Windows (PC)

### 1. Install Python

1. Go to [python.org/downloads](https://www.python.org/downloads/)
2. Download the latest **Python 3** installer (3.10 or newer)
3. Run it — **check the box "Add python.exe to PATH"** before clicking Install
   (this is the step everyone misses)
4. Verify: open **Command Prompt** and run

```bash
python --version
```

You should see something like `Python 3.14.0`.

### 2. Get the app files

Download this repo (Code → Download ZIP) and unzip it anywhere, e.g.
`Documents\AI Career Coach`.

### 3. Install the app's packages

In Command Prompt, move into the app folder and install:

```bash
cd Documents\AI Career Coach
pip install -r requirements.txt
```

### 4. Run it

```bash
streamlit run app.py
```

A browser tab opens automatically with the app. To stop it later, press
`Ctrl+C` in the Command Prompt window.

### 5. Add your API key

1. Get a free key: [Google AI Studio](https://aistudio.google.com/apikey) →
   **Create API key**
2. In the app's sidebar, paste it into the **🔑 API Key** box and hit **Save**

Done — load a resume and go.

---

## 🍎 Mac

### 1. Install Python

Macs ship with an old system Python — install a current one:

- **Easiest:** [python.org/downloads](https://www.python.org/downloads/) →
  download the macOS installer → run it
- **Or with Homebrew:** `brew install python`

Verify in **Terminal**:

```bash
python3 --version
```

### 2. Get the app files

Download this repo (Code → Download ZIP) and unzip it anywhere, e.g.
`~/Desktop/AI Career Coach`.

### 3. Install the app's packages

In Terminal, move into the app folder and install:

```bash
cd ~/Desktop/"AI Career Coach"
pip3 install -r requirements.txt
```

> If `pip3` isn't found, try `python3 -m pip install -r requirements.txt`.

### 4. Run it

```bash
streamlit run app.py
```

(If that fails: `python3 -m streamlit run app.py`.)

A browser tab opens automatically with the app. To stop it later, press
`Ctrl+C` in the Terminal window.

### 5. Add your API key

1. Get a free key: [Google AI Studio](https://aistudio.google.com/apikey) →
   **Create API key**
2. In the app's sidebar, paste it into the **🔑 API Key** box and hit **Save**

Done — load a resume and go.

---

## 🔑 About the API key

- The key is **free** and takes 2 minutes to create.
- You can also put it in a `.env` file (copy `.env.example` → `.env`) —
  but the sidebar box is easier and always takes priority. The app reads `.env`
  only from this project folder.
- The app defaults to **Classroom / fast — Gemini 3.5 Flash-Lite**. You can
  select Gemini 3.8 Flash in the sidebar when you prefer higher-quality output.
- Gemini quotas depend on the Google project and can change. If the app shows a
  quota message, open the provided [AI Studio rate-limit page](https://aistudio.google.com/rate-limit).
  A different key from the same Google project will not increase its capacity.
- **Never share your key or commit it to git.** `.gitignore` already blocks `.env`.

## ❓ Troubleshooting

| Problem | Fix |
|---------|-----|
| `streamlit: command not found` | Close and reopen the terminal, then reinstall: `pip install -r requirements.txt` |
| `pip: command not found` (Mac) | Use `pip3` or `python3 -m pip` instead |
| Browser doesn't open | Copy the `http://localhost:8501` URL from the terminal into your browser |
| "No API key yet" | Paste your key in the sidebar and hit **Save** |
| Gemini quota message | Open the linked AI Studio rate-limit page. Wait for the project quota to reset or use a project with available quota. |
| App looks broken after an update | Stop it (`Ctrl+C` in the terminal) and run `streamlit run app.py` again |
