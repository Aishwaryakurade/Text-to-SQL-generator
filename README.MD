
# 🧠 Text-to-SQL Generator

A powerful Natural Language to SQL interface designed for stakeholders, business users, and non-technical personnel. This tool replaces the need for a dedicated data analyst by allowing users to retrieve data from an SQLite database using simple English queries.

---

## 🚀 Features

- ✅ Converts English questions to SQL using LLaMA-3 via Groq API
- ✅ Uses LangChain for structured prompting
- ✅ Queries data from a local SQLite database (`student.db`)
- ✅ Clean and interactive Streamlit web UI
- ✅ .env file support for secure API key management
- ✅ Fully extensible and lightweight

---

## 📌 Use Case

**Problem**: Stakeholders often need quick access to data but lack SQL skills.

**Solution**: This project lets them query the database by simply typing natural language questions like:

```

"How many students scored more than 90?"

```

🔁 Behind the scenes:
1. LLM converts it to SQL: `SELECT COUNT(*) FROM STUDENT WHERE MARKS > 90;`
2. SQL is executed on `student.db`
3. Result is displayed in the Streamlit app

---

## 📂 Project Structure

```

📁 text-to-sql-generator/
├── venv/                   # Virtual environment (ignored in Git)
├── .env                   # Contains API keys (e.g., GROQ\_API\_KEY)
├── .gitignore             # Ignores venv, .env, etc.
├── database.py            # Sets up the database
├── main.py                # Streamlit app entry point
├── README.md              # Project documentation
├── requirements.txt       # Python dependencies
└── student.db             # SQLite database file

````

---

## ⚙️ Installation

### 1. Clone the repository
```bash
git clone https://github.com/yourusername/text-to-sql-generator.git
cd text-to-sql-generator
````

### 2. Create and activate virtual environment

```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Add your Groq API key to `.env`

```
GROQ_API_KEY=your_actual_groq_api_key
```

---

## 🧪 Run the App

```bash
streamlit run main.py
```

Then go to `http://localhost:8501` in your browser.

---

## 📊 Example Questions

* "Show all students in Section A"
* "How many students are in Data Science?"
* "List all students with marks above 85"
* "What is the average score in DEVOPS?"

---

## 🔐 Security & Notes

* ✅ `.env` is included in `.gitignore` for secure key storage.
* ❌ Avoid allowing arbitrary SQL input from users. Always validate.
* 📌 Only the `STUDENT` table is supported in this version.

---

## 💡 Future Enhancements

* Connect to live production databases (PostgreSQL, MySQL)
* Add user authentication
* Expand to multiple tables and schemas
* Export results to CSV
* Add data visualizations (charts, graphs)


---

## 🤝 Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

---

## 🙋‍♀️ Built With

* [Streamlit](https://streamlit.io/)
* [LangChain](https://www.langchain.com/)
* [LLaMA 3 via Groq](https://console.groq.com/)
* [SQLite](https://www.sqlite.org/index.html)




