# LLM API Server

A Node.js backend server that provides a simple API layer for interacting with multiple Large Language Model (LLM) providers.

The goal is to keep the frontend independent from individual AI providers by exposing a common backend API.

## 🚀 Features

* Node.js backend server
* Express.js REST API
* Multiple LLM provider integrations
* Centralized API handling
* Environment variable support for API keys
* JSON request/response format
* Easy to add new LLM providers
* Modular route structure

## 🛠️ Tech Stack

* Node.js
* Express.js
* JavaScript
* REST APIs
* LLM APIs

## 📂 Project Structure

```text
server/
│
├── routes/
│   ├── openai.js
│   ├── gemini.js
│   ├── claude.js
│   └── api.js
│
├── controllers/
│   ├── openaiController.js
│   ├── geminiController.js
│   └── claudeController.js
│
├── services/
│   ├── openaiService.js
│   ├── geminiService.js
│   └── claudeService.js
│
├── .env
├── .gitignore
├── package.json
└── server.js
```

## 📦 Installation

Clone the repository:

```bash
git clone https://github.com/Parasgera5/Tutorial.git
```

Navigate to the server directory:

```bash
cd Tutorial/server
```

Install dependencies:

```bash
npm install
```

## 🔑 Environment Variables

Create a `.env` file in the server directory:

```env
PORT=5000

OPENAI_API_KEY=your_openai_api_key
GEMINI_API_KEY=your_gemini_api_key
ANTHROPIC_API_KEY=your_anthropic_api_key
```

Never commit your `.env` file to GitHub.

Add it to `.gitignore`:

```gitignore
node_modules/
.env
```

## ▶️ Running the Server

Start the server:

```bash
node server.js
```

For development:

```bash
npm run dev
```

The server will run on:

```text
http://localhost:5000
```

## 🔗 API Endpoints

### OpenAI

```http
POST /api/openai
```

Example request:

```json
{
  "prompt": "Explain recursion in simple terms"
}
```

### Gemini

```http
POST /api/gemini
```

Example request:

```json
{
  "prompt": "Explain how REST APIs work"
}
```

### Claude

```http
POST /api/claude
```

Example request:

```json
{
  "prompt": "Write a JavaScript function to reverse a string"
}
```

## 📡 Example Response

```json
{
  "success": true,
  "response": "Recursion is a technique where a function calls itself..."
}
```

## 🔄 Request Flow

```text
Client
   │
   ▼
Node.js / Express Server
   │
   ├── /api/openai ──► OpenAI API
   │
   ├── /api/gemini ──► Gemini API
   │
   └── /api/claude ──► Claude API
   │
   ▼
JSON Response
   │
   ▼
Client
```

## 🧪 Testing

You can test the APIs using:

* Postman
* Thunder Client
* cURL
* Frontend applications

Example using cURL:

```bash
curl -X POST http://localhost:5000/api/gemini \
-H "Content-Type: application/json" \
-d "{\"prompt\":\"What is Node.js?\"}"
```

## 📌 Future Improvements

* Streaming LLM responses
* Authentication
* Rate limiting
* Request validation
* Conversation history
* Token usage tracking
* Response caching
* AI model selection
* Error handling and retries
* Logging and monitoring

## 👨‍💻 Author

**Paras Gera**

GitHub: [Parasgera5](https://github.com/Parasgera5)
