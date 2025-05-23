
# Text-to-SQL Framework

This is a lightweight and modular framework designed for students in LLM (Large Language Models) course to build and evaluate Text-to-SQL models. The framework includes data loading, SQL generation evaluation, and a consistent interface to run custom methods.

---

## 📁 Project Structure

```

.
├── data/                   # Dataset files (e.g., SQLite DBs, JSONs)
├── nano_data/             # Main codebase
│   bird_loader.py     # Loads and preprocesses the bird dataset
│   ├── db_manager.py      # Manages database interactions
│   ├── evaluation.py      # Provides evaluation metrics and helpers
│   ├── run_method.py      # Defines the `run_method` executor
├── requirements.txt       # Python dependencies

````

---

## 🚀 Quick Start

### 1. **Clone the Repository**

```bash
git clone https://github.com/safdarian/text2sql-framework.git
cd text2sql-framework
````

### 2. **Install Dependencies**

```bash
pip install -r requirements.txt
```

### 3. **Write Your Method**

Implement a function using this template:

````python
from method_run import run_method

def function_template(item):
    # Your Code Here
    query = ""
    return {**item, 'sql': query}
````

### 4. **Run Your Method**

Use the framework's runner to evaluate your method:

```python
run_method(function_template, SLEEP_TIME=10, mode="dev")
```

You can change the `mode` to `"nano"` depending on what you’re testing.

---

## 🧪 Evaluation

The `evaluation.py` script will help you compare your generated SQL with ground truth using logical and execution-based metrics.

---

## 🎓 For Students

You’re encouraged to:

* Write and test custom SQL generation logic
* Use `db_manager.py` to query the database
* Use `run_method.py` for execution and evaluation.

---

## 🤝 Contributing

This project is intended for educational purposes. Contributions (e.g., fixes, enhancements) are welcome via issues or pull requests.

---

## 📄 License

MIT License


