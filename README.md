# library-management-system-
Library management system  include all books name and their book id, number of students enrolled in the library with their name and student id, which book with its book id has been taken by which student with their name and student id
# Library Management and Book Circulation Tracking System

A Java console-based project for managing books, students, issue/return transactions, overdue fines, and borrowing history.

## Features

- Add and view books
- Register and view students
- Search books by Book ID
- Check book availability
- Issue and return books
- Automatic 14-day free borrowing period
- Automatic ₹10/day overdue fine
- Borrowing history
- Overdue report
- Most borrowed books report
- Persistent CSV file storage

## Technologies

- Java 17 or later
- VS Code
- Java Collections
- Java File I/O
- java.time API
- Git/GitHub

## Run in VS Code / Terminal

From the project root:

```bash
javac -d out $(find src -name "*.java")
java -cp out library.Main
```

On Windows PowerShell:

```powershell
javac -d out (Get-ChildItem -Recurse src -Filter *.java).FullName
java -cp out library.Main
```

If your Java version supports the VS Code Java Extension Pack, you can also open `src/library/Main.java` and click Run.

## Data

The program automatically creates:

- data/books.csv
- data/students.csv
- data/borrow_history.csv

The first run creates sample books and students.

## Project Structure

- `model` - data classes
- `service` - application/business logic
- `storage` - persistent file storage
- `util` - input validation, date formatting and fine calculation
- `Main.java` - menu and application entry point
