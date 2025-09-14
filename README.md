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



## **Task 2: JSON Schema Classification & Extraction**

* Extracts structured information from user chat messages.
* Converts unstructured chat text into a JSON object following a predefined schema.
* Useful for collecting user details like name, email, phone, location, and age.

### **How it Works**

* `info_schema` defines the required fields: `name`, `email`, `phone`, `location`, `age`.
* `extract_info(user_input)` function:

  1. Takes a user chat message as input.
  2. Sends the message and schema to Groq API.
  3. Receives structured JSON output with extracted information.
  4. Returns or prints the JSON object for further use.

