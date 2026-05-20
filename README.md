# Simple Rule-Based Chatbot

A lightweight, Python-based console chatbot that interacts with users using predefined, keyword-matching rules. This project is a foundational example of a **Rule-Based Expert System** applied to Natural Language Processing (NLP).

## Table of Contents

* [Overview](https://www.google.com/search?q=%23overview)
* [How It Works](https://www.google.com/search?q=%23how-it-works)
* [Features](https://www.google.com/search?q=%23features)
* [Prerequisites](https://www.google.com/search?q=%23prerequisites)
* [How to Run](https://www.google.com/search?q=%23how-to-run)
* [Example Usage](https://www.google.com/search?q=%23example-usage)
* [Extending the Rules](https://www.google.com/search?q=%23extending-the-rules)

## Overview

This chatbot simulates a conversation by scanning user inputs for specific, predefined keywords. Unlike AI models that use machine learning to predict responses, this system relies entirely on a deterministic set of developer-defined rules stored inside a dictionary mapping.

## How It Works

1. **Input Capture:** The script opens an infinite loop (`while True`) that continuously prompts the user for text input.
2. **Pre-processing:** The system normalizes the user's text by converting it entirely to lowercase. This ensures that inputs like "HELLO", "Hello", and "hello" are treated identically.
3. **Keyword Matching:** The chatbot iterates through its knowledge base (a dictionary of rules). If a keyword is detected anywhere inside the user's sentence, the system immediately returns the corresponding response.
4. **Fallback Mechanism:** If none of the predefined keywords are found in the string, the chatbot triggers a generic fallback response asking the user to rephrase.
5. **Graceful Exit:** If the user inputs the specific commands `exit` or `quit`, the application breaks out of the loop and closes down cleanly.

## Features

* **Case-Insensitive Matching:** Processes text reliably regardless of user capitalization.
* **Substring Detection:** Finds keywords even if they are embedded within full sentences (e.g., typing *"What is the **weather** like today?"* will successfully trigger the weather response).
* **Built-in Fallback:** Handles unexpected or out-of-scope inputs gracefully without crashing.
* **Clean Session Termination:** Includes a native exit utility for terminal control.

## Prerequisites

* **Python 3.x** installed on your system.

No external libraries or third-party dependencies are required to run this project.

## How to Run

1. **Clone or Save the Code:** Save the Python script to your local machine as `chatbot.py`.
2. **Open Terminal / Command Prompt:**
Navigate to the directory where you saved the file:
```bash
cd path/to/your/folder

```


3. **Execute the Script:**
Run the file using Python:
```bash
python chatbot.py

```

## Example Usage

```text
You: Hello there!
Chatbot: Hello! How can I help you today?

You: can you help me with something?
Chatbot: Sure! I'm here to help. What do you need assistance with?

You: what is your name
Chatbot: I'm a simple rule-based chatbot. I don't have a name, but you can call me Chatbot!

You: what are you cooking?
Chatbot: I'm sorry, I don't understand that. Can you please rephrase?

You: exit
Chatbot: Goodbye! Have a good day

```
