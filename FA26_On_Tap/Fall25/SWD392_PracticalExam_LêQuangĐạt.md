# SWD392 - Software Architecture and Design
# Practical Exam
**Duration: 90 minutes**
*Format: Provide your answers in a Word file, using the Draw.io desktop software for all diagrams. Do not use ChatGPT, Copilot, or any other AI code generation tool during the exam.*
### Problem statement
A company plans to develop an online food ordering system to improve customer convenience and simplify restaurant management.
Users are able to browse menus, view dish details, place orders, and track order status. Restaurants can manage menus and receive orders in real time. The system supports multiple users and restaurants, with each restaurant having many dishes. In addition, each order can contain many dishes, and dishes can appear in many orders.
The system follows a client-server model:
- The client will be built with React technology.
- The server will be a REST API that follows the MVC pattern (e.g., ASP.NET Core Web API, Spring Boot Rest API, Rest API with node.js...).
- For the database, Microsoft SQL Server (MS SQL), MySQL or PostgreSQL can be used.
- Communication between client and server is carried out via HTTP requests/responses using the JSON data format.

## Part 1: Data analysis and design (5 points)
1. LIST the main entities and their key attributes based on the problem description. (1 point)
2. DRAW the conceptual ERD for the system. (1 point)
3. DRAW the logical ERD (with primary/foreign keys and basic data types) using (1.5 points)
4. LIST the main states of the Order entity during the order process and DRAW the state diagram for Dish. (1.5 points)
## Part 2: REST API function design (3 points)
1. DESCRIBE the classes/tables used on the client side, server side (Controller, Service, Repository), and database for the "place order" function. (1 points)
2. DRAW a sequence diagram for the "place order" function between client and server (REST API) including authentication and authorization. (2 points)
## Part 3: Design pattern identification and analysis (2 points)
Given the following pseudocode:
```java
interface Dish {
    String getDescription();
    double getCost();
}

class BasicDish implements Dish {
    public String getDescription() { return "Basic Dish"; }
    public double getCost() { return 5.0; }
}

abstract class DishDecorator implements Dish {
    protected Dish decoratedDish;
    public DishDecorator(Dish dish) { this.decoratedDish = dish; }
    public String getDescription() { return decoratedDish.getDescription(); }
    public double getCost() { return decoratedDish.getCost(); }
}

class CheeseDecorator extends DishDecorator {
    public CheeseDecorator(Dish dish) { super(dish); }
    public String getDescription() { return decoratedDish.getDescription() + ", Cheese"; }
    public double getCost() { return decoratedDish.getCost() + 1.5; }
}

class SauceDecorator extends DishDecorator {
    public SauceDecorator(Dish dish) { super(dish); }
    public String getDescription() { return decoratedDish.getDescription() + ", Sauce"; }
    public double getCost() { return decoratedDish.getCost() + 8.75;
    }
}
```
1. WHAT DESIGN PATTERN is used in the code above? Identify its name and pattern family (creational, structural, or behavioral.) (0.5 points)
2. DRAW the class diagram for this pattern. (1 point)
3. DESCRIBE a practical situation in software development where this pattern would be appropriate. (0.5 points)
**Good luck with your exam!**
