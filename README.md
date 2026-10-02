# ✈️ TravelBuddy Agent with Memory

TravelBuddy is an AI-powered travel planning agent built with **LangChain** and **LangGraph**.

It helps users plan trips by:

* Researching destinations and attractions
* Searching for flight options
* Maintaining conversational memory across multiple messages

The project uses **Google Gemini** as the LLM, **Tavily** for destination research, and **SerpAPI Google Flights** for flight searches.

## 🚀 Features

* 🤖 AI travel assistant powered by Google Gemini
* 🌍 Destination research using Tavily
* ✈️ Flight search using SerpAPI Google Flights
* 🧠 Conversational memory using LangGraph
* 💬 Multi-turn conversations
* 📅 Travel-date aware flight searches
* 🔑 Environment variable support for API keys

## 🏗️ Architecture

```text
                         User
                           │
                           ▼
                  ┌─────────────────┐
                  │   TravelBuddy   │
                  │      Agent      │
                  └────────┬────────┘
                           │
                 ┌─────────┴─────────┐
                 ▼                   ▼
        ┌────────────────┐   ┌────────────────┐
        │     Tavily     │   │    SerpAPI     │
        │   Destination  │   │ Google Flights │
        │    Research    │   │     Search     │
        └────────────────┘   └────────────────┘
                 │                   │
                 └─────────┬─────────┘
                           ▼
                  ┌─────────────────┐
                  │    LangGraph    │
                  │     Memory      │
                  │  InMemorySaver  │
                  └────────┬────────┘
                           │
                           ▼
                    Google Gemini
                           │
                           ▼
                    Final Response
```

## 🛠️ Tech Stack

| Technology    | Purpose                         |
| ------------- | ------------------------------- |
| Python        | Programming language            |
| LangChain     | Agent and tool integration      |
| LangGraph     | Conversation memory             |
| Google Gemini | Large Language Model            |
| Tavily        | Destination web research        |
| SerpAPI       | Google Flights search           |
| python-dotenv | Environment variable management |

## 📁 Project Structure

```text
travelbuddy-agent-memory/
│
├── app.py
├── .env
├── .gitignore
├── requirements.txt
└── README.md
```

## ⚙️ Installation

Clone the repository:

```bash
git clone https://github.com/YOUR_USERNAME/travelbuddy-agent-memory.git
cd travelbuddy-agent-memory
```

Create a virtual environment:

```bash
python -m venv venv
```

Activate the virtual environment on Linux/macOS:

```bash
source venv/bin/activate
```

On Windows:

```bash
venv\Scripts\activate
```

Install the dependencies:

```bash
pip install -r requirements.txt
```

## 📦 Required Packages

Your project uses the following packages:

```text
langchain
langchain-google-genai
langgraph
langchain-tavily
google-search-results
python-dotenv
requests
```

You can install them with:

```bash
pip install -U langchain langchain-google-genai langgraph langchain-tavily google-search-results python-dotenv requests
```

## 🔑 API Keys

Create a `.env` file in the project root:

```env
GOOGLE_API_KEY=your_google_gemi
```
