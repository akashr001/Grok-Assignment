## Task 1: Conversation Management & Summarization
- Maintains conversation history between user and assistant.
- Summarizes the conversation every K messages (k-th run summarization).
- Truncates history to last `MAX_TURNS` messages to keep context concise.

### How it Works
- `conversation_history` stores all messages.
- `chat_with_groq(user_input)` function:
  1. Adds user input to history.
  2. Summarizes conversation every K messages.
  3. Sends request to Groq API and returns assistant reply.
  4. Truncates history to last `MAX_TURNS` messages.



