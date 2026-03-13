# 🤖 AI Task Manager

An **AI-powered task management assistant** built using **LangChain,
Groq LLM, SQLite, and Streamlit**. The application allows users to
**create, read, update, and delete tasks using natural language**.

Instead of manually writing SQL queries, users can simply chat with the
AI and it will manage the tasks stored in the database.

------------------------------------------------------------------------

# 🚀 Features

## 🧠 AI-powered Task Management

Users interact with the system using natural language such as:

Add a task to complete my assignment\
Show my pending tasks\
Mark task 3 as completed\
Delete the task "buy groceries"

The AI agent automatically converts these instructions into SQL
operations.

------------------------------------------------------------------------

## 📋 CRUD Operations Supported

  Operation     Example Prompt
  ------------- -----------------------------------
  Create Task   "Add a task to finish my project"
  View Tasks    "Show my tasks"
  Update Task   "Mark task 2 as completed"
  Delete Task   "Delete task 5"

------------------------------------------------------------------------

## 🗄️ Database Integration

The project uses **SQLite** to store tasks.

Table Schema:

  Column        Type        Description
  ------------- ----------- -----------------------------------
  id            INTEGER     Primary Key
  title         TEXT        Task title
  description   TEXT        Task details
  status        TEXT        pending / in_progress / completed
  created_at    TIMESTAMP   Task creation time

------------------------------------------------------------------------

# 🧩 Tech Stack

  Technology   Purpose
  ------------ -----------------------
  Python       Core language
  Streamlit    Web UI
  LangChain    AI Agent framework
  Groq LLM     Large language model
  SQLite       Database
  LangGraph    Agent memory handling

------------------------------------------------------------------------

# 🏗️ Project Structure

    AI_task_manager
    │
    ├── main.py
    ├── my_tasks.db
    ├── requirements.txt
    ├── pyproject.toml
    ├── uv.lock
    ├── README.md
    ├── how_to_run.txt
    └── .gitignore

------------------------------------------------------------------------

# ⚙️ Installation

### 1️⃣ Clone the Repository

``` bash
git clone https://github.com/Rajatkpaliwal/AI_task_manager.git
cd AI_task_manager
```

### 2️⃣ Create Virtual Environment

``` bash
python -m venv venv
```

Activate it:

Windows

    venv\Scripts\activate

Mac/Linux

    source venv/bin/activate

### 3️⃣ Install Dependencies

    pip install -r requirements.txt

### 4️⃣ Setup Environment Variables

Create a `.env` file in the root directory.

Example:

    GROQ_API_KEY=your_api_key_here

------------------------------------------------------------------------

# ▶️ Running the Application

Start the Streamlit app:

    streamlit run main.py

Then open:

http://localhost:8501

------------------------------------------------------------------------

# 💬 Example Commands

Create Tasks

Add a task to complete my AI project

View Tasks

Show my tasks

Update Tasks

Mark task 1 as completed

Delete Tasks

Delete task 3

------------------------------------------------------------------------

# 🧠 How It Works

### Step 1 --- User Input

User sends a natural language instruction.

Example:

Add a task to buy groceries

### Step 2 --- AI Agent Processing

The LangChain agent: 1. Understands user intent 2. Converts the request
into SQL 3. Executes the query on SQLite 4. Returns structured results

### Step 3 --- Database Execution

Example SQL generated:

``` sql
INSERT INTO tasks(title, description, status)
VALUES ('buy groceries', '', 'pending');
```

### Step 4 --- Result Display

The assistant confirms the operation and displays the updated task list.

------------------------------------------------------------------------

# 🔐 Safety Rules Implemented

The agent follows these constraints:

-   Maximum **10 rows returned per query**
-   Every write operation verified using a SELECT query
-   Structured table output for UI display

------------------------------------------------------------------------

# 📌 Future Improvements

Possible enhancements:

-   Task reminders
-   Multi-user authentication
-   Task priorities
-   Due dates
-   Task categories
-   Cloud deployment (AWS / Render / GCP)
-   Vector memory for long-term context

# 👨‍💻 Author

**Rajat Paliwal**

GitHub:\
https://github.com/Rajatkpaliwal