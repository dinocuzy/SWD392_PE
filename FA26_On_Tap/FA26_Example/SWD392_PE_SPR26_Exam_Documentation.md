# SWD392 Practice Exam - StayEase System Architecture & UML Models
## 1. Business Overview & Submission Instructions
StayEase is a comprehensive digital platform designed to connect **Property Owners (Hosts)** with **Travelers (Customers)**. The system streamlines the entire process of finding, reserving, and managing short-term accommodations.
### System Actors & Roles
- **Customers:** Can search for available rooms based on location and dates, create reservations, and process payments. They are responsible for paying a deposit to confirm their booking.
- **Hosts:** Responsible for listing their properties, managing room details (amenities, pricing), and performing room inspections upon guest departure.
- **Staff/Administrators:** Oversee the platform's operations, manage user accounts, and generate financial reports.
### Submission Requirements
- **Format:** Submit your answer as a single Word file or a .rar/.zip archive.
- **File Naming:** SWD392_PE_SPR26_[StudentID].docx or SWD392_PE_SPR26_[StudentID].rar
- **Note:** Submissions with incorrect file names may not be graded. Internet access is NOT permitted during the exam. You are allowed to use UML modeling tools in offline mode (Visual Paradigm, Visio, Draw.io).
## 2. Question 1 (3.0 points) – Design-level Class Diagram
**Business Scenario:** You are required to design a design-level Class Diagram for the StayEase homestay booking system. The system is built around a predefined set of classes representing users, rooms, reservations, and payments. Your task is to enrich these classes with appropriate attributes, methods, and relationships to reflect the business logic.
### Class Diagram Requirements
- **Inheritance:** The classes Customer and Host (Property Owner) are specialized types of User and must inherit from it.
- **Multiplicity & Association:** A customer can create multiple reservations, while each reservation is linked to exactly one room.
- **Composition:** A reservation involves one or more payments (such as a 'Deposit' or 'Final Payment'). A payment record cannot exist without a corresponding reservation.
- **Layered Dependency:** Business logic related to room availability and booking is handled by a service class (BookingService). This service class depends on repository interfaces to interact with data.
- **Interface Implementation:** All repository classes (e.g., RoomRepository, ReservationRepository) must implement a generic interface named IGenericRepository.
### Required UML Relationships & Details
- Inheritance (Generalization) and Interface Implementation (Realization).
- Association, Aggregation, and Composition where appropriate.
- Dependency relationships between the Service layer and the Repository layer.
- Multiplicity, attributes, and methods should be defined clearly and reasonably for each class (e.g., status for Rooms, totalAmount for Reservations).
## 3. Question 2 (4.0 points) – Sequence Diagram
**Business Scenario:** A Customer wants to book a homestay room through the StayEase platform. The process starts when the customer interacts with the BookingUI (a boundary object) to submit their booking request (Room ID and stay dates). The request is handled by a BookingController (a control object).
### Process Steps
- **Step 1:** The controller calls a RoomRepository to verify the current status and availability of the selected room for the given dates.
- **Step 2:** If the room is available, the controller proceeds to call a PaymentService to process a mandatory Deposit Payment via an external gateway.
- **Step 3:** Depending on the payment result:
- **If successful:** The controller creates a new Reservation record, saves it using the ReservationRepository, and updates the room's status to "Booked".
- **If failed:** The controller returns an error message to the BookingUI and the process stops.
### Sequence Diagram Requirements
- The diagram must be designed using Layered Architecture.
- **User-facing:** A user-facing component (BookingUI).
- **Controller/Service:** A controller/service component handling business logic (BookingController, BookingService).
- **Repositories:** Repository components responsible for data access (RoomRepository, ReservationRepository).
- **Domain Entities:** Domain entities such as Reservation and Room.
- **Repository Pattern:** Repository Pattern usage must be explicit through repository method calls (e.g., getById, save, updateStatus).
- **Conditional Behavior:** Conditional behavior must be modeled using alt (alternative) fragments for Room availability (Available vs. Occupied) and Payment status (Success vs. Failure).
## 4. Question 3 (3.0 points) – Activity Diagram
### Use Case: Check-out and Inspection
Business Scenario: This workflow describes the process when a Guest checks out of a homestay. The Host (Property Owner) must perform a physical inspection of the room to ensure no damage has occurred.
### Process Steps
- **Step 1:** The Host starts by inspecting the room condition.
- **Step 2:** The Host then enters the inspection results into the StayEase system.
- **Step 3:** The System evaluates the inspection report:
- **If damage is found:** The System calculates an additional Damage Fee and adds it to the Final Invoice.
- **If no damage is found:** The System generates the Final Invoice based only on the remaining stay balance.
- **Step 4:** The Host requests the Guest to settle the payment.
- **Step 5:** After the payment is confirmed, the System updates the Reservation status to "Completed" and changes the Room status to "Cleaning".
### Activity Diagram Requirements
- The diagram must include at least two swimlanes representing Host and System responsibilities.
- Decision nodes must be used to determine whether additional fees (Damage Fees) are applied.
- The workflow must clearly show the update of both Reservation and Room statuses.
- Start and end points of the activity must be clearly indicated using proper UML notation.
- Your diagram must be created at the design level, including Actors/Roles and Components/Services.
