✅ 📘 PROJECT: Student Management System (Java + Swing + MySQL)

This project is a desktop GUI application built using:

Java Swing → for the user interface

JDBC → to connect Java with MySQL

MySQL → database to store student records

The system allows you to add, view, sort, search, and modify student data.

🧱 PROJECT STRUCTURE
✔ src/AppGUI.java

Contains the main GUI (text fields + buttons + event handling)

✔ src/dbConnect.java

Connects Java program to MySQL database.

✔ src/Table.java

Converts database results (ResultSet) into a format for showing in a GUI table.

✔ src/Main.java

Starts the application.

✔ student_data.sql

SQL script to create the students table.

Everything is correct and working together.

🖥️ HOW THE APPLICATION WORKS 

This project creates a window app that interacts with a MySQL database.
The GUI contains:

Student ID

First Name

Last Name

Major

Phone

GPA

Date of Birth

Buttons (Add / Display / Sort / Search / Modify)

The system performs CRUD operations:

✔ Create – Add new student
✔ Read – Display all students
✔ Update – Modify selected student’s data
✔ Delete – (Not included but easy to add)
🧩 1. AppGUI.java — The Interface + Button Actions

This is the heart of the project.

It builds the GUI window using Swing:

Labels (JLabel)

Input boxes (JTextField)

Buttons (JButton)

Events (ActionListener)

Every button has a purpose:

➤ Add Button

Takes the input from text fields and runs:

INSERT INTO sdata VALUES(...)

➤ Display Button

Shows all students:

SELECT * FROM sdata


Result is shown in a JTable popup window.

➤ Sort Button

Sorts by:

First name

Last name

Major

Using SQL:

ORDER BY first_name

➤ Search Button

Searches by:

Student ID

Last Name

Major

The search is dynamic:

SELECT * FROM sdata WHERE major LIKE '%CSE%'

➤ Modify Button

Updates student details using:

UPDATE sdata SET major = 'EEE' WHERE student_id = '001'

🧩 2. dbConnect.java — Database Connection

This file connects Java program to MySQL using:

Class.forName("com.mysql.cj.jdbc.Driver");
Connection conn = DriverManager.getConnection(url, user, pass);


You must set:

String db = "studata"; 
String user = "root";
String pass = "yourpassword";


The program will not run unless DB connection is correct.

🧩 3. Table.java — Converts SQL result to GUI Table

When "Display", "Search", or "Sort" is clicked, SQL returns a ResultSet.

This class converts it to DefaultTableModel so Swing can show it in:

new JTable(model)

🧩 4. Main.java — Application Entry Point

Starts the GUI:

new AppGUI();

🗄️ Database Table (from student_data.sql)

The project uses this table:

Student_ID
first_name
last_name
major
Phone
GPA
DOB


Example data is also provided.

🎯 WHAT THIS PROJECT TEACHES YOU

✔ GUI Programming (Swing)
✔ Event Handling (ActionListener)
✔ Database Connectivity (JDBC)
✔ SQL CRUD operations
✔ Displaying table data using JTable
✔ Building real-world desktop software

🌟 STRENGTHS OF YOUR PROJECT

✓ Fully functional
✓ Good UI
✓ Real MySQL integration
✓ Easy to understand
✓ Perfect for beginners and college submissions

🔧 WHAT CAN BE IMPROVED

Add Delete button

Prevent SQL Injection

Add form validations

Add dropdowns instead of typing major

Display table inside the window (not popup)

Save logs

Add export to PDF/Excel

If you want, I can upgrade the project for you.

🚀 If you want, I can also create:

✔ A full PDF report
✔ A PowerPoint presentation
✔ A mini-project abstract
✔ ER diagram + UML
✔ A more modern version using JavaFX
✔ A web version using Spring Boot + React
