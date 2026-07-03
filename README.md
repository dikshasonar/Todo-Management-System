# Todo-Management-System
A JavaFX-based Todo Management System with user authentication, task management, MySQL database integration, and email notification support.

# 🚀 Installation and Setup Guide

Follow these steps to download and run the project on your local machine.

---

## Step 1: Clone the Repository

Open **Git Bash** or **Command Prompt** and run:

```bash
git clone https://github.com/your-username/todo-management-system.git
```

Or download the project manually:

1. Open the GitHub repository.
2. Click the **Code** button.
3. Select **Download ZIP**.
4. Extract the ZIP file to your desired location.

---

## Step 2: Install Required Software

Make sure the following software is installed on your computer.

| Software | Version |
|----------|---------|
| Java JDK | 17 or later |
| JavaFX SDK | 17 or later |
| MySQL Server | 8.0 or later |
| Eclipse IDE (Recommended) | Latest Version |

---

## Step 3: Download Required Libraries

### 1. JavaFX SDK

Download the JavaFX SDK from:

https://gluonhq.com/products/javafx/

Extract the downloaded ZIP file.

Example:

```
C:\javafx-sdk-21\
```

---

### 2. MySQL Connector/J

Download from:

https://dev.mysql.com/downloads/connector/j/

Add the following JAR file to your project:

```
mysql-connector-j-x.x.x.jar
```

---

### 3. Jakarta Mail API

Download from:

https://eclipse-ee4j.github.io/angus-mail/

Add these JAR files:

```
jakarta.mail.jar
jakarta.activation.jar
```

---

## Step 4: Open the Project

### In Eclipse

1. Open Eclipse.
2. Click **File → Import**.
3. Select **Existing Projects into Workspace**.
4. Click **Next**.
5. Browse to the extracted project folder.
6. Click **Finish**.

---

## Step 5: Add External Libraries

Right-click the project.

```
Build Path
    ↓
Configure Build Path
    ↓
Libraries
    ↓
Add External JARs
```

Add:

- JavaFX SDK libraries
- MySQL Connector/J
- Jakarta Mail JARs

Click **Apply and Close**.

---

## Step 6: Configure JavaFX

Right-click the project.

```
Run As
    ↓
Run Configurations
```

Under **Arguments**, add the following VM arguments:

```text
--module-path "C:\javafx-sdk-21\lib" --add-modules javafx.controls,javafx.fxml
```

Replace the path with the location of your JavaFX SDK.

---

## Step 7: Configure MySQL Database

1. Install MySQL Server.
2. Create a new database:

```sql
CREATE DATABASE todo_db;
```

3. Create the required tables (`users` and `tasks`).

4. Open `DBHelper.java` and update:

```java
String url = "jdbc:mysql://localhost:3306/todo_db";
String username = "root";
String password = "your_password";
```

---

## Step 8: Configure Email Settings

Open:

```
EmailSender.java
```

Update:

- Gmail address
- App Password
- SMTP Host
- SMTP Port

Example:

```text
Email : your_email@gmail.com
Password : Gmail App Password
SMTP Host : smtp.gmail.com
Port : 587
```

> **Note:** Use a Gmail App Password instead of your regular Gmail password.

---

## Step 9: Run the Project

Open:

```
src
└── com
    └── info
        └── tod
            └── TodoApp.java
```

Right-click **TodoApp.java**.

Select:

```
Run As
    ↓
Java Application
```

---

# 📂 Project Hierarchy

```
todo-management-system/
│
├── src/
│   └── com/
│       └── info/
│           └── tod/
│               ├── TodoApp.java
│               ├── LoginPage.java
│               ├── DBHelper.java
│               ├── Task.java
│               ├── User.java
│               └── EmailSender.java
│
├── lib/
│   ├── mysql-connector-j.jar
│   ├── jakarta.mail.jar
│   └── javafx-sdk/
│
├── README.md
└── .gitignore
```

---

# 📁 Project Workflow

```
Application Starts
        │
        ▼
 Login Page
        │
        ▼
Authentication
        │
        ▼
 Dashboard
        │
 ┌──────┼────────┐
 │      │        │
 ▼      ▼        ▼
Add   Update   Delete
Task   Task     Task
 │
 ▼
Save to MySQL
 │
 ▼
Display Updated Tasks
 │
 ▼
Email Notification (Optional)
```


# 🛠 Technologies Used

| Technology | Purpose |
|------------|---------|
| Java | Programming Language |
| JavaFX | GUI Development |
| JDBC | Database Connectivity |
| MySQL | Database |
| Eclipse IDE | Development Environment |
| JavaMail API | Email Sending |

---



---
