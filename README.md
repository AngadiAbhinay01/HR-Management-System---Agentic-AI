# 👨‍💼 HR Management System (HRMS)

![Python](https://img.shields.io/badge/Python-3.10+-blue)
![FastMCP](https://img.shields.io/badge/FastMCP-MCP_Server-green)
![MCP](https://img.shields.io/badge/Model_Context_Protocol-AI-orange)
![Email](https://img.shields.io/badge/SMTP-Email-red)
![UV](https://img.shields.io/badge/UV-Package_Manager-purple)

An AI-powered **Human Resource Management System (HRMS)** built using **Model Context Protocol (MCP)** and **FastMCP** that provides intelligent HR services through standardized tools.

The system enables HR teams to efficiently manage employees, meetings, leave requests, support tickets, and automated email notifications through a modular and scalable architecture.

---

# 📌 Project Overview

Managing HR operations manually becomes difficult as organizations grow.

This project provides an intelligent HR Management System that centralizes multiple HR functionalities into a single platform.

The system exposes HR operations as MCP tools, allowing AI assistants and MCP clients to interact with HR services seamlessly.

Core HR services include:

- Employee Management
- Meeting Management
- Leave Management
- Ticket Management
- Email Notification Service

The modular architecture makes it easy to extend with additional HR functionalities in the future.

---

## 🚀 Features

- Employee record management
- Employee search and retrieval
- Meeting scheduling and management
- Leave request creation and tracking
- Support ticket management
- Automated email notifications
- MCP-compliant tool architecture
- FastMCP server implementation
- Modular and scalable codebase
- Environment variable support
- Easy integration with AI assistants

---

## 🎯 Problem Statement

Organizations often manage HR operations across multiple disconnected systems, leading to:

- Manual employee record management
- Inefficient leave approval process
- Difficulty scheduling meetings
- Lack of centralized ticket tracking
- Manual email communication
- Poor scalability

This HRMS solves these problems by exposing HR operations as intelligent MCP tools that can be accessed by AI assistants or compatible MCP clients.

Example:

> User: "Add a new employee named John Doe."

The system:

1. Receives the MCP request
2. Validates employee information
3. Stores employee details
4. Returns confirmation
5. Sends notification (if configured)

---

# 🏗 System Architecture

```text
                    MCP Client
                        │
                        ▼
                FastMCP Server
                        │
        ┌───────────────┼────────────────┐
        ▼               ▼                ▼
 Employee Manager   Meeting Manager   Leave Manager
        │               │                │
        └───────────────┼────────────────┘
                        │
                        ▼
                Ticket Manager
                        │
                        ▼
                 Email Service
                        │
                        ▼
                   SMTP Server
```

---

# 📂 Project Workflow

## Step 1: MCP Client Request

The user interacts with an MCP-compatible client.

Example:

```text
Add a new employee
```

or

```text
Apply leave for Employee ID 102
```

---

## Step 2: FastMCP Tool Invocation

The MCP server receives the request and routes it to the appropriate HR tool.

Examples:

- add_employee()
- get_employee_details()
- schedule_meeting()
- apply_leave()
- create_ticket()
- send_email()

---

## Step 3: Business Logic Processing

Each manager module performs its specific task.

Examples:

Employee Manager

- Add Employee
- Update Employee
- Search Employee
- Delete Employee

Meeting Manager

- Schedule Meeting
- Update Meeting
- Cancel Meeting

Leave Manager

- Apply Leave
- Approve Leave
- Reject Leave
- Leave History

Ticket Manager

- Create Ticket
- Update Ticket
- Resolve Ticket

---

## Step 4: Email Notification

Whenever required, the Email Service sends automated notifications using SMTP.

Examples:

- Leave Approval
- Meeting Invitation
- Employee Registration
- Ticket Updates

---

## Step 5: Response Generation

The server returns a structured response back to the MCP client.

Example:

```text
Employee successfully added.
```

---

# 📊 Core Modules

## 👨 Employee Management

Handles employee-related operations.

### Features

- Add Employee
- Update Employee
- Delete Employee
- Search Employee
- View Employee Details

---

## 📅 Meeting Management

Schedules and manages meetings.

### Features

- Create Meeting
- Update Meeting
- Cancel Meeting
- View Meeting Details

---

## 🏖 Leave Management

Processes employee leave requests.

### Features

- Apply Leave
- Approve Leave
- Reject Leave
- Leave History

---

## 🎫 Ticket Management

Manages employee support requests.

### Features

- Create Ticket
- Assign Ticket
- Resolve Ticket
- Track Ticket Status

---

## 📧 Email Management

Handles automated notifications.

### Features

- SMTP Integration
- Email Templates
- Automated Notifications
- Meeting Invitations
- Leave Updates

---

# 🤖 MCP Components

## FastMCP Server

Responsible for:

- Registering MCP tools
- Handling client requests
- Tool execution
- Standardized communication

---

## HR Managers

Each HR functionality is implemented as an independent manager.

- EmployeeManager
- MeetingManager
- LeaveManager
- TicketManager

This modular design improves maintainability and scalability.

---

## Email Sender

Responsible for:

- SMTP Authentication
- Sending Emails
- Notification Handling

---

# 📂 Project Structure

```text
HR-Management-System/
│
├── hrms/
│   ├── __init__.py
│   ├── employee_manager.py
│   ├── meeting_manager.py
│   ├── leave_manager.py
│   ├── ticket_manager.py
│
├── emails.py
├── utils.py
├── server.py
├── .env
├── pyproject.toml
├── uv.lock
├── requirements.txt
└── README.md
```

---

# ⚙ Setup Instructions

## 1️⃣ Clone Repository

```bash
git clone https://github.com/yourusername/HR-Management-System.git

cd HR-Management-System
```

---

## 2️⃣ Create Virtual Environment

```bash
python -m venv .venv
```

Activate

**Windows**

```bash
.venv\Scripts\activate
```

**Linux / Mac**

```bash
source .venv/bin/activate
```

---

## 3️⃣ Install Dependencies

Using pip

```bash
pip install -r requirements.txt
```

Or using UV

```bash
uv sync
```

---

## 4️⃣ Configure Environment Variables

Create a `.env` file

```env
CB_EMAIL=your_email@gmail.com
CB_EMAIL_PWD=your_email_password
```

---

## 5️⃣ Run the MCP Server

Using Python

```bash
python server.py
```

Or using UV

```bash
uv run server.py
```

---

# 🛠 Tech Stack

## Programming

- Python

### MCP Framework

- Model Context Protocol (MCP)
- FastMCP

### Email Service

- SMTP
- Python smtplib

### Environment Management

- python-dotenv

### Package Management

- UV
- pip

### Development Tools

- VS Code
- Python Virtual Environment

---

# 📈 Example MCP Operations

```text
Add Employee
```

```text
Get Employee Details
```

```text
Schedule Meeting
```

```text
Apply Leave
```

```text
Approve Leave
```

```text
Create Support Ticket
```

```text
Send Email Notification
```

---

# 💡 Key Learnings

- Understanding Model Context Protocol (MCP)
- Building MCP Servers using FastMCP
- Designing modular Python applications
- Implementing HR management workflows
- Tool-based AI integrations
- Environment variable management
- SMTP email automation
- Building scalable backend architectures
- Package management using UV
- Creating AI-compatible service architectures

---

# 🔮 Future Enhancements

- Database integration (SQLite/PostgreSQL)
- Authentication & Authorization
- Employee Dashboard
- HR Analytics Dashboard
- Attendance Management
- Payroll Management
- Performance Evaluation Module
- REST API Integration
- Docker Deployment
- Cloud Deployment (AWS/Azure/GCP)
- Multi-user Role Management
- AI-powered HR Assistant
- Slack/MS Teams Integration

---

# 👨‍💻 Author

**Abhinay Angadi**

📧 Email: [angadiabhinay2001@gmail.com](mailto:angadiabhinay2001@gmail.com)

💼 LinkedIn: https://linkedin.com/in/abhinay-angadi-541004159

💻 GitHub: https://github.com/AngadiAbhinay01

---

# ⭐ If You Found This Project Helpful

If you found this project useful or learned something from it, please consider giving it a ⭐ on GitHub.

Your support motivates future improvements and helps others discover the project.

---

**Built with Python, FastMCP, Model Context Protocol (MCP), SMTP, and UV to create a modular and intelligent Human Resource Management System.** 🚀👨‍💼
