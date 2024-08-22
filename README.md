# README
# Student Management System

This is a simple command-line Student Management System implemented in Python. It allows users to perform basic operations such as adding, deleting, updating, and viewing student information. The code adheres to SOLID principles, eliminates redundancy, and follows best practices like KISS and YAGNI.

## Features

- Add New Student: Add a new student with a unique ID, name, age, and major.
- Delete Student: Remove a student from the database using their ID.
- Update Student Information: Update the name, age, or major of an existing student.
- View All Students: Display all students currently stored in the database.

## Refactoring and Improvements

- SRP (Single Responsibility Principle): Each class now has a single responsibility. The `Student` class is responsible only for holding and displaying student data. The `StudentDatabase` manages student storage and operations, while the `StudentManagementSystem` handles the user interaction and higher-level management.
- OCP (Open/Closed Principle): The system is open for extension but closed for modification. You can easily extend functionalities like searching or filtering students by adding methods to the `StudentDatabase` without altering the core logic.
- DRY (Don't Repeat Yourself): Redundant code has been minimized. For instance, all student updates are now handled through a single method in the `StudentDatabase`.
- KISS (Keep It Simple, Stupid): The design is kept simple and easy to understand, with a clear separation of concerns.
- YAGNI (You Ain't Gonna Need It): Removed unnecessary methods and complexity, focusing only on required features.

## How to Run

1. Clone the Repository:
    ```bash
    git clone https://github.com/yourusername/student-management-system.git
    ```
2. Navigate to the Project Directory:
    ```bash
    cd student-management-system
    ```
3. Run the System:
    ```bash
    python student_management_system.py
    ```
4. Follow the Menu Prompts: The system will display a menu with options to add, delete, update, or view students. Simply enter the corresponding number to perform the desired operation.

## Example Usage

Upon running the system, you will see a menu like this:

Student Management System
1. Add New Student
2. Delete Student
3. Update Student Information
4. View All Students
5. Exit
```

Choose an option by entering the number and following the prompts to manage student records.

## License

This project is licensed under the MIT License. See the LICENSE file for details.

This documentation should provide clear guidance on how to use and understand the refactored code.
