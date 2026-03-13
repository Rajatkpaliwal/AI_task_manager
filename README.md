🤖 AI Task Manager

An AI-powered task management assistant built using LangChain, Groq LLM, SQLite, and Streamlit.
The application allows users to create, read, update, and delete tasks using natural language.

Instead of manually writing SQL queries, users can simply chat with the AI and it will manage the tasks stored in the database.

🚀 Features
🧠 AI-powered Task Management

Users interact with the system using natural language such as:

Add a task to complete my assignment
Show my pending tasks
Mark task 3 as completed
Delete the task "buy groceries"

The AI agent automatically converts these instructions into SQL operations.

📋 CRUD Operations Supported
Operation	Example Prompt
Create Task	"Add a task to finish my project"
View Tasks	"Show my tasks"
Update Task	"Mark task 2 as completed"
Delete Task	"Delete task 5"
🗄️ Database Integration

The project uses SQLite to store tasks.

Table Schema:

Column	Type	Description
id	INTEGER	Primary Key
title	TEXT	Task title
description	TEXT	Task details
status	TEXT	pending / in_progress / completed
created_at	TIMESTAMP	Task creation time
🧩 Tech Stack
Technology	Purpose
Python	Core language
Streamlit	Web UI
LangChain	AI Agent framework
Groq LLM	Large language model
SQLite	Database
LangGraph	Agent memory handling
🏗️ Project Structure
AI_task_manager
│
├── main.py                # Main application
├── my_tasks.db            # SQLite database
├── requirements.txt       # Python dependencies
├── pyproject.toml         # Python project configuration
├── uv.lock                # Dependency lock file
├── README.md              # Project documentation
├── how_to_run.txt         # Running instructions
└── .gitignore             # Ignored files
⚙️ Installation
1️⃣ Clone the Repository
git clone https://github.com/Rajatkpaliwal/AI_task_manager.git
cd AI_task_manager
2️⃣ Create Virtual Environment
python -m venv venv

Activate it:

Windows

venv\Scripts\activate

Mac/Linux

source venv/bin/activate
3️⃣ Install Dependencies
pip install -r requirements.txt
4️⃣ Setup Environment Variables

Create a .env file in the root directory.

Example:

GROQ_API_KEY=your_api_key_here
▶️ Running the Application

Start the Streamlit app:

streamlit run main.py

Then open your browser at:

http://localhost:8501
💬 Example Commands

You can interact with the assistant like this:

Create Tasks
Add a task to complete my AI project
View Tasks
Show my tasks
Update Tasks
Mark task 1 as completed
Delete Tasks
Delete task 3
🧠 How It Works
Step 1 — User Input

User sends a natural language instruction.

Example:

Add a task to buy groceries
Step 2 — AI Agent Processing

The LangChain agent:

Understands user intent

Converts the request into SQL

Executes the query on SQLite

Returns structured results

Step 3 — Database Execution

Example SQL generated:

INSERT INTO tasks(title, description, status)
VALUES ('buy groceries', '', 'pending');
Step 4 — Result Display

The assistant confirms the operation and displays the updated task list.

🧠 AI Agent Configuration

The agent uses:

Groq LLM

SQLDatabaseToolkit

LangGraph memory

System prompt rules

The system prompt defines:

Query limits

CRUD behavior

Table schema awareness

This ensures safe and structured database interactions.

🔐 Safety Rules Implemented

The agent follows these constraints:

Maximum 10 rows returned per query

Every write operation must be verified using a SELECT

Structured table output for UI display

📌 Future Improvements

Possible enhancements:

✅ Task reminders

✅ Multi-user login system

✅ Task priority levels

✅ Due dates

✅ Task categories

✅ Deploy on cloud (AWS / GCP / Render)

✅ Vector memory for task history

📄 License

This project is open-source and available under the MIT License.

👨‍💻 Author

Rajat Paliwal

GitHub
https://github.com/Rajatkpaliwal