# 🧭 RepoPilot AI

> AI-powered GitHub repository analyzer built for IBM Bob Hackathon 2026

RepoPilot AI is a single-page web application that uses AI to analyze GitHub repositories and provide instant insights into architecture, tech stack, and codebase structure. Get onboarding guides, ask questions about any repository, and understand complex codebases in minutes.

[![IBM Bob Hackathon 2026](https://img.shields.io/badge/IBM%20Bob-Hackathon%202026-blue?style=flat-square)](https://github.com)
[![Powered by Groq](https://img.shields.io/badge/Powered%20by-Groq-orange?style=flat-square)](https://groq.com)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg?style=flat-square)](LICENSE)

## ✨ Features

- 🔍 **Repository Analysis** - Fetch and analyze any public GitHub repository
- 🏗️ **Architecture Visualization** - Understand system components, layers, and dependencies
- 🛠️ **Tech Stack Detection** - Automatically identify frameworks, libraries, and tools
- 💬 **AI-Powered Chat** - Ask questions about the codebase using Groq LLM
- 📚 **Onboarding Guide** - Auto-generate developer onboarding documentation
- 🎨 **Modern UI** - Beautiful dark theme with smooth animations

## 🚀 Quick Start

### Prerequisites

- A modern web browser (Chrome, Firefox, Safari, Edge)
- A free Groq API key ([Get one here](https://console.groq.com))

### Installation

1. **Download the file**
   ```bash
   # Clone or download index.html
   git clone <your-repo-url>
   # OR simply download index.html
   ```

2. **Get your Groq API key**
   - Visit [console.groq.com](https://console.groq.com)
   - Sign up for a free account
   - Generate an API key (starts with `gsk_`)

3. **Configure the API key** (Choose one method)

   **Method A: Edit the file (Recommended)**
   - Open `index.html` in a text editor
   - Find line 438: `const GROQ_API_KEY = 'PASTE_YOUR_GROQ_KEY_HERE';`
   - Replace `PASTE_YOUR_GROQ_KEY_HERE` with your actual key
   - Save the file

   **Method B: Enter in browser**
   - Open `index.html` in your browser
   - Paste your API key in the "Groq API Key" field
   - It will be saved in localStorage for future use

4. **Open and use**
   ```bash
   # Simply open index.html in your browser
   open index.html  # macOS
   start index.html # Windows
   xdg-open index.html # Linux
   ```

## 📖 Usage

### Analyze a Repository

1. Enter a GitHub repository URL (e.g., `https://github.com/fastapi/fastapi`)
2. Click **Analyze** button
3. Wait for the AI to process the repository
4. Explore the results across different tabs

### Navigate Tabs

- **Overview** - Repository stats, description, and quick insights
- **Architecture** - System components, layers, and relationships
- **Tech Stack** - Detected technologies and dependencies
- **Onboarding** - Step-by-step guide for new developers
- **Ask Codebase** - Interactive chat to ask questions
- **Dev Guide** - Generated markdown documentation

### Chat with the Codebase

1. Switch to the **Ask Codebase** tab
2. Type your question in the chat input
3. Press Enter to send (Shift+Enter for new line)
4. Get AI-powered answers about the repository

### Export Documentation

- Click **Download Guide** to save the onboarding documentation as `ONBOARDING.md`
- Click **Copy** to copy the guide to clipboard

## 🛠️ Technical Stack

- **Frontend**: Pure HTML/CSS/JavaScript (no build tools required)
- **AI/LLM**: Groq API (llama-3.3-70b-versatile)
- **APIs**: GitHub REST API
- **Libraries**: 
  - [Marked.js](https://marked.js.org/) - Markdown rendering
  - [Font Awesome](https://fontawesome.com/) - Icons
  - [Google Fonts](https://fonts.google.com/) - JetBrains Mono & Inter

## 🎨 Design Features

- Modern dark theme with glassmorphism effects
- Responsive layout (desktop & mobile)
- Smooth animations and transitions
- Custom scrollbars
- Live status indicators
- Progress tracking
- Error handling with user-friendly messages

## 🔧 Customization

### Modify Colors

Edit CSS variables in the `:root` selector (lines 13-20):

```css
:root {
  --bg: #0b0f1e;        /* Background */
  --card: #131929;      /* Card background */
  --blue: #4f8fff;      /* Primary color */
  --text: #e2e8f7;      /* Text color */
  /* ... more variables */
}
```

### Change AI Model

Modify the `callGroq` function (line 496) to use a different model:

```javascript
model: 'llama-3.3-70b-versatile', // Change this
```

## 📝 Example Repositories to Try

- `fastapi/fastapi` - Modern Python web framework
- `expressjs/express` - Node.js web framework
- `django/django` - Python web framework
- `vuejs/vue` - Progressive JavaScript framework
- `vercel/next.js` - React framework

## 🤝 Contributing

Contributions are welcome! This project was built for the IBM Bob Hackathon 2026.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- **IBM Bob Hackathon 2026** - For the inspiration and challenge
- **Groq** - For providing fast and powerful LLM inference
- **GitHub** - For the comprehensive API
- **Open Source Community** - For the amazing tools and libraries

## 📧 Contact

For questions or feedback about RepoPilot AI, please open an issue on GitHub.

---

<div align="center">
  <strong>Built with ❤️ for IBM Bob Hackathon 2026</strong>
  <br>
  <sub>Powered by Groq AI • No installation required • 100% client-side</sub>
</div>