# Practical Exam: SWD392 - Cyber AI FPTx
**Student Management Administration Portal**
**Instructions**
- You work as a software engineer at the "Cyber AI FPTx" company, and your assignment is to keep developing features for the Student Management Administration Portal.
- Accessing the Internet during the exam is NOT permitted.
- UML modeling tools (e.g., Visual Paradigm, Draw.io, or PlantUML) may be used, but only in offline mode.
- Base your work on your knowledge and make realistic assumptions wherever needed.
- Combine your diagrams and written answers into a single document and hand it in following the invigilator's instructions.
- The wording of this exam is intended to be clear and simple.

## Question 1. (3.0 points)
Business Scenario: The system must capture how students, courses, and their grades relate to one another. A Student may enroll in many Courses, and each Course may have many enrolled Students. Whenever a Student finishes a Course, a GradeReport is created. This GradeReport is associated with exactly one Student and one Course, and it holds the final grade (e.g., '5.0', '6.0', '7.0', '8.0'). A GradeReport cannot exist unless both a Student and a Course are present.
Task: Create a Class Diagram that accurately represents this scenario.
- The diagram has to include the classes Student, Course, and GradeReport. Give careful thought to the nature of the relationship between Student and Course.
- GradeReport must be correctly modeled as an Association Class, with its connections and attributes displayed.

## Question 2. (3.0 points)
Business Scenario: A student wishes to sign up for a new course through the portal. The student works with a Course Registration View (boundary object), which forwards the chosen course ID to a RegistrationController (control object). Before proceeding, the controller verifies the student's eligibility (for example, whether the prerequisites have been met) by invoking a PrerequisiteService (service object). If the student is eligible, the controller then creates a new enrollment record using an EnrollmentRepository (entity object).
Task: Pick the most suitable UML diagram (Sequence or Communication) for clearly presenting the step-by-step, time-ordered flow of messages in this registration process, then draw your chosen diagram. Every object must be labeled with its correct application logic stereotype («boundary», «control», etc.).

## Question 3. (2.0 points)
Business Scenario: A student's academic standing (học lực) goes through a lifecycle driven by their GPA. A new student begins in the GoodStanding state. At the end of every semester, the GPA is recomputed. If the GPA drops below a certain threshold (e.g., 5.0), the student's status changes to AcademicWarning. When a student on AcademicWarning still has a GPA below the threshold in the following semester, they move to the Academic Probation state. From either Warning or Probation, a GPA that climbs above the threshold brings the student back to the GoodStanding state. A student on Probation who fails to improve eventually reaches the final state of Dismissed.
Task: Draw a Statechart Diagram for the StudentAcademicStatus object.
- The diagram must show all the states: GoodStanding, Academic Warning, Academic Probation, Dismissed.
- Clearly label the events (e.g., gpaRecalculated) and the guard conditions (e.g., [GPA < 5.0]) that trigger the state changes.

## Question 4. (1.0 point)
Task: The Student Management Portal is a typical web-based application. Its key requirements are a clear separation of concerns, easy maintainability, and the ability for different teams (UI designers, backend developers, database administrators) to work in parallel. The system should also be organized so that new developers can understand it quickly and get onboarded easily.
- Suggest a well-known, appropriate software architecture that best fits a traditional web application with these requirements.
- Name the architecture you select and explain why its structure is a good choice for this project. List one key advantage and one key disadvantage.

## Question 5. (1.0 point)
Business Scenario: Imagine a specific course, "SWD392", which has a limited number of available seats. Many students are interested in this course. When a registered student drops the course, a seat becomes available. The system needs to immediately notify all students who are on the waiting list for this course, so they can try to register for the newly opened spot. The core Course object, which manages the available seats, should not need to know the specific details of which students are on the waiting list or how to contact them. It should simply "announce" that a seat has opened up.
Task: Identify and name a specific Behavioral Design Pattern that allows an object (the Course) to notify a list of dependent objects (the Students on the waiting list) of any state changes, without the Course object needing to know who its dependents are. Explain why this pattern is the best solution for this specific problem.

**END OF EXAMINATION**
*(Invigilators will not provide further explanations)*
