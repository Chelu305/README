# README
# Student Management System
class Student:
    def __init__(self, student_id, name, age, major):
    
     # Initialize a Student with an ID, name, age, and major
self.student_id = student_id
        self.name = name
        self.age = age
        self.major = major

  def display(self):
  
        # Display the student's information
 print(f"ID: {self.student_id}, Name: {self.name}, Age: {self.age}, Major: {self.major}")


class StudentDatabase:
    def __init__(self):
    
        # Initialize the StudentDatabase as a dictionary for easy look-up by student_id
        
  self.students = {}
def add_student(self, student):
    
        # Add a new student to the database
self.students[student.student_id] = student
def remove_student(self, student_id):

        # Remove a student from the database using student_id
        
if student_id in self.students:
            del self.students[student_id]

def update_student(self, student_id, name=None, age=None, major=None):

        # Update a student's information based on provided parameters
student = self.students.get(student_id)
        if student:
            if name:
                student.name = name
            if age:
                student.age = age
            if major:
                student.major = major

def find_student(self, student_id):

        # Find and return a student by their ID
        return
self.students.get(student_id)

 def display_all_students(self):
 
        # Display all students in the database
if not self.students:
            print("No students in the database.")
        for student in self.students.values():
            student.display()


class StudentManagementSystem:
    def __init__(self):
    
        # Initialize the management system with an empty student database
self.database = StudentDatabase()

def add_new_student(self, student_id, name, age, major):

        # Add a new student after checking if the student ID is unique
if student_id in self.database.students:
            print("Student with this ID already exists.")
            return
        student = Student(student_id, name, age, major)
        self.database.add_student(student)

def delete_student(self, student_id):

        # Delete a student from the database
 if student_id not in self.database.students:
            print("Student not found.")
            return
        self.database.remove_student(student_id)

def update_student_info(self, student_id, name=None, age=None, major=None):

        # Update a student's information in the database
if student_id not in self.database.students:
         print("Student not found.")
            return
        self.database.update_student(student_id, name, age, major)

def show_all_students(self):

        # Display all students in the database
 self.database.display_all_students()

def run(self):

        # Menu system for interacting with the StudentManagementSystem
while True:
print("\n--- Student Management System ---")
print("1. Add New Student")
print("2. Delete Student")
print("3. Update Student Information")
print("4. View All Students") print("5. Exit")

choice = input("Enter your choice: ")

   if choice == "1":
                student_id = input("Enter Student ID: ")
    name = input("Enter Name: ")
    age = int(input("Enter Age: "))
    major = input("Enter Major: ")
                self.add_new_student(student_id, name, age, major)

 elif choice == "2":
student_id = input("Enter Student ID to Delete: ")
                self.delete_student(student_id)
elif choice == "3":
student_id = input("Enter Student ID to Update: ")
name = input("Enter New Name (leave blank to keep current): ")
age = input("Enter New Age (leave blank to keep current): ")
major = input("Enter New Major (leave blank to keep current): ")
age = int(age) if age else None
                self.update_student_info(student_id, name=name, age=age, major=major)
elif choice == "4":
                self.show_all_students()
elif choice == "5":
print("Exiting the system.")
break
else:
print("Invalid choice. Please try again.")


# Example Usage
system = StudentManagementSystem()
system.run()


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
    git clone https://github.com/chelu305/student-management-system.git
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
