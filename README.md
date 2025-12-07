✉️ AI-Powered Email Writer

Spring Boot + React + Chrome Extension (MV3)

An AI-based email assistant that helps you draft smart replies directly from a web UI or a browser extension.

It integrates Spring Boot 3, React, and Chrome Extension MV3 with AI APIs (OpenAI / Gemini).

🧠 Tech Stack
⚙️ Backend (API – Spring Boot)

Java 17+

Spring Boot 3

Spring Web

Spring AI (OpenAI / Gemini)

Maven

⚛️ Frontend (React App)

React 18

JavaScript/TypeScript

Axios / Fetch API

🧩 Browser Extension (MV3)

Chrome Extension Manifest V3

HTML/CSS/JS

React-based popup (optional)

📦 Project Structure
.
├── src/                     # Spring Boot backend
│   ├── main/
│   │   ├── java/...         # controllers, services, configs
│   │   └── resources/
│   │       ├── application.yml
│   │       └── templates/   # if any
│   └── test/
│
├── email-writer-react/      # React frontend
│   ├── src/
│   ├── package.json
│   └── ...
│
├── email-writer-ext/        # Chrome extension (MV3)
│   ├── manifest.json
│   ├── icons/
│   └── src/
│
├── pom.xml                  # Maven config
└── README.md

✨ Features

🤖 AI-generated email replies

🔌 REST API for integration

🖥️ React web UI

🧭 Chrome extension for Gmail, Outlook, etc.

🔐 API key based access

📦 Modular: frontend + backend + extension

🔧 Prerequisites

Install these before running:

☕ Java 17+

🧰 Maven 3+

🟦 Node.js 18+ and npm/yarn

🌐 Google Chrome / Chromium

🔑 API Key: OpenAI / Gemini

🔐 Configuration

Set your AI API key in backend config file:

src/main/resources/application.properties

ai.api.key=YOUR_API_KEY
ai.api.base-url=https://api.openai.com/v1


Or using environment variables (recommended):

export AI_API_KEY=YOUR_API_KEY_HERE
export AI_API_BASE_URL=https://api.openai.com/v1

🚀 How to Run
1️⃣ Start Backend (Spring Boot)

From project root:

mvn spring-boot:run


Runs at:

http://localhost:8080

2️⃣ Start Frontend (React App)

From project root:

cd email-writer-react
npm install
npm run dev


Opens at:

http://localhost:3000


Configure API URL in .env:

For Vite:

VITE_API_BASE_URL=http://localhost:8080


For CRA:

REACT_APP_API_BASE_URL=http://localhost:8080

3️⃣ Load Chrome Extension

Open Chrome
chrome://extensions/

Turn on Developer mode

Click Load unpacked

Select the folder:

email-writer-ext


(or dist if using bundler)

Extension icon will appear in toolbar

Make sure extension API URL = http://localhost:8080

📡 Example API Request

POST /api/v1/email/generate

Request body:

{
  "prompt": "Reply politely and ask for more details.",
  "context": "Client is asking about pricing."
}


Example response:

{
  "generatedEmail": "Hi, thanks for reaching out..."
}

## 🖼️ Additional Visuals

![Browser Extension](https://i.postimg.cc/Y0yFk1Kw/Screenshot-2025-08-07-032502.png)  
*Browser extension*

![AI Reply](https://i.postimg.cc/wTyyLRY7/Screenshot-2025-08-07-033115.png)  
*AI-powered reply*


🧪 Testing

Backend tests:

mvn test


Frontend tests:

cd email-writer-react
npm test

🛣️ Roadmap

 Support multiple AI providers

 Email history storage

 OAuth login

 Email templates (HR, support, sales)

 Export email to PDF

🤝 Contributing

Fork this repo

Create a branch feature/xyz

Commit changes

Open PR

📄 License

MIT License (or your choice)

