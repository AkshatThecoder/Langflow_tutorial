
# 🚀 Langflow Streamlit Integration - Customer Query Flow

This project is a **Streamlit**-powered interface that connects to a **Langflow API** hosted on **Astra Datastax Cloud**. It allows users to enter a query and receive responses from the `Customer` flow in Langflow.

---

## 📂 Project Structure

```
.
├── main.py              # Main Streamlit app
├── secret_key.py         # API keys (should be kept private)
└── .env                   # Environment variables (not provided here)
```

---

## ⚙️ How It Works

- **User Input:** Type a question into the Streamlit app.
- **Flow Execution:** The input is sent to the `Customer` flow in Langflow.
- **Response Display:** The result from Langflow is displayed inside the Streamlit app.

---

## 📄 Requirements

Create a `requirements.txt` file with:
```
streamlit
requests
python-dotenv
```

Install dependencies:
```bash
pip install -r requirements.txt
```

---

## 📥 Setup Instructions

1. Clone this repository.
2. Add a `.env` file with your **Langflow app token**:
```
APP_TOKEN=your_actual_app_token_here
```
3. Run the app:
```bash
streamlit run main.py
```

---

## 🔑 Important Note on Keys

- **`secret_key.py`** contains sensitive keys (OpenAI, Gemini, YouTube).
- Do **NOT push this file to a public repository** — it should be added to `.gitignore`.

---

## 🌐 Example Flow URL (Replace as needed)

Your flow is called `Customer` and lives inside:
```
LANGFLOW_ID = c6e6ac48-d075-461e-8fe3-d8820b2db07e
FLOW_ID = 5d746e92-cfb7-4745-8d18-7158debba829
```
The base API URL:
```
https://api.langflow.astra.datastax.com
```

---

## ✅ Example Run

```
User Input: What are the shipment times?
Response: Shipment times depend on the product and destination. For domestic orders, typical delivery takes 3-5 business days. International orders may take 7-14 business days. Please contact support for specific queries.
```

---

## 🛠️ Future Improvements

- Add caching to avoid repetitive API calls.
- Improve error handling for better user experience.
- Consider adding response history.
