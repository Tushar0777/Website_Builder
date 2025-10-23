# AI-Powered Terminal Web Dev Agent

An AI agent that automatically builds frontend projects (`index.html`, `style.css`, `script.js`) by executing terminal commands. Uses **Google Gemini AI** to plan, execute, and validate steps.

---

## Features

- Execute any terminal command programmatically.
- OS-aware multi-line file writing:
  - **Linux/macOS:** `cat << 'EOF'`
  - **Windows:** PowerShell `Set-Content` with here-strings (`@' ... '@`)
- Validates each step by reading back file content.
- Maintains a history of all actions and AI responses.
- Interactive terminal prompt.

---

## Prerequisites

- Node.js (v18+)
- NPM/Yarn
- Google GenAI API key

---

## Installation

```bash
git clone <repo-url>
cd <repo-folder>
npm install
Add your API key in index.js:

javascript
Copy code
const ai = new GoogleGenAI({ apiKey: "YOUR_API_KEY_HERE" });
Usage
bash
Copy code
node index.js
Type your request, e.g.:

css
Copy code
Create a calculator website
The agent will create the project folder, files, populate them, and validate content.