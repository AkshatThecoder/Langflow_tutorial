
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
