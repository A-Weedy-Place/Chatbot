# Chatbot

## 📌 What this project is
This is a **terminal-based chatbot** built using **Facebook’s BlenderBot-400M-distill**, a conversational AI model.  
It can remember previous turns in a conversation and generate context-aware responses.

---

## 📦 Libraries Used

### 1. [transformers](https://huggingface.co/transformers/)
- A library by Hugging Face that provides state-of-the-art **Natural Language Processing (NLP)** models.
- It allows us to load pre-trained **LLMs (Large Language Models)** like BlenderBot.

### 2. [torch (PyTorch)](https://pytorch.org/)
- A deep learning framework used under the hood by Hugging Face models.
- Handles the **tensor computations** and model execution (CPU/GPU).

### Key Concepts:
- **LLM (Large Language Model):** A neural network trained on huge amounts of text to understand and generate human-like language.  
- **Transformer:** A neural network architecture designed for sequential data (like text). BlenderBot is built on this.  
- **Tokenizer:** A tool that converts text into numbers (tokens) the model understands, and back into words.

---

## 🛠 What the Code Does
1. Loads the **BlenderBot-400M-distill** model and tokenizer.
2. Keeps track of the **conversation history**.
3. Takes user input from the terminal.
4. Feeds the conversation + user input to the model.
5. Generates and prints a response.
6. Repeats, allowing a continuous chat.

---

## 🚀 How to Use It
1. Install dependencies:
   ```bash
   pip install transformers torch
