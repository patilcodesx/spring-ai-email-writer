# 📨 AI-Powered Email Writer  
### 🚀 Spring Boot + React + Chrome Extension (MV3)

An AI-based email assistant that helps you draft smart replies directly from a **web UI** or a **browser extension**.

It integrates **Spring Boot 3**, **React 18**, and a **Chrome Extension (MV3)** with AI models like **OpenAI / Gemini**.

---

## 🧠 Tech Stack Overview

### ⚙️ Backend — **Spring Boot API**
```
Java 17+
Spring Boot 3
Spring Web
Spring AI (OpenAI / Gemini)
Maven
```

### 🎨 Frontend — **React App**
```
React 18
JavaScript / TypeScript
Axios / Fetch API
Vite (recommended)
```

### 🧩 Browser Extension — **MV3**
```
Chrome Extension Manifest V3
HTML / CSS / JS
React Popup UI
```

---

## 📦 Project Structure
```
.
├── src/                     # Spring Boot backend
│   ├── main/
│   │   ├── java/...         # controllers, services, config
│   │   └── resources/
│   │       ├── application.yml
│   │       └── templates/
│   └── test/
│
├── email-writer-react/      # React frontend
│   ├── src/
│   ├── package.json
│   └── ...
│
├── email-writer-ext/        # Chrome extension (MV3)
│   ├── manifest.json
│   ├── src/
│   └── ...
│
├── pom.xml
└── README.md
```

---

## ✨ Features

- 🤖 **AI-powered email generation**
- 🎯 Use via **REST API**, **React UI**, or **Chrome Extension**
- 🔐 Secure API access using keys
- 🧩 Modular architecture
- ⚡ Fast development with Vite + Spring Boot DevTools

---

## 🔧 Requirements

Before running, install:

- ☕ Java 17+
- 🧰 Maven 3+
- 🟦 Node.js 18+ + npm/yarn
- 🌐 Chrome Browser
- 🔑 API Key from OpenAI/Gemini

---

## 🔐 Configuration

Edit `application.properties`:

```
ai.api.key=YOUR_API_KEY
ai.api.url=https://api.openai.com/v1
```

Recommended — **environment variables**:

```
export AI_API_KEY=YOUR_API_KEY
export AI_API_URL=https://api.openai.com/v1
```

---

## 🚀 Run the Project

### 1️⃣ Start Backend (Spring Boot)

```
mvn spring-boot:run
```

Backend URL:

```
http://localhost:8080
```

---

### 2️⃣ Start Frontend (React UI)

```
cd email-writer-react
npm install
npm run dev
```

Web UI:

```
http://localhost:3000
```

Check `.env`:

```
VITE_API_BASE_URL=http://localhost:8080
```

---

### 3️⃣ Load Chrome Extension

- Open Chrome
- Go to: `chrome://extensions/`
- Enable **Developer mode**
- Click **Load unpacked**
- Select: `email-writer-ext` (or `dist` folder)

---

## 📡 API Example

**POST** `/api/v1/email/generate`

Request Body:

```json
{
  "prompt": "Reply politely with more details.",
  "context": "Client asked about pricing."
}
```

Response:

```json
{
  "generatedEmail": "Hi, thanks for reaching out..."
}
```

---


## 🖼️ Additional Visuals

![Browser Extension](https://i.postimg.cc/Y0yFk1Kw/Screenshot-2025-08-07-032502.png)  
*Browser extension*

![AI Reply](https://i.postimg.cc/wTyyLRY7/Screenshot-2025-08-07-033115.png)  
*AI-powered reply*



## 🧪 Testing

Backend:
```
mvn test
```

Frontend:
```
cd email-writer-react
npm test
```



