# SWD392 - Software Architecture and Design
# Practical Exam - SUMMER 2025
**Duration: 90 minutes**
*Format: Provide your answers in a Word file and create all diagrams with the Draw.io desktop software. Using ChatGPT, Copilot, or any other AI code generation tools during the exam is prohibited.*
### Problem Statement
A cinema intends to build a comprehensive cinema management system to enhance the movie-going experience and streamline its daily operations.
Through the system, customers can browse movies, check showtimes, and reserve tickets online. They may choose specific seats and view movie details such as genre, duration, rating, and description. The cinema operates several halls, each with its own seating arrangement. Customers are able to review their booking history and receive confirmation emails. Ticket prices are calculated according to seat type (regular, VIP, couple seats) and show timing (matinee, prime time, late night). Staff can manage movie schedules, keep track of seat availability, and handle payments. The system supports online bookings as well as walk-in ticket purchases made at the cinema counter.
Customers receive real-time notifications about seat availability changes, booking confirmations, and showtime updates. Staff dashboards are refreshed live whenever tickets are booked or cancelled.
The system is expected to be developed using a client-server architecture:
- The client will be implemented with React technology.
- The server will be a REST API following the MVC pattern (e.g., ASP.NET Core Web API, Spring Boot Rest API, Rest API with Node.js...).
- The database will be Microsoft SQL Server (MS SQL), MySQL or PostgreSQL.
- Communication between client and server is done via HTTP requests/responses using JSON data format.

## Part 1: Data analysis and design (5 points)
1. LIST the main entities and their key attributes described in the problem. (1 point)
2. DRAW the conceptual ERD for the system. (1 point)
3. DRAW the use case diagram for the cinema management system showing main actors and their interactions. (1.5 points)
4. LIST the main states of the Booking entity during the ticket booking process and DRAW the state diagram for Booking. (1.5 points)
## Part 2: REST API function design (3 points)
1. DRAW a class diagram (detailed design) showing the client-side and server-side classes (Controller, Service, Repository) used for the "create booking" function. (1.5 points)
2. DRAW a sequence diagram for the "create booking" function between client and server (REST API) with authentication and authorization. (1.5 points)
## Part 3: Design pattern identification and analysis (2 points)
Examine the pseudocode below:
```java
public interface Notification {
    public void update(String movieTitle, String showTime, int availableSeat);
}

public class ShowtimeSubject {
    private List<Notification> notifications;
    private String movieTitle;
    private String showTime;
    private int availableSeat;
    public void addNotification(Notification notification) { /*...*/ }
    public void removeNotification(Notification notification) { /*...*/ }
    public void notifyNotifications() {
        for (Notification notification : notifications) {
            notification.update(movieTitle, showTime, availableSeat);
        }
    }
    public void updateShowtime(String title, String time, int seat) {
        this.movieTitle = title;
        this.showTime = time;
        this.availableSeat = seat;
        notifyNotifications();
    }
}

public class CustomerNotification implements Notification {
    public void update(String movieTitle, String showTime, int availableSeat) {
        /* Send notification to customer */
    }
}
```
1. WHAT DESIGN PATTERN does the code above apply? Identify its name and pattern family (creational, structural, or behavioral). (0.5 points)
2. DRAW the class diagram for this pattern. (1 point)
3. DESCRIBE a practical situation in software development where this pattern would be appropriate. (0.5 points)
**Good luck with your exam!**
