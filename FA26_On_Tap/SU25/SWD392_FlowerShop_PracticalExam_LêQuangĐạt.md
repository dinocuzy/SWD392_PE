# SWD392 - Software Architecture and Design
# Practical Exam
**Duration: 90 minutes**
*Format: Answers are to be submitted in a Word document, using Draw.io desktop software for all diagrams. ChatGPT, Copilot, or any other AI code generation tools must not be used during the exam.*
### Problem statement
To improve the flower shopping experience and streamline operations, a flower shop intends to build a comprehensive flower shop management system. Through this system, customers can browse flowers, view available arrangements, and place online orders for bouquets. Users are able to pick specific flowers, personalize arrangements, and view flower details such as type, color, seasonal availability, care instructions, and pricing.
The shop offers several flower categories, including fresh flowers, artificial flowers, and seasonal arrangements. Customers can review their past orders and receive confirmation emails. Pricing in the system depends on flower type (premium, standard, budget), arrangement complexity (simple bouquet, elaborate arrangement, wedding package), and delivery options (same-day, next-day, scheduled delivery). Staff members can manage the flower inventory, keep track of stock levels, create custom arrangements, and process payments. The system accommodates both online ordering and in-store walk-in purchases at the flower shop.
The system is expected to be built using a client-server architecture:
- The client will be implemented with React technology.
- The server will be a REST API following the MVC pattern (e.g., ASP.NET Core Web API, Spring Boot REST, FastAPI, REST API with Node.js...).
- The database will be Relational Database such as Microsoft SQL Server (MS SQL) or MySQL or PostgreSQL.
- Communication between client and server is done via HTTP requests/responses using JSON data format.

## Part 1: Data analysis and design (5 points)
1. LIST the primary entities and their key attributes derived from the problem description. (1 point)
2. DRAW the conceptual ERD for the system. (1 point)
3. DRAW the logical ERD (with primary/foreign keys and basic data types). (1.5 points)
4. LIST the main states of the Order entity throughout the order process and DRAW the state diagram for Order. (1.5 points)
## Part 2: REST API function design (3 points)
1. DRAW a class diagram (detailed design) depicting the client-side and server-side classes (Controller, Service, Repository) used for the "create order" function. (1.5 points)
2. DRAW a sequence diagram for the "create order" function between client and server (REST API) with authentication and authorization. (1.5 points)
## Part 3: Design pattern identification and analysis (2 points)
Consider the following pseudocode:
```java
public interface Pricing {
    public double calculatePrice(double basePrice, int quantity, String customerType);
}

public class RegularPricing implements Pricing {
    public double calculatePrice(double basePrice, int quantity, String customerType) {
        return basePrice * quantity;
    }
}

public class SeasonalPricing implements Pricing {
    public double calculatePrice(double basePrice, int quantity, String customerType) {
        double seasonalDiscount = 0.15; // 15% seasonal discount
        return basePrice * quantity * (1 - seasonalDiscount);
    }
}

public class VIPPricing implements Pricing {
    public double calculatePrice(double basePrice, int quantity, String customerType) {
        double vipDiscount = 0.20; // 20% VIP discount
        return basePrice * quantity * (1 - vipDiscount);
    }
}

public class FlowerOrder {
    private Pricing pricing;
    public void setPricing(Pricing p) {
        this.pricing = p;
    }
    public double calculateOrderTotal(double basePrice, int quantity, String customerType) {
        return pricing.calculatePrice(basePrice, quantity, customerType);
    }
}
```
1. WHAT DESIGN PATTERN is used in the code above? Identify its name and pattern family (creational, structural, or behavioral). (0.5 points)
2. DRAW the class diagram for this pattern. (1 point)
3. DESCRIBE a practical situation in software development in which this pattern would be appropriate. (0.5 points)
**Good luck with your exam!**
