# 🧠 RAG Q&A Conversation With PDF (Chat History Enabled)

This project is a **Conversational Retrieval-Augmented Generation (RAG)** app built using **Streamlit**. It allows users to **upload PDF documents** and interact with them in a **chat-like interface**, powered by **LangChain**, **Groq**, and **Chroma**. The system maintains **chat history**, supports **context-aware question reformulation**, and uses **HuggingFace embeddings** for document retrieval.

---

## 🚀 Features

- 📄 Upload one or more PDF documents.
- 🗣️ Ask questions about the content in natural language.
- 💬 Maintains full chat history for context-aware responses.
- 🔁 Reformulates user questions based on conversation history.
- 🧠 Uses RAG (Retrieval-Augmented Generation) to answer from relevant document chunks.
- ⚡ Powered by Groq’s **Gemma2-9b-It** language model.
- 🧩 Modular and extendable with LangChain components.

---

## 🧰 Built With

- [Streamlit](https://streamlit.io/)
- [LangChain](https://www.langchain.com/)
- [LangChain Chroma](https://python.langchain.com/docs/integrations/vectorstores/chroma)
- [Groq API](https://console.groq.com/)
- [HuggingFace Transformers](https://huggingface.co/)
- [Chroma Vectorstore](https://www.trychroma.com/)
- [Python-dotenv](https://pypi.org/project/python-dotenv/)

---

## 📦 Installation

1. **Clone the repository**:

   ```bash
   git clone https://github.com/nak5hatra/PDFRAG.git
   cd PDFRAG
   ```

2. **Create a virtual environment**:
    ```bash
    python -m venv venv
    source venv/bin/activate  # or venv\Scripts\activate on Windows
    ```
3. **Install dependencies**:
    ```bbash
    pip install -r requirements.txt
    ```
4. **Set up environment variables**:
    Create a .env file and add your HuggingFace token:
    ```bash
    HF_TOKEN=your_huggingface_token
    ```
## 🔑 Required API Keys

- Groq API Key (for LLM processing)
- HuggingFace Token (for generating document embeddings)

## ▶️ Running the App
    streamlit run app.py
### Once running, you'll be able to:
  1. Enter your Groq API key in the UI.
  2. Upload one or more PDF files.
  3. Start chatting and asking questions about the PDF content!

## 📂 Project Structure
    ├── app.py              # Main Streamlit app
    ├── requirements.txt    # Python dependencies
    └── .env                # Environment variables (not included in repo)
## 📌 Notes
- Chunk size and overlap are set to 5000 and 500 respectively for optimal PDF splitting.
- Chat history is stored in-memory per session using Streamlit’s session state.
- Reformulated queries help handle follow-up questions more intelligently.

## 💡 Acknowledgments
Thanks to the teams behind:
  - LangChain
  - Groq
  - HuggingFace
  - Streamlit
  - Chroma
