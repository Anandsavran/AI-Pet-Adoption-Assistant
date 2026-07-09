<div align="center">
 
<!-- HEADER BANNER -->   
<img src="https://capsule-render.vercel.app/api? type=waving&color=0:1a1a2e,50:16213e,100:0f3460&height=200&section=header&text=Paws%20Hearts&fontSize=38&fontColor=4fc3f7&fontAlignY=38&desc=Paws%20&%20Hearts%20AI%20Pet%20Adoption%20Assistant&descAlignY=58&descColor=90caf9&animation=fadeIn" width="100%"/>
 
# 🐾 Paws & Hearts — AI Pet Adoption Assistant    
 
> **Making pet adoption easier, friendlier, and smarter — one conversation at a time.**  

[![HTML](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![CSS](https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/CSS)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![Gemini API](https://img.shields.io/badge/Gemini%20API-4285F4?style=flat-square&logo=google&logoColor=white)](https://ai.google.dev/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg?style=flat-square)](LICENSE)

</div>

---

## 📖 About

**Paws & Hearts** is an AI-powered pet adoption assistant that simulates a warm, intelligent chatbot experience to help users find their perfect furry companion. It understands natural language queries, recommends pets based on user preferences, guides users through the adoption process, and even lets them submit adoption interest forms — all within a single conversational interface.

---

## ✨ Features

| Feature | Description |
|---|---|
| 🤖 **AI Chatbot** | Gemini-powered responses for any pet-related query |
| 🐶 **Pet Recommendations** | Suggests pets by breed, size, energy level, and lifestyle |
| 🃏 **Pet Cards** | Visual cards with photo, age, breed, shelter info, and adoption link |
| ⚡ **Quick Replies** | One-tap buttons like *Find a Dog*, *Find a Cat*, *Adoption Tips* |
| 📋 **Adoption Form** | In-chat form to submit name, email, phone, and adoption reason |
| 💬 **Context-Aware Chat** | Maintains conversation history for follow-up questions |
| 🏠 **Shelter Info** | Footer navigation with shelter details, adoption process, and contact |

---

## 🏗️ System Architecture

```
┌──────────────┐
│     User     │
└──────┬───────┘
       │
┌──────▼──────────────┐         ┌───────────────────────┐
│   Chat Interface    │ ◄─────► │   Gemini AI Response  │
│  (HTML/CSS/JS)      │         │      (Dynamic AI)     │
└──────┬──────────────┘         └───────────────────────┘
       │
┌──────▼──────────────────┐
│  Pet Recommendation     │
│       Logic             │
└──────┬──────────────────┘
       │
┌──────▼──────────────────┐
│   Mock Pet Database     │
│  (Local JS Dataset)     │
└─────────────────────────┘
```

**Data Flow:**
1. User sends a message or taps a quick reply
2. JavaScript checks the mock DB for keyword matches (e.g., *dog*, *apartment*)
3. If matched → Pet cards are rendered directly
4. If not matched → Query is sent to Gemini API with conversation context
5. AI response is displayed in the chat bubble layout

---

## 🧩 Component Breakdown

### 1. 🖥️ Frontend (HTML + CSS)
- Chat bubble layout with **fade-in animations** and **typing indicators**
- Warm, welcoming UI with decorative elements and background imagery
- Fully **responsive** design
- Quick reply buttons for guided navigation

### 2. ⚙️ Chatbot Interaction Layer (JavaScript)
- Keyword detection for intents like `dogs`, `cats`, `apartment`, `energy`
- Handles quick replies, form submission, and message rendering
- Stores **chat history** for context-aware follow-ups

### 3. 🗃️ Static Pet Database
- Mock dataset embedded in JavaScript
- Each pet record includes: `name`, `breed`, `age`, `image`, `energy level`, `shelter`
- Simulates real API data for demos and testing

### 4. 🤖 Gemini API Integration
- Handles queries not covered by the static database
- Prompt-engineered to be **informative, warm, and human-like**
- Example: *"What dog breeds are good for kids?"* → AI answers with context
- Falls back gracefully by asking clarifying questions when unsure

---

## 🚀 Getting Started

### Prerequisites
- A modern web browser (Chrome, Firefox, Edge)
- A valid [Gemini API Key](https://ai.google.dev/)

### Installation

```bash
# Clone the repository
git clone https://github.com/your-username/paws-and-hearts.git

# Navigate into the project
cd paws-and-hearts
```

### Configuration

Open the main JavaScript file and replace the placeholder with your Gemini API key:

```javascript
const GEMINI_API_KEY = "YOUR_API_KEY_HERE";
```

### Run

Simply open `index.html` in your browser — no build step required.

```bash
# Or serve locally
npx serve .
```

---

## 💡 AI Assistant Design

### Prompt Engineering
- The Gemini API is prompted to respond as a **friendly, knowledgeable pet adoption advisor**
- Responses follow a consistent format: pet info → care tips → next steps
- Ensures replies are warm, supportive, and actionable

### Context Maintenance
- Chat history is stored and sent with each API call
- Enables meaningful follow-ups like *"Tell me more about Luna"*

### Fallback Handling
- If the query is ambiguous, the AI responds with **clarifying questions**
- Example: *"Are you looking for a dog or a cat? And do you have a large or small living space?"*

---

## 📁 Project Structure

```
paws-and-hearts/
│
├── index.html          # Main HTML structure
├── style.css           # Styling, animations, responsive layout
├── script.js           # Chatbot logic, Gemini API calls, pet DB
├── assets/
│   ├── images/         # Pet images and background
│   └── icons/          # UI icons
└── README.md
```

---

## 🛣️ Roadmap

- [ ] Connect to a live pet adoption API (e.g., Petfinder API)
- [ ] Add user authentication for saved favorites
- [ ] Enable real shelter booking/appointment scheduling
- [ ] Mobile app wrapper (PWA)
- [ ] Multi-language support

---

## 🤝 Contributing

Contributions are welcome! Feel free to open an issue or submit a pull request.

```bash
# Fork the repo, then:
git checkout -b feature/your-feature-name
git commit -m "Add: your feature description"
git push origin feature/your-feature-name
```
---

<div align="center">

Made with ❤️ for pets and the people who love them.

*Every pet deserves a forever home.*
<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f3460,50:16213e,100:1a1a2e&height=100&section=footer" width="100%"/>

*⭐ Star this repo if you found it helpful!*


</div>





