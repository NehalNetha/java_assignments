```markdown
# java_assignments

This repository contains Java assignments. Currently, it includes a student management system.

## Assignment 3: Student Management System

This assignment implements a simple student management system that allows users to add, display, and search for student records.

### Features

*   **Add Student:** Allows users to input student details such as name, PRN, date of birth, and marks.
*   **Display Students:** Displays the details of all students stored in the system.
*   **Search by PRN:** Allows users to search for a student by their PRN (Permanent Registration Number).
*   **Input Validation:** Basic validation to ensure the user inputs an integer between 1 and 4 when selecting the option.

### Files

*   `Assignment3/Main.java`: The main class that contains the program's entry point and handles the user interface.
*   `Assignment3/Student.java`: A class that represents a student, with attributes like name, PRN, date of birth, and marks.
*   `Assignment3/StudentFunction.java`: A class that contains the logic for adding, displaying, and searching for students.

### How to Run

1.  **Clone the repository:**

    ```bash
    git clone https://github.com/NehalNetha/java_assignments.git
    ```

2.  **Navigate to the `Assignment3` directory:**

    ```bash
    cd java_assignments/Assignment3
    ```

3.  **Compile the Java files:**

    ```bash
    javac Main.java Student.java StudentFunction.java
    ```

4.  **Run the `Main` class:**

    ```bash
    java Main
    ```

### Usage

After running the program, you will be presented with a menu:

```
Welcome to the student dashboard
1. Add a Student
2. Display Students
3. Search by PRN
4. Exit
Choose option [1..4]:
```

*   **To add a student:** Enter `1` and follow the prompts to input the student's details.
*   **To display all students:** Enter `2`.
*   **To search for a student by PRN:** Enter `3` and enter the PRN of the student you want to find.
*   **To exit the program:** Enter `4`.

### Code Explanation

#### `Main.java`

This file contains the `main` method, which is the entry point of the program. It presents a menu to the user and calls the appropriate methods from the `StudentFunction` class based on the user's input. It also implements basic error handling for invalid integer inputs when choosing an option.

#### `Student.java`

This file defines the `Student` class, which represents a student. It has the following attributes:

*   `name`: The student's name (String).
*   `prn`: The student's PRN (String).
*   `dob`: The student's date of birth (String).
*   `marks`: The student's marks (int).

It also includes getter methods for each of these attributes.

#### `StudentFunction.java`

This file contains the `StudentFunction` class, which provides the following functionalities:

*   `addStudent()`:  Prompts the user for student details and creates a new `Student` object, which is then added to an `ArrayList` called `students`.  It also trims the input strings to remove leading/trailing whitespace and prints a success message after adding the data.
*   `displayStudents()`: Iterates through the `students` `ArrayList` and prints the details of each student.
*   `searchByPrn()`: Prompts the user for a PRN to search for. It then iterates through the `students` `ArrayList` and checks if any student's PRN matches the search term. If a match is found, the student's details are printed. If no match is found, a "not found" message is displayed.
*   `searchByName()`:  (Currently has a bug - searches using PRN prompt but should search by name). Prompts the user for a name to search for. It then iterates through the `students` `ArrayList` and checks if any student's name matches the search term. If a match is found, the student's details are printed. If no match is found, a "not found" message is displayed.

### Potential Improvements

*   **Input Validation:** Implement more robust input validation to ensure that the user enters valid data (e.g., checking the format of the date of birth, ensuring marks are within a valid range).
*   **Error Handling:** Implement more comprehensive error handling to handle potential exceptions, such as `NumberFormatException` when parsing marks.
*   **Data Persistence:** Implement data persistence to store student records in a file or database so that they are not lost when the program is closed.
*   **Search by Name:** Fix `searchByName()` to actually search for students by name, not PRN.
*   **User Interface:** Improve the user interface to make it more user-friendly.

### Author

Nehal Netha
```