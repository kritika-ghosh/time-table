# Task Management Application

A simple yet efficient **Task Manager** built using **Java Swing** for the GUI and **MySQL** for persistent data storage. This application allows users to add, update, delete, and view tasks, making task organization seamless.

---

## Features

- **Add New Tasks:** Input task name, description, due date, and priority.
- **View Tasks:** Display all tasks in a table format.
- **Update Tasks:** Edit existing task details.
- **Delete Tasks:** Remove tasks from the list.
- **Persistent Storage:** All data is stored in a MySQL database.
- **User-Friendly GUI:** Clean and interactive interface built using Java Swing.

---

## Technologies Used

- **Java SE**
- **Java Swing** (GUI Framework)
- **JDBC (Java Database Connectivity)**
- **MySQL Database**

---

## Prerequisites:

- **Java JDK 8+**
- **MySQL Server**
- **MySQL JDBC Driver** (Connector/J)

---

## Steps:

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/task-manager-java.git
cd task-manager-java
```

### 2. Database Setup

- Open MySQL Workbench or any MySQL client.
- Run the following SQL script to create the database and table:

```sql
CREATE DATABASE task_manager;

USE task_manager;

CREATE TABLE tasks (
    id INT AUTO_INCREMENT PRIMARY KEY,
    title VARCHAR(100) NOT NULL,
    description TEXT,
    due_date DATE,
    priority VARCHAR(20)
);
```

### 3. Configure Database Connection

- In your Java project, locate the database connection file (`DBConnection.java` or similar).
- Update the following credentials:

```java
String url = "jdbc:mysql://localhost:3306/task_manager";
String user = "your_mysql_username";
String password = "your_mysql_password";
```

### 4. Add MySQL JDBC Driver

- Download the MySQL JDBC driver (Connector/J) `.jar` file.
- Add the `.jar` file to your project's classpath.

### 5. Compile and Run the Application

#### Open Terminal in VS Code (or preferred terminal)

#### Compile the Java File

```bash
javac -cp ".;path/to/mysql-connector-java-x.x.x.jar" path/to/YourMainClass.java
```

#### Run the Java Application

```bash
java -cp ".;path/to/mysql-connector-java-x.x.x.jar;path/to" YourMainClass
```

> Replace `path/to/` and `YourMainClass` with the actual paths and class name in your project.

- The GUI window should now appear, allowing you to manage your tasks.

---

## Future Enhancements

- Add search and filter functionality.
- Implement task categories or tags.
- Add deadline reminders/notifications.
- Export tasks to CSV or PDF.
- User authentication and multiple user support.

---
