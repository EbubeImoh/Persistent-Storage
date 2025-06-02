# Memory Agent with Persistent Storage

This project is a smart reminder assistant powered by Google ADK and Gemini, featuring persistent memory using SQLite. The agent can remember your reminders and user information across conversations.

## Features

- **Persistent Reminders:** Add, view, update, and delete reminders that are saved across sessions.
- **User Personalization:** Remembers your name and addresses you personally.
- **Interactive CLI:** Chat with the agent in your terminal.
- **State Visualization:** See your current reminders and user info before and after each interaction.

## Project Structure

```
.
├── main.py
├── utils.py
├── my_agent_data.db
├── requirements.txt
├── .env
├── memory_agent/
│   ├── __init__.py
│   └── agent.py
```

## Getting Started

### 1. Install Dependencies

```sh
pip install -r requirements.txt
```

### 2. Set Up Environment Variables

Create a `.env` file with your Google API key:

```
GOOGLE_GENAI_USE_VERTEXAI=0
GOOGLE_API_KEY=your-google-api-key
```

### 3. Run the Agent

```sh
python main.py
```

### 4. Usage

- Type your reminders or requests in the terminal.
- Type `exit` or `quit` to end the conversation.
- Your reminders and name will be remembered for future sessions.

## How It Works

- The agent uses [memory_agent/agent.py](memory_agent/agent.py) to define tools for managing reminders and user info.
- Persistent state is managed via SQLite using `google.adk.sessions.DatabaseSessionService`.
- The main loop is in [main.py](main.py), and user interaction utilities are in [utils.py](utils.py).

## Requirements

- Python 3.9+
- google-genai
- google-adk
- dotenv

## License

This project is for educational/demo purposes.
