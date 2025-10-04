# 🚀 CodeGate

**CodeGate** is a powerful, interactive command-line Python security auditor powered by Google's Gemini Large Language Model (LLM). Designed for developers, security engineers, and code reviewers, CodeGate helps you identify vulnerabilities, security risks, and bad coding practices in your Python projects with speed and clarity.

---

## 🌟 Features

- **Gemini LLM-Powered Analysis**: Leverages Google's Gemini model for deep code understanding.
- **Static & AI Security Scanning**: Detects vulnerabilities using both static analysis and generative AI.
- **Interactive REPL**: User-friendly command-line interface for hands-on auditing.
- **Paste Mode**: Analyze code snippets instantly—perfect for quick checks.
- **Rich Output**: Uses [Rich](https://github.com/Textualize/rich) for beautiful, colored terminal output.
- **History Tracking**: Maintains a log of your scans for easy reference.
- **Caching & Configurable Settings**: Speed up repeated scans and tailor the tool to your workflow.

---

## 🛡️ What Does CodeGate Detect?

- **Command Injection**: Unsafe use of `os.system`, `subprocess`, `eval`, `exec`, etc.
- **Path Traversal**: Dangerous file operations with user input.
- **SQL Injection**: Vulnerabilities from raw SQL string construction.
- **Deserialization Issues**: Unsafe use of `pickle.loads`, `yaml.load`, etc.
- **Cryptographic Flaws**: Weak algorithms, hardcoded secrets.
- **Information Disclosure**: Sensitive data leaks in logs or errors.
- **Resource Exhaustion**: Infinite loops, unbounded allocations.
- **Network Security**: Insecure connections, unvalidated URLs.
- **Input Validation Problems**: Buffer overflows, missing sanitization.

---

## 🏗️ Installation

```bash
git clone https://github.com/001Priyans/codeGate.git
cd codeGate
pip install -r requirements.txt
python setup.py install
```

---

## ⚙️ Configuration

Create a config file at `~/.codegate/config.yaml`:

```yaml
gemini:
  api_key: "YOUR_GEMINI_API_KEY"
  model: "gemini-1.5-pro"
  temperature: 0.1
  max_tokens: 4000

settings:
  save_history: true
  history_path: "~/.codegate/history.json"
  enable_caching: true
  cache_duration: 24

output:
  colored: true
  verbose: false
```

---

## 🚦 Usage

Launch the interactive REPL:

```bash
codegate
```

**Available Commands:**
- `scan [file]`: Analyze a Python file for vulnerabilities.
- `paste`: Enter paste mode to analyze a code snippet.
- `history`: Show your scan history.
- `help`: Show help message.
- `:quit`: Exit CodeGate.

---

## 📁 Project Structure

- `src/codegate/cli/commands.py` – CLI commands & main logic
- `src/codegate/core/` – Core analysis modules (Gemini, static, risk engine)
- `src/codegate/utils/` – Caching, config, helpers, history
- `tests/` – Test suite

---

## 🤝 Contributing

PRs, issues, and suggestions are welcome! Please open an issue for bugs or feature requests.

---

---

## 💡 Author

Created by [001Priyans](https://github.com/001Priyans).

---

> **Impress your team and secure your code with CodeGate!**
