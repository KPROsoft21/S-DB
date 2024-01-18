# Student Management System 
A python based software which helpful to maintain students records very efficiently. 
Used CRUD operations to implement all the database operations.

ASSIGNMENT BY:-

&#10004; KIBUR E,
&#10004; KIRUBEL D,
&#10004; MOHAMMED S,

## Features
1) Adding students names
2) Deleting students names
3) Updating student details

## Installation 
1. Clone the repository 
```
https://github.com/KPROsoft21/Student-Management-System.git
```
2. Check the status of your file 
```
$git status
```

3.For using VScode for editing your files 
```
$git code .
```
4. To directly add your files to github
```
$git add .
```
5. After writing your code commit your changes 
```
$git commit -m  <message>
```
6. To pull your code to reposoitory
```
$git push origin master
```
Thats all about installation and version control with **Git**


----------------------------------------------------------------




## DATABASE creation
1. Create Database
```
CREATE DATABASE SDBS
```

2. Create Tables 
```
CREATE TABLE students (
    Roll_No INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(255),
    name VARCHAR(255),    
    student_age INT,
    -- Add more fields as needed
);
```

same for Teachers table

3. Connect To DB
```
import pymysql

# Establish a connection to the MySQL server
con = pymysql.connect(host="localhost", user="root", password="root", database="SDB")

# Now you can proceed with your code
```
4. To Relate Fields
```
SELECT *
FROM students
JOIN teachers ON students.dept = teachers.dept;
```


## Contributors ❤
- [Kibur](https://github.com/KPROsoft21). 

# ERD

+-------------+         +-------------+         +-------------+
|   Student   |         |   Teacher   |         |    Class    |
+-------------+         +-------------+         +-------------+
| Roll_No     |         | Roll_No     |         | Class_ID    |
| Name        |         | Name        |         | Class_Name  |
| Dept        |         | Dept        |         | Grade_Level |
| Email       |         | Email       |         +-------------+
| Gender      |         | Gender      |        /           \
| Contact     |         | Contact     |       /             \
+-------------+         +-------------+      /               \
       |                 |                 /                 \
       |                 |                /                   \
       |                 |               /                     \
       |                 |              /                       \
       |       +------------------------+                         \
       +-------|      Enrollment       |                           \
               +------------------------+                             \
               | Enrollment_ID         |                               \
               | Student_ID (FK)       |                                \
               | Class_ID (FK)         |                                 \
               | Enrollment_Date       |                                  \
               +------------------------+                                   \
                           |                                              \
                           |                                               \
                           |                                                \
               +------------------------+                                  \
               |   Teaching Assignment  |                                    \
               +------------------------+                                      \
               | Assignment_ID          |                                        \
               | Teacher_ID (FK)        |                                         \
               | Class_ID (FK)          |                                          \
               +------------------------+                                            \
                           |                                                    \
                           |                                                     \
                           |                                                      \
               +------------------------+                                        \
               | Subject Assignment     |                                          \
               +------------------------+                                            \
               | Assignment_ID          |                                              \
               | Teacher_ID (FK)        |                                               \
               | Subject_ID (FK)        |                                                \
               +------------------------+                                                 \
