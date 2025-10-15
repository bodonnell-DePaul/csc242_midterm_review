# CSC 242 Midterm Review: Comprehensive GUI Application Project

**Course:** CSC 242: Introduction to Computer Science II  
**Topic:** Integrating Object-Oriented Programming, GUI Development, and Advanced Python Concepts  
**Objective:** Create a Tkinter application that demonstrates all key concepts covered in Assignments 1-4

---

## Learning Objectives
By completing this midterm review project, you will demonstrate mastery of:
- **Object-Oriented Programming**: Classes, inheritance, encapsulation, special methods
- **Scope and Variable Management**: Local, global, and instance variable scoping
- **GUI Programming**: Tkinter event handling, widgets, and user interaction
- **File I/O and Data Processing**: Reading files, error handling, data validation
- **Collections and Data Structures**: Custom container classes and data management
- **Event-Driven Programming**: Button callbacks, user input validation, program flow control

---

## Project Overview: Library Management System GUI

You will create a **Library Management System** with a graphical user interface that allows users to manage books, patrons, and transactions. This system will integrate all the key programming concepts from your assignments while keeping the scope manageable for a midterm project.

### Application Requirements

Your application must demonstrate the following concepts through a working GUI:

1. **Object-Oriented Design** (from HW1 & HW2)
2. **Class Inheritance** (from HW4)
3. **GUI Event Handling** (from HW4)
4. **Scope Management** (from HW1)
5. **File Processing** (from HW2)
6. **Collection Management** (from HW3)

---

## Class Structure Requirements

### 1. Base Classes (Inheritance Demonstration)

#### `Person` (Base Class)
Create a base class that will be inherited by other person-related classes:
- **Attributes**: Name, ID number, contact information
- **Methods**: Basic getters, string representations
- **Purpose**: Demonstrates inheritance foundation

#### `Book` (Independent Class)  
Create a book class similar to your HW1 work:
- **Attributes**: Title, author, ISBN, availability status
- **Methods**: Check out/in functionality, string representations
- **Purpose**: Demonstrates object-oriented design principles

### 2. Derived Classes (Inheritance Implementation)

Create **two derived classes** that inherit from `Person`:
- One class for library patrons
- One class for library staff
- Each should add specialized attributes and methods
- Override at least one method from the base class

### 3. Collection Management Class

Create a class that manages collections of books or patrons:
- Implement custom container behavior
- Include methods for adding, removing, and searching
- Demonstrate proper data structure management

---

## GUI Requirements

### Main Window Structure
Your Tkinter application must include:

#### Essential Widgets:
- **Buttons**: At least 4 different action buttons with event handlers
- **Entry Fields**: For user input (names, IDs, search terms)
- **Labels**: For displaying information and instructions
- **Listbox or Text Widget**: For displaying collections of items
- **(Optional) Menu or Additional Windows**: For advanced functionality

#### Required Functionality:
1. **Add New Items** (books or patrons)
2. **Display Items** 
3. **Perform Transactions** (check out/in books)
4. **File Operations** (save/load data)

### Event Handling Requirements
- Each button must have a properly implemented callback function
- Demonstrate input validation and error handling
- Show appropriate user feedback for all actions
- Handle edge cases gracefully (empty inputs, duplicate entries, etc.)

---

## Scope Demonstration Requirements

Your application must clearly demonstrate different variable scopes:

### Instance Scope  
- Use instance variables in your classes
- Show proper encapsulation with getter/setter methods where appropriate

### Local Scope
- Use local variables within methods
- Demonstrate how local variables don't interfere with instance variables

### Method Parameter Scope
- Pass parameters between methods and functions
- Show how parameter values are passed and used locally

---

## File Processing Requirements

Implement file I/O functionality that demonstrates:
- **Reading from files**: Load initial data (books, patrons, etc.)
- **Writing to files**: Save application state
- **Error handling**: Gracefully handle missing files, corrupted data
- **Data validation**: Ensure file data meets expected formats

### File Format Suggestions:
- CSV format for tabular data
- Text format for simple lists  
- Include sample data files with your submission

### Sample Data Files Provided:
The following CSV files are included to help you test your application:

#### Full Dataset Files:
- **`books.csv`** - 20 books with ISBN, title, author, genre, publication year, and availability
- **`patrons.csv`** - 15 library patrons with ID, contact info, membership date, and status
- **`staff.csv`** - 10 staff members with positions, departments, hire dates, and salaries
- **`transactions.csv`** - 15 sample transactions showing checkouts, returns, and fees
- **`library_settings.csv`** - Configuration settings for your library system

