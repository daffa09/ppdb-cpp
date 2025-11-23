<!-- portfolio -->
<!-- slug: ppdb-cpp -->
<!-- title: PPDB C++ -->
<!-- description: Simple student admission system (PPDB) built with C++ using in-memory data storage -->
<!-- image: https://github.com/user-attachments/assets/75c4e8d6-9cc1-4d53-8761-cead8603805e -->
<!-- tags: c++, console-app, admission-system, learning-project -->

# PPDB C++ - Student Admission System

<img width="1536" height="1024" alt="ppdb-cpp" src="https://github.com/user-attachments/assets/75c4e8d6-9cc1-4d53-8761-cead8603805e" />

A simple student admission system (PPDB - Penerimaan Peserta Didik Baru) built with C++. This console-based application manages new student registrations using in-memory data storage, demonstrating fundamental C++ programming concepts.

## 📋 Overview

This PPDB (New Student Admission) application is a console-based system that handles student registration processes. Built without database integration, it uses in-memory data structures to store information within a single session, making it an excellent learning project for C++ fundamentals.

## ✨ Features

- **Student Registration**: Register new students with complete information
- **View Registrations**: Display all registered students
- **In-memory Storage**: Data stored during program runtime
- **Admin Access**: Special admin menu (accessible with code 13)
- **Session-based**: All data available within one program session

### Admin Features

Access admin panel by entering number **13** in main menu:
- **Username**: `admin`
- **Password**: `admin`

Admin capabilities:
- View all registrations
- Manage system settings
- Access special functions

## 🛠️ Technologies Used

- **C++**: Core programming language
- **STL**: Standard Template Library (vectors, strings)
- **Console I/O**: For user interaction

## 📁 Project Structure

```
ppdb-cpp/
├── src/
│   └── main.cpp          # Main application file
├── bin/
│   └── ppdb.exe         # Compiled executable
├── .vscode/             # VS Code configuration
├── .gitignore
└── README.md
```

## 🚀 Getting Started

### Prerequisites

- C++ compiler (GCC, Clang, or MSVC)
- Command line interface

### Compilation

**Using GCC:**
```bash
g++ -o ppdb src/main.cpp
```

**Using Clang:**
```bash
clang++ -o ppdb src/main.cpp
```

**Using Visual Studio:**
1. Open project in Visual Studio
2. Build → Build Solution
3. Executable in Debug/Release folder

### Running the Application

**Linux/macOS:**
```bash
./ppdb
```

**Windows:**
```bash
ppdb.exe
```

Or double-click the executable

## 💻 Usage Guide

### Main Menu

Upon starting, you'll see the main menu with options:
1. Register New Student
2. View All Registrations
3. Exit
13. Admin Panel (hidden option)

### Registering Students

1. Select option 1
2. Enter student information:
   - Full Name
   - Date of Birth
   - Address
   - Parent/Guardian Name
   - Phone Number
   - Previous School
   - Desired Class/Program
3. Data saved to memory
4. Return to main menu

### Viewing Registrations

1. Select option 2
2. See list of all registered students
3. Information displayed in  formatted table
4. Return to main menu

### Admin Access

1. Enter **13** from main menu
2. Login with credentials:
   - Username: `admin`
   - Password: `admin`
3. Access admin features:
   - View detailed statistics
   - Export data (if implemented)
   - System management

## 📊 Data Structure

Student information stored in memory:

```cpp
struct Student {
    string name;
    string dateOfBirth;
    string address;
    string parentName;
    string phoneNumber;
    string previousSchool;
    string desiredClass;
    int registrationNumber;
};
```

## 🎓 Learning Concepts

This project demonstrates:
- **Struct/Class Usage**: Data organization
- **Vector Container**: Dynamic arrays
- **Console I/O**: User interaction
- **Control Structures**: Loops and conditionals
- **Functions**: Code organization
- **String Manipulation**: Text processing
- **In-memory Storage**: Data management within session

## ⚠️ Important Notes

### Data Persistence

**Note**: This application does **NOT** use a database. All data is stored in memory during program execution:

- Data exists only while program is running
- When you exit, all data is lost
- Each run starts with empty data
- No file saving implemented

This is intentional for learning purposes, focusing on C++ fundamentals without database complexity.

## 🔧 Code Example

Basic structure:
```cpp
#include <iostream>
#include <vector>
#include <string>

using namespace std;

struct Student {
    string name;
    int regNumber;
    // ... other fields
};

vector<Student> students; // In-memory storage

void addStudent() {
    Student newStudent;
    // Get input from user
    students.push_back(newStudent);
}

void viewStudents() {
    for(const auto& student : students) {
        cout << student.name << endl;
    }
}

int main() {
    int choice;
    while(true) {
        // Display menu
        cin >> choice;
        
        switch(choice) {
            case 1: addStudent(); break;
            case 2: viewStudents(); break;
            case 13: adminPanel(); break;
            case 3: return 0;
        }
    }
}
```

## 🐛 Troubleshooting

**Program Crashes on Input**
- Check input validation
-Ensure correct data types

**Admin Panel Not Accessible**
- Enter exactly **13** (not "admin" or other)
- Follow with correct credentials

**Data Disappears**
- This is normal - data is session-based
- All data clears when program exits

## 🚀 Future Enhancements

To make this production-ready:
- File-based storage (text/CSV files)
- Database integration (SQLite, MySQL)
- Data validation and error handling
- Search and filter capabilities
- Edit/delete student records
- Print registration forms
- Backup and restore
- User authentication system
- GUI interface (Qt, wxWidgets)

## 🎯 Use Cases

- Learning C++ fundamentals
- Understanding data structures
- Practicing console applications
- Teaching programming basics
- Simple registration systems

## 🤝 Contributing

This is a learning project. Feel free to fork and enhance with:
- File I/O for persistence
- Better UI/UX
- Additional features
- Database integration

## 📄 License

Open source and available for educational purposes.

## 💭 Personal Note

This is a simple PPDB application that doesn't use a database. All data is stored in-memory within a single session. It was great practice for learning C++ fundamentals without the complexity of database integration!

---

**Built for Learning C++** 🎓📝  
Simple student admission system with in-memory storage
