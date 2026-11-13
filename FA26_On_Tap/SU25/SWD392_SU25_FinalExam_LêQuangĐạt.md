**FINAL PRACTICAL EXAM: SWD392-SU25**
**Duration: 85 Minutes**
**Instructions**
- You are working as a software engineer at Cyber AI FPTx. Your job is to build a new Student Management Portal for a university.
- Use your expertise and make realistic assumptions where necessary.
- Produce all diagrams with an offline UML tool (e.g., Visual Paradigm, DrawIO, PlantUML).
- Put your diagrams and written answers into a single MS Word document (.doc or .docx) for submission.
- Internet access is not allowed during the exam.

## Question 1. (3.0 points)
Business Scenario: The system must represent the structure of the university. A University exists as a single entity. The university consists of many Departments (such as "Computer Science" or "Business"). Each department belongs to the university and cannot exist on its own. Every department has many Professors. Some professors are Tenured Professors (permanent staff), while others are Adjunct Professors (part-time).
Task: Create a Class Diagram at the entity level (showing only class names, no attributes).
- The diagram must show the relationships among University, Department, Professor, Tenured Professor, and Adjunct Professor.
- You must correctly depict composition, aggregation, and generalization relationships, including multiplicities.

## Question 2. (3.0 points)
Business Scenario: A student signs into the portal to check their final grade for a course. The student interacts with a GradesView (a boundary object). This view sends a request to a GradesController (a control object). The controller then obtains the grade information from a StudentGradesService (a service object), which in turn reads data from a GradesRecord (an entity object).
Task: Select the most suitable UML diagram (Sequence or Communication) to clearly show the step-by-step, time-ordered flow of messages for this process. Draw the diagram you have selected. You must label each object with its correct application logic stereotype («boundary», «control», etc.).

## Question 3. (2.0 points)
Business Scenario: A student's enrollment in a course follows a lifecycle. Initially, the student is in the Registered state. When the semester begins, their state changes to Active. If the student formally withdraws from the course, their state becomes Dropped. At the end of the semester, after the final grade has been submitted, their state changes to either Passed or Failed.
Task: Draw a Statechart Diagram for a CourseEnrollment object.
- The diagram must show all the states: Registered, Active, Dropped, Passed, Failed.
- Clearly label the events that trigger the state changes (e.g., semester_starts) and the actions that occur (e.g., calculateFinalGrade()).

## Question 4. (1.0 point)
Task: Propose a suitable software architecture for the entire "Student Management Administration Portal."
- State the name of the architecture you choose.
- List two (2) advantages and one (1) disadvantage of your choice for this project.

## Question 5. (1.0 point)
Business Scenario: The portal requires a single, globally accessible object to manage application-wide settings, such as the current academic year and the name of the university. It is critical that this settings object has one and only one instance across the whole system.
Task: Identify and name a specific Design Pattern that guarantees a class has only one instance and provides a global point of access to it.

**END OF EXAMINATION**
*(Invigilators will not provide further explanations)*
