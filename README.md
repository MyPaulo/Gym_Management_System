# Gym Management System

A comprehensive Java-based command-line application for managing gym operations, including member registration, staff management, fitness classes, and equipment inventory.

## Demo
![Application Demo_output](Gym_demo.svg)


## Features

### 🏋️ Member Management
- Register new members with unique IDs
- Update member information (contact, email, membership type)
- View member lists
- Remove members from the system
- Support for Standard and Premium membership types

### 👥 Staff Management
- Staff authentication and login system
- Add new staff members
- Update staff information
- Remove staff members
- Role-based access control

### 🏃 Fitness Classes
- Schedule new fitness classes
- Update existing class details
- Search classes by various criteria
- Cancel classes
- View available classes

### 🏋️‍♂️ Equipment Management
- Add new equipment to inventory
- Update equipment information
- Search equipment by name or description
- Delete equipment from inventory
- View complete equipment inventory

### 📊 Reporting System
- Generate membership reports
- Class attendance reports
- Equipment inventory reports
- Export reports to files

### 💾 Data Persistence
- Auto-save functionality
- Manual save/load operations
- Serialization support for data persistence

## System Requirements
- Java 8 or higher
- Command-line interface
- Minimum 512MB RAM
- 50MB free disk space

## Installation & Setup

1. **Clone the repository:**
   ```bash
   git clone https://github.com/username/gym-management-system.git
   cd gym-management-system
   ```

2. **Compile the Java files:**
   ```bash
   javac *.java
   ```

3. **Run the application:**
   ```bash
   java Main
   ```

## Usage

### First Time Setup
The system comes with a default admin account:
- **Staff ID:** STF0000
- **Password:** admin
- **Role:** SysAdmin

### Main Menu Options

1. **Login** - Authenticate as a staff member
2. **Manage Staff** - Add, update, or remove staff (requires login)
3. **Register New Member** - Add new gym members (requires login)
4. **Update Member Information** - Modify existing member details (requires login)
5. **Display Member List** - View all registered members
6. **Remove Member** - Delete member from system (requires login)
7. **Manage Fitness Classes** - Schedule, update, or cancel classes (requires login)
8. **Display Available Classes** - View all scheduled classes
9. **Manage Equipment** - Add, update, or remove equipment (requires login)
10. **View Equipment Inventory** - Display all equipment
11. **Generate Reports** - Create various system reports (requires login)
12. **Logout** - End current session
0. **Exit** - Close the application

### Input Validation

The system includes comprehensive input validation:
- **Names:** Only alphabetic characters and spaces
- **Phone Numbers:** Must be 10 digits
- **Email:** Must follow standard email format
- **Time Format:** HH:MM AM/PM format
- **Membership Types:** Standard or Premium only

### Data Storage
- All data is automatically saved to serialized files
- Auto-save can be toggled on/off
- Manual save operations occur after major changes
- Data is loaded automatically on startup

## Class Structure

### Core Classes

- **`Main.java`** - Entry point and application launcher
- **`GymInterface.java`** - Command-line interface handler
- **`GymManagementSystem.java`** - Backend operations 
- **`Member.java`** - Member entity with unique ID generation
- **`Staff.java`** - Staff entity with authentication support
- **`User.java`** - Base class for Member and Staff 
- **`FitnessClass.java`** - Fitness class entity 
- **`Equipment.java`** - Equipment entity

### Exception Classes
- **`InvalidUserException`** - Custom exception for user-related errors
- **`InvalidClassException`** - Custom exception for class-related errors

## Key Features

### Authentication System
- Secure login with staff ID and password
- Session management
- Role-based access control

### ID Generation
- **Members:** MEM0001, MEM0002, etc.
- **Staff:** STF0001, STF0002, etc.
- Thread-safe unique ID generation

### Input Validation
- Regex-based validation for all inputs
- Error handling with user-friendly messages
- Retry mechanisms for invalid inputs

### Search Functionality
- Search classes by ID, name, instructor, or capacity
- Search equipment by name or description
- Case-insensitive search options

## Error Handling

The system includes comprehensive error handling:
- Input validation with clear error messages
- Exception handling for all operations
- Graceful handling of invalid user inputs
- Safe data persistence operations


## Future Enhancements

- GUI interface using JavaFX or Swing
- Database integration (MySQL/PostgreSQL)
- Member check-in/check-out system
- Advanced reporting with charts

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Support
For support or questions, please create an issue in the GitHub repository.

---

## Acknowledgment
👥 Group Members & Their Contributions
This project was developed as part of a group effort for our coursework(Comp 2120). Special thanks to my teammates

Paul Osuji
Designed and implemented the command-line interface (CLI)
Developed core logic for managing Members, Staff, Equipment, and Fitness Classes
Implemented security features including login/logout and role-based access
Created the abstract User class and object templates for all major entities
Led overall system architecture, testing, and integration

Inan Syed
Assisted with I/O programming and data persistence logic
Contributed to the autosave feature using multithreading
Participated in report generation logic and code reviews

Temirlan Rashid
Contributed to custom exception handling and input validation
Assisted with ID generation logic and regex-based validation
Participated in testing, debugging, and code reviews


**Note:** This is a console-based application designed for educational purposes and small gym operations.