#### Sample/Test Files (Smaller datasets for initial testing):
- **`books_sample.csv`** - 5 books for basic testing
- **`patrons_sample.csv`** - 5 patrons for basic testing

#### CSV File Formats:

**Books Format:**
```
ISBN,Title,Author,Genre,Publication_Year,Available
9780132350884,Clean Code,Robert C. Martin,Programming,2008,True
```

**Patrons Format:**
```
Patron_ID,Name,Email,Phone,Address,Membership_Date,Status
P001,Alice Johnson,alice.johnson@email.com,555-0101,123 Oak Street,2022-01-15,Active
```

**Staff Format:**
```
Staff_ID,Name,Email,Phone,Position,Department,Hire_Date,Salary
S001,Sarah Mitchell,sarah.mitchell@library.org,555-1001,Head Librarian,Administration,2018-03-15,65000
```

**Transactions Format:**
```
Transaction_ID,Patron_ID,ISBN,Transaction_Type,Date,Due_Date,Staff_ID,Notes
T001,P001,9780132350884,Checkout,2024-10-01,2024-10-15,S005,Regular checkout
```

Use these files to test your file I/O functionality, data validation, and error handling capabilities.

---

## Implementation Guidelines

### Getting Started
1. **Plan your class hierarchy** before coding
2. **Design your GUI layout** on paper first  
3. **Start with basic functionality** and add features incrementally
4. **Test each component** as you build it

### Code Organization
- Use separate files for different classes if it helps organization
- Include comprehensive docstrings for all classes and methods
- Use meaningful variable names and follow Python naming conventions
- Comment complex logic and explain design decisions

### Testing Strategy
- Test each class independently before integration
- Verify GUI responds correctly to all user actions
- Test file operations with various file conditions
- Validate that inheritance works as expected

---

## Minimal Starter Code Structure

```python
import tkinter as tk
from tkinter import messagebox, filedialog
import datetime
import random

# Global variable example - document why this is global
LIBRARY_NAME = "CSC 242 Library System"

class Person:
    """Base class demonstrating inheritance foundation"""
    def __init__(self, name, person_id):
        # TODO: Initialize base attributes
        pass
    
    def get_info(self):
        # TODO: Return basic person information
        # This method should be overridden in derived classes
        pass

class LibraryApp(tk.Tk):
    """Main application class - inherits from Tk"""
    def __init__(self):
        super().__init__()
        # TODO: Initialize GUI
        self.setup_gui()
        
    def setup_gui(self):
        # TODO: Create widgets and layout
        pass
    
    def button_click_handler(self):
        # TODO: Example event handler
        # Demonstrate scope by using local, instance, and global variables
        pass

if __name__ == "__main__":
    # TODO: Create and run application
    pass
```

---

### Documentation Requirements:
- Include docstrings for all classes and methods
- Comment areas where you demonstrate specific concepts
- Explain your inheritance hierarchy and why you designed it that way
- Document any global variables and why they need global scope

---

## Tips for Success

1. **Start Early**: This project integrates multiple complex concepts
2. **Plan Your Design**: Spend time designing before coding
3. **Build Incrementally**: Get basic functionality working first
4. **Test Frequently**: Don't wait until the end to test your code
5. **Ask Questions**: If you're unsure about a requirement, ask for clarification
6. **Keep It Simple**: Focus on demonstrating concepts clearly rather than building complex features

Remember: The goal is to demonstrate your understanding of the key concepts, not to build the most feature-rich application possible. A simple, well-designed application that clearly shows all required concepts will score better than a complex application that doesn't properly demonstrate the learning objectives.

---

## Concepts Checklist

Before submitting, verify your application demonstrates:

- [ ] **Base class with inheritance** (at least one base, two derived classes)
- [ ] **Method overriding** in derived classes  
- [ ] **Proper use of self and instance variables**
- [ ] **Global variable with justified usage**
- [ ] **Local variables in methods**
- [ ] **Tkinter GUI with multiple widget types**
- [ ] **Event handlers for button clicks**
- [ ] **File reading with error handling**
- [ ] **File writing functionality**
- [ ] **Collection/container management**
- [ ] **Input validation and user feedback**
- [ ] **Comprehensive docstrings and comments**

Good luck with your midterm project!
