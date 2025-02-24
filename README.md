# Jarvis-Voice-Assistant
A human-like voice assistant with advanced NLP capabilities

*Python-powered AI companion featuring voice interaction, browser automation, and GPT-4 integration*

[![Python Version](https://img.shields.io/badge/python-3.8%2B-blue)](https://www.python.org/)
[![OpenAI](https://img.shields.io/badge/API-OpenAI-green)](https://openai.com/)

## Features 🌟
- 🗣️ Natural voice interaction with emotional inflection
- 🧠 GPT-4 powered contextual understanding
- 🌐 Chrome browser automation
- ⏰ Time-aware responses
- 💡 Personality matrix with dynamic responses
- 🔄 Conversation memory and context retention
- 📦 Modular architecture for easy expansion

## Complete System Workflow

### 1. Initialization Sequence 🌟
```python
1. Environment Setup:
   - Load API keys from .env file
   - Initialize OpenAI client with GPT-4
   - Configure speech engine (pyttsx3)
   - Prepare Chrome driver (Selenium)

2. Personality Activation:
   - Load greeting/farewell templates
   - Set emotional response parameters
   - Initialize conversation memory

3. Hardware Check:
   - Test microphone availability
   - Verify speaker functionality
   - Establish Google Speech Recognition connection

          ┌────────────────────────┐
          │  Voice Input           │
          │  (Listening State)     │
          └──────────┬─────────────┘
                     ↓
          ┌────────────────────────┐
          │  Speech Recognition    │
          │  (Google API)          │
          └──────────┬─────────────┘
                     ↓
          ┌────────────────────────┐
          │  Command Analysis      │
          │  - Intent Detection    │
          │  - Context Matching    │
          └──────────┬─────────────┘
                     ↓
          ┌────────────────────────┐
          │  GPT-4 Processing      │
          │  - Memory Augmentation │
          │  - Response Generation │
          └──────────┬─────────────┘
                     ↓
          ┌────────────────────────┐
          │  Action Execution      │
          │  - Browser Control     │
          │  - Voice Response      │
          │  - Memory Update       │
          └────────────────────────┘
```

### 2. Memory Management 🧠

Short-term: In-memory list (conversation_history)

Context Window: Last 6 messages (3 exchanges)

Persistent Storage: None (volatile memory only)


### 3. Command Processing Flow ⚙️

Voice Input -> Text Conversion

Command Type Detection:

Browser Operations (Chrome control)

Information Requests (GPT-4 queries)

Conversation Continuation

System Commands (Exit/Reset)

Contextual Enrichment:

Add user name reference

Include time awareness

Attach previous interactions

### 4. Action Execution Matrix:

Command Type	Action	Example
open chrome	Launch browser	"Open Chrome"
search for	Google search	"Search for AI news"
what is	GPT-4 explanation	"What is quantum computing"
exit	Clean shutdown	"Goodbye Jarvis"

### 5. Technical Stack:

Selenium WebDriver

Chrome Options Configuration

Explicit Waits (10s timeout)

XPath/CSS Selector Handling

