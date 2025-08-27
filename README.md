# Chatbot

## 📌 What this project is
This is a **web-based chatbot** built using **Facebook's BlenderBot-400M-distill**, a conversational AI model.  
It can remember previous turns in a conversation and generate context-aware responses.

---

## 📦 Libraries Used

### 1. [transformers](https://huggingface.co/transformers/)
- A library by Hugging Face that provides state-of-the-art **Natural Language Processing (NLP)** models.
- It allows us to load pre-trained **LLMs (Large Language Models)** like BlenderBot.

### 2. [torch (PyTorch)](https://pytorch.org/)
- A deep learning framework used under the hood by Hugging Face models.
- Handles the **tensor computations** and model execution (CPU/GPU).

### 3. [Flask](https://flask.palletsprojects.com/)
- A lightweight web framework for Python.
- Handles HTTP requests and serves the web interface.

### 4. [Flask-CORS](https://flask-cors.readthedocs.io/)
- An extension for Flask that handles Cross-Origin Resource Sharing (CORS).
- Enables the frontend to communicate with the backend API.

### Key Concepts:
- **LLM (Large Language Model):** A neural network trained on huge amounts of text to understand and generate human-like language.  
- **Transformer:** A neural network architecture designed for sequential data (like text). BlenderBot is built on this.  
- **Tokenizer:** A tool that converts text into numbers (tokens) the model understands, and back into words.

---

## 🛠 What the Code Does

### Backend (app.py):
1. Loads the **BlenderBot-400M-distill** model and tokenizer.
2. Creates a Flask web server with API endpoints.
3. Keeps track of the **conversation history**.
4. Receives user messages via HTTP POST requests.
5. Feeds the conversation + user input to the model.
6. Generates responses and sends them back to the frontend.

### Frontend (script.js):
1. Provides a user interface for the chat.
2. Captures user input from the message form.
3. Sends messages to the backend API.
4. Displays a loading animation while waiting for responses.
5. Renders both user messages and AI responses in the chat window.

---

## 🚀 How to Use It

1. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

2. Start the Flask server:
   ```bash
   python app.py
   ```

3. Open your browser and navigate to:
   ```
   http://127.0.0.1:5000/
   ```

4. Type your message in the input field and press Enter to chat with the AI.

---

## 📁 Project Structure

- **app.py**: The Flask backend that handles the AI model and API endpoints.
- **requirements.txt**: List of Python dependencies.
- **templates/index.html**: The HTML structure of the web interface.
- **static/script.js**: JavaScript code for the frontend functionality.
- **static/css/style.css**: CSS styles for the user interface.
- **static/**: Directory containing images and icons used in the interface.
