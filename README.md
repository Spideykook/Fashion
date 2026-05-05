# 🛍️ Fashion – AI Shopping Assistant

Fashion is a Django-based conversational shopping assistant that allows users to search for products and get support-related answers using natural language.

Instead of browsing through filters or categories, users can simply ask:

> “Find me a black dress under ₹3000 and what’s your return policy?”

The system is designed to handle both product discovery and support queries within a single conversation.

---

## ✨ Features

* 💬 Chat-based interface for product discovery
* 🛒 Natural language product search
* 📦 Handles support queries (returns, availability, etc.)
* 🔀 Basic query routing between product and support logic
* 🧠 Maintains short conversation context within a session

---

## 🧩 Tech Stack

* **Backend:** Django
* **Frontend:** HTML, CSS
* **Database:** PostgreSQL
* **Search:** FAISS + Sentence Transformers
* **AI Responses:** Llama 3 via Ollama

---

## ⚙️ How It Works

* The user sends a query through the chat interface
* The system determines the intent of the query
* Product queries are matched using vector search
* Support queries are handled using predefined logic
* A response is generated and returned to the user

This project focuses on building a practical conversational interface for e-commerce use cases.

---

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/Spideykook/Fashion.git
cd Fashion
```

---

### 2. Create a virtual environment

```bash
python -m venv venv
venv\Scripts\activate   # Windows
```

---

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

---

### 4. Configure PostgreSQL

Update your database settings in `core/settings.py` with your PostgreSQL credentials.

---

### 5. Run migrations

```bash
python manage.py migrate
```

---

### 6. Seed demo data (recommended)

```bash
python manage.py seed_demo
```

---

### 7. Build search index

```bash
python manage.py rebuild_index
```

> ⚠️ This downloads a model (~80MB) on first run.

---

### 8. Install and run Ollama (for AI responses)

Download Ollama: https://ollama.com

```bash
ollama pull llama3
```

Make sure Ollama is running before starting the server.

---

### 9. Run the server

```bash
python manage.py runserver
```

Open:
👉 http://127.0.0.1:8000/

---

## 🧪 Notes

* The FAISS index is not included in the repository and is generated locally
* The application runs without Ollama, but AI-generated responses require it

---

## 📁 Project Structure

```
chatbot/        # Chat handling logic
core/           # Django project settings
products/       # Product models and views
support/        # Support-related responses
templates/      # HTML templates
manage.py
requirements.txt
```

---

## 🎯 Future Improvements

* Improve search relevance and ranking
* Add product recommendations
* Enhance chat UI/UX
* Extend conversation memory

---

## 👩‍💻 Author

Built as a learning project to explore how conversational interfaces can improve online shopping experiences.
