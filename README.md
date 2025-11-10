# Gemini Logger

Gemini Logger is a simple CLI chat application using the **Google Gemini API**.  
It takes user input, generates AI responses, and stores the conversation logs in a **hidden folder**, which can be copied to a desired location upon exit.

## ⚡ Features
- Interactive CLI interface  
- AI-generated responses using Gemini API  
- Log management:
  - Hidden folder: `~/.gemini-logger/dialogues.txt`
  - Visible folder upon exit: `~/GeminiLogs/dialogues.txt`
- Suppresses warning messages (no warning logs displayed)  
- Safe API key management via environment variables  

## 💻 Installation & Usage

### 1. Verify Python 3 installation
```bash
python3 --version
````

### 2. Install required libraries

```bash
pip install google-generativeai
# Optional: install absl to manage warning logs
pip install absl-py
```

### 3. Set the environment variable

```bash
export GEMINI_API_KEY="YOUR_API_KEY_HERE"
```

### 4. Run the script

```bash
./gemini-logger
```

* Type `exit` or `quit` to end the session.
* Upon exit, logs will be copied to `~/GeminiLogs/dialogues.txt`.

## 📂 Log Locations

| Type         | Path                             |
| ------------ | -------------------------------- |
| Hidden logs  | `~/.gemini-logger/dialogues.txt` |
| Visible logs | `~/GeminiLogs/dialogues.txt`     |

## ⚙️ Example Usage

```text
=== Gemini Logger ===
Type your message and press Enter. Type 'exit' to quit.

You: Hi, Gemini!
AI: Hello! How can I assist you today?

You: How’s the weather today?
AI: It looks sunny and clear today.
```

## 📝 Notes

* Make sure the `GEMINI_API_KEY` environment variable is set.
* Logs contain your personal conversation data; be cautious when sharing.
* On Mac, place the executable in a path like `/Users/hyunsu/bin` for easy CLI access.
