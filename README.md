# **Student Report Card System**  

This project is a **C++ application** that integrates with a **MySQL database** to manage and update student report cards. It allows users to input student scores, calculate averages, assign grades, and update the database accordingly.  

---

## **Features**  
✅ **Database Connectivity**: Uses MySQL to store and retrieve student records.  
✅ **Student Data Management**: Insert student details and update grades based on scores.  
✅ **Automatic Grade Calculation**: Assigns grades according to predefined criteria.  
✅ **User Interaction**: Provides a simple console-based menu for user input.  

---

## **Technologies Used**  
- **C++**  
- **MySQL Database**  
- **MySQL Connector for C++**  
- **Windows API (`windows.h`)** – Used for delays (`Sleep()`)  
- **Standard C++ Libraries** – `iostream`, `sstream`, etc.  

---

## **Setup Instructions**  

### **Prerequisites**  
- Install **MySQL Server** and create a database for storing student records.  
- Install **MySQL Connector/C++** to enable MySQL connectivity.  
- Set up a MySQL table using the following schema:  

```sql
CREATE TABLE Student (
    RollNo VARCHAR(20) PRIMARY KEY,
    Name VARCHAR(50),
    Avg FLOAT DEFAULT 0.0,
    Grade VARCHAR(5) DEFAULT 'NULL'
);
```

---

### **Compilation & Execution**  
1. **Configure MySQL Credentials**:  
   - Update the `HOST`, `USER`, `PW`, and `DB` constants in the C++ file with your database details.  
2. **Compile the Program** (Using g++):  
   ```sh
   g++ student_report.cpp -o student_report -lmysql
   ```
3. **Run the Executable**:  
   ```sh
   ./student_report
   ```

---

## **How It Works**  
1. On startup, the program **connects to the MySQL database**.  
2. Inserts default student records (if not already present).  
3. Provides a **menu-driven interface**:  
   - **Generate Report Card**: Takes user input for student scores, calculates the average, assigns a grade, and updates the database.  
   - **Exit**: Closes the application.  
4. Displays the updated student report from the database.  

---

## **Grading System**  
| **Average Marks** | **Grade** |  
|-------------------|----------|  
| 90 - 100         | A+       |  
| 80 - 89          | A        |  
| 70 - 79          | B+       |  
| 60 - 69          | B        |  
| 50 - 59          | C        |  
| 40 - 49          | D        |  
| Below 40         | F (Fail) |  

---

## **Possible Enhancements**  
- Add a **GUI interface** using Qt or Tkinter.  
- Implement **student search and deletion features**.  
- Store **more subjects and dynamic grading**.
- 
---

## **License**  
This project is open-source and can be modified or distributed freely.  

---
