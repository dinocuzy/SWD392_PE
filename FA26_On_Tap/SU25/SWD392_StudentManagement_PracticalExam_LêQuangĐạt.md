# SWD392 - Software Architecture and Design
# Practical Exam
**Duration: 90 minutes**
*Format: Provide your answers in a Word file using Draw.io desktop software for all diagrams. ChatGPT, Copilot, and any other AI code generation tools are not allowed during the exam.*
### Problem statement
To modernize student management operations and improve the user experience, the university plans to develop a new student management system.
Users can search for subjects, classes, and students, and view student details such as personal information, subject registrations, attended classes, and grades. The system tracks the class attendance of each student and manages multiple subjects, classes, and students; a student passes a subject when their grade is greater than or equal to 5 points. Notifications are sent to users when they miss a class or fail a subject.
The system is planned to be developed using a client-server architecture:
- The client will be implemented with React technology.
- The server will be a REST API following the MVC pattern (e.g., ASP.NET Core Web API, Spring Boot Rest API, Rest API with node.js...).
- The database will be Microsoft SQL Server (MS SQL), MySQL or PostgreSQL.
- Communication between client and server is done via HTTP requests/responses using JSON data format.

## Part 1: Data analysis and design (5 points)
1. Based on the problem description, LIST the main entities and their key attributes. (1 point)
2. DRAW the conceptual ERD for the system. (1 point)
3. DRAW the logical ERD (with primary/foreign keys and basic data types) using (1.5 points)
4. LIST the main states of the Student entity while studying a subject, and DRAW the state diagram for that studying process. (1.5 points)
## Part 2: REST API function design (3 points)
1. For the "register subject" function, DESCRIBE the classes/tables used on the client side, server side (MVC: Controller, Service, Repository), and in the database. (1 points)
2. DRAW a sequence diagram for the "register subject" function between client and server (REST API) with authentication and authorization. (2 points)
## Part 3: Design Pattern Identification and Analysis (2 points)
Read the explanation of a design pattern:
Here is how it works: imagine that you created an object, but later decided to create a new one. Instead of receiving a fresh object, you get the one you already created.
Questions:
1. What design pattern is used in the code above? Identify its name and its pattern family (creational, structural, or behavioral). (0.5 points)
2. Write the pseudo code for this pattern. (1 point)
3. Describe a practical situation in software development where this pattern would be appropriate. (0.5 points)
**Good luck with your exam!**
