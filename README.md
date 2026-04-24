# AlexIsAgent - Custom AI Agent with Tool Calling

## Overview

AlexIsAgent is a simple AI agent built completely from scratch using Python and Groq API.
This project demonstrates how an AI assistant can use external tools (functions) to solve user queries.

In this project, the agent can answer weather-related questions by calling a custom temperature tool.

Example:

- User asks: `What is the current temperature in New York?`
- Agent decides to use tool
- Tool runs Python function
- Agent returns final answer

---

## Why This Project?

Most developers use frameworks like LangChain or LangGraph directly.

This project is different because:

- No LangChain
- No LangGraph
- No prebuilt agent system
- Full custom logic written manually

This helps in understanding how AI agents actually work internally.

---

## Features

- Custom AI Agent class
- Conversation memory support
- Tool calling support
- Automatic tool selection
- Function execution from model response
- Realistic agent workflow
- Easy to extend with more tools

---

## Technologies Used

- Python
- Groq API
- dotenv
- JSON

---

## Project Structure

```bash
project/
│── main.py
│── .env
│── README.md
```

---

## Environment Setup

Create `.env` file:

```env
GROQ_API_KEY=your_api_key_here
```

Install dependencies:

```bash
pip install groq python-dotenv
```

---

## How It Works

### 1. Load API Key

The project loads secret key from `.env`.

### 2. Create Groq Client

Used to communicate with model.

### 3. Define Tool Function

```python
get_temperature(city)
```

Returns city temperature.

### 4. Tool Schema

Model understands when to call function.

### 5. Agent Class

Custom class handles:

- user messages
- model calls
- tool execution
- final response

---

## Example Run

Input:

```python
What is the current temperature in New York?
```

Output:

```python
Response from Alex: The current temperature in New York is 25°C.
```

---

## Supported Cities

Currently tool supports:

- New York
- London
- Mumbai

Other cities return default value.

---

## Why This Project Is Valuable

This project teaches:

- Function calling
- Agent loop design
- Message memory
- Tool execution flow
- LLM integration
- AI architecture basics

---

## Future Improvements

- Real weather API integration
- Multiple tools support
- Calculator tool
- Search tool
- Memory database
- GUI chatbot
- Voice assistant
- LangGraph version

---

## Key Learning

Instead of using frameworks directly, building from scratch gives deep understanding of:

```text
User Query → LLM Decision → Tool Call → Tool Output → Final Answer
```

---

## Author

Shivam Kumar

---

## Final Note

This project may look simple, but it covers the real foundation of modern AI agents.
Every advanced framework performs similar steps internally.
