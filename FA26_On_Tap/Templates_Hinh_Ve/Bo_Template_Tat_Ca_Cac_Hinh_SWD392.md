# BỘ TEMPLATE TẤT CẢ CÁC HÌNH VẼ TRONG ĐỀ THI SWD392 PE (ĐIỀN KHUYẾT LÀ DÙNG NGAY)

> **Thư mục chứa các file `.drawio` mở trực tiếp bằng Draw.io Desktop:**  
> 📁 `c:\Users\ASUS\Desktop\SWD392_PE\FA26_On_Tap\Templates_Hinh_Ve`

---

## 1. DANH SÁCH FILE `.DRAWIO` ĐÃ TẠO SẴN CHO BẠN

Bạn chỉ cần mở phần mềm **Draw.io Desktop** $\rightarrow$ bấm `File -> Open` và chọn:

| STT | Tên File `.drawio` | Công dụng trong phòng thi |
| :-: | :--- | :--- |
| **⭐ 0** | **`00_SWD392_PE_ALL_IN_ONE_TEMPLATES.drawio`** | **File Tổng Hợp 7 Tab trong 1 file duy nhất!** Mở 1 file này lên là có đủ 7 tab ở thanh dưới cùng của Draw.io. |
| **1** | `01_Template_Class_Diagram_PE.drawio` | **Template Câu 1 (3.0đ):** Đựng sẵn 3 cụm (`User` kế thừa + `Entities` có `1`, `0..*`, Composition/Aggregation + `Controller -> Service -> IGenericRepository<T> <- Repositories`). |
| **2** | `02_Template_Sequence_Diagram_PE.drawio` | **Template Câu 2 (4.0đ):** Đựng sẵn khung `sd`, 7 cột Lifelines, 2 khung `alt` (còn chỗ vs hết chỗ; thanh toán thành công vs thất bại), đánh số message 1–24 và mũi tên trả về nét đứt. |
| **3** | `03_Template_Statechart_Diagram_PE.drawio` | **Template Câu 3A (3.0đ / 1.5đ):** Đựng sẵn `●` Initial, `◉` Final, 5 trạng thái chính + 2 trạng thái hủy/lỗi (`Cancelled`, `PaymentFailed/Rejected`), 8 mũi tên có sẵn nhãn `event [guard]`. |
| **4** | `04_Template_Activity_Diagram_Swimlanes_PE.drawio` | **Template Câu 3B (3.0đ):** Đựng sẵn bảng 2 cột **Swimlanes** (`Host/Customer` và `System`), hình thoi **Decision Node**, thanh đồng thời cập nhật 2 trạng thái cuối quy trình. |
| **5** | `05_Template_ERD_Conceptual_And_Logical_PE.drawio` | **Template Part 1.2 & 1.3 (2.5đ):** Gồm cả **Conceptual ERD** (không FK, không kiểu dữ liệu) ở nửa trên và **Logical ERD** (có PK/FK, kiểu dữ liệu, bảng trung gian) ở nửa dưới. |
| **6** | `06_Template_UseCase_Diagram_PE.drawio` | **Template Part 1.3 (1.5đ):** Đựng sẵn khung System Boundary, Actors bên ngoài, các Use Case chuẩn động từ và mũi tên `«include»` / `«extend»` đúng chiều. |
| **7** | `07_Template_4_Design_Patterns_PE.drawio` | **Template Part 3.2 (1.0đ):** Đựng sẵn 4 sơ đồ Class Diagram của đúng 4 Pattern trong đề: **Observer, Strategy, Decorator, Singleton**. |

---

## 2. BẢNG TRA CỨU ĐIỀN KHUYẾT `[...]` CHO TẤT CẢ CÁC ĐỀ TRƯỚC ĐÂY

Khi mở Template lên, bạn chỉ việc thay các ô ngoặc vuông `[...]` theo bảng đối chiếu này:

| Từ khóa trong Template | Đề `FA26_Ex` (StayEase) | Đề `SP26` (EMS Event) | Đề `SU26_PE1` (SmartPark) | Đề `SU26_PE2` (MediCare) | Đề `SU25` (Cinema) | Đề `SU25` (FlowerShop) | Đề `Fall25` (Food) |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **`[Role1]`** *(Người đặt/mua)* | `Customer` | `Student`, `Lecturer` | `Customer` *(+ `Vehicle`)* | `Patient` | `Customer` | `Customer` | `User` / `Customer` |
| **`[Role2]`** *(Người cung cấp)* | `Host` | `Organizer` | `ParkingStaff` | `Doctor` | `Staff` | `Staff` | `Restaurant` |
| **`[Role3]`** *(Người quản lý/lễ tân)* | `Staff` / `Admin` | `Admin` | `Admin` | `Receptionist` | `Admin` | `Admin` | `Admin` |
| **`[Resource]`** *(Tài nguyên được đặt)* | `Room` | `Event` | `ParkingSlot` | `DoctorSchedule` | `Showtime` & `Seat` | `Flower` | `Dish` |
| **`[MainTx]`** *(Giao dịch chính)* | `Reservation` | `Registration` | `ParkingTicket` | `Appointment` | `Booking` | `Order` | `Order` |
| **`[Payment]`** *(Thanh toán)* | `Payment` | *(Không bắt buộc)* | `Payment` | `Payment` | `Payment` | `Payment` | `Payment` |
| **`[Service]`** | `BookingService` | `EventService` | `ParkingService` | `AppointmentService` | `BookingService` | `OrderService` | `OrderService` |
| **`[ResourceRepo]`** | `RoomRepository` | `EventRepository` | `ParkingSlotRepository` | `DoctorRepository` | `ShowtimeRepository` | `FlowerRepository` | `DishRepository` |
| **`[MainTxRepo]`** | `ReservationRepository` | `RegistrationRepository` | `ParkingTicketRepository` | `AppointmentRepository` | `BookingRepository` | `OrderRepository` | `OrderRepository` |

---

## 3. HÌNH XEM TRƯỚC (MERMAID LIVE PREVIEW) CỦA TẤT CẢ 7 TEMPLATE

*(Bạn cũng có thể copy khối mã bên dưới vào Draw.io bằng cách bấm: `Arrange -> Insert -> Advanced -> Mermaid...`)*

---

### HÌNH 1A: TEMPLATE CLASS DIAGRAM CHUẨN ĐỀ MỚI (3.0 ĐIỂM)

```mermaid
classDiagram
    direction TB
    class User {
        <<entity>>
        #int userId
        #String fullName
        #String email
        #String phone
        +login(email, pass) bool
        +updateProfile() void
    }
    class Role1_Customer_Patient_Student {
        <<entity>>
        -String memberCode
        +searchResource() List
        +createMainTx() MainTx
    }
    class Role2_Host_Doctor_Organizer {
        <<entity>>
        -String departmentOrSpecialty
        +manageResource() void
    }
    class Role3_Staff_Receptionist_Admin {
        <<entity>>
        -String staffCode
        +confirmOrMonitor() void
    }

    class Resource_Room_Event_Slot_Schedule {
        <<entity>>
        -int resourceId
        -String nameOrCode
        -double priceOrCapacity
        -String status
        +isAvailable() bool
        +updateStatus(newStatus) void
    }
    class MainTx_Reservation_Registration_Ticket_Appointment {
        <<entity>>
        -int transactionId
        -DateTime createdDate
        -double totalAmount
        -String status
        +calculateTotal() double
        +updateStatus(newStatus) void
    }
    class Payment {
        <<entity>>
        -int paymentId
        -double amount
        -DateTime paymentDate
        -String paymentStatus
        +processPayment() bool
    }

    class IGenericRepository~T~ {
        <<interface>>
        +getById(id) T
        +getAll() List~T~
        +save(entity) void
        +update(entity) void
        +delete(id) void
    }
    class ResourceRepository {
        <<repository>>
        +getById(id) Resource
        +save(entity) void
        +checkAvailability(id) bool
        +updateStatus(id, status) void
    }
    class MainTxRepository {
        <<repository>>
        +getById(id) MainTx
        +save(entity) void
        +update(entity) void
        +updateStatus(id, status) void
    }
    class MainTxService {
        <<service>>
        -IGenericRepository resourceRepo
        -IGenericRepository mainTxRepo
        +processMainTx(userId, resourceId) bool
    }
    class MainTxController {
        <<controller>>
        -MainTxService service
        +submitMainTxRequest(userId, resourceId) Response
    }

    User <|-- Role1_Customer_Patient_Student
    User <|-- Role2_Host_Doctor_Organizer
    User <|-- Role3_Staff_Receptionist_Admin

    Role2_Host_Doctor_Organizer "1" o-- "0..*" Resource_Room_Event_Slot_Schedule : manages
    Role1_Customer_Patient_Student "1" --> "0..*" MainTx_Reservation_Registration_Ticket_Appointment : creates
    MainTx_Reservation_Registration_Ticket_Appointment "0..*" --> "1" Resource_Room_Event_Slot_Schedule : refers to
    MainTx_Reservation_Registration_Ticket_Appointment "1" *-- "0..1" Payment : contains

    IGenericRepository~T~ <|.. ResourceRepository
    IGenericRepository~T~ <|.. MainTxRepository

    MainTxController ..> MainTxService : uses
    MainTxService ..> IGenericRepository~T~ : depends on
    ResourceRepository ..> Resource_Room_Event_Slot_Schedule : manages
    MainTxRepository ..> MainTx_Reservation_Registration_Ticket_Appointment : manages
```

---

### HÌNH 1B: TEMPLATE CLASS DIAGRAM CÓ ASSOCIATION CLASS (ĐỀ `SU25_CYBERAI` & `SU25_FINAL`)

```mermaid
classDiagram
    class University {
        <<entity>>
        -int universityId
        -String name
    }
    class Department {
        <<entity>>
        -int deptId
        -String deptName
    }
    class Professor {
        <<entity>>
        #int profId
        #String fullName
    }
    class TenuredProfessor {
        <<entity>>
        -double researchGrant
    }
    class AdjunctProfessor {
        <<entity>>
        -int contractHours
    }
    class Student {
        <<entity>>
        -String studentId
        -String fullName
    }
    class Course {
        <<entity>>
        -String courseId
        -String title
        -int credits
    }
    class GradeReport {
        <<Association Class>>
        -String reportId
        -double finalGrade
        -String semester
        +isPassed() bool
    }

    University "1" *-- "1..*" Department : Composition (cannot exist alone)
    Department "1" o-- "1..*" Professor : Aggregation (exists independently)
    Professor <|-- TenuredProfessor
    Professor <|-- AdjunctProfessor
    Student "0..*" -- "0..*" Course : enrolls in
    Course .. GradeReport : Association Class
    Student .. GradeReport : Association Class
```

---

### HÌNH 2: TEMPLATE SEQUENCE DIAGRAM CHUẨN 4.0 ĐIỂM (LAYERED + REPOSITORY + 2 KHUNG `ALT`)

```mermaid
sequenceDiagram
    autonumber
    actor Actor as [Actor: Customer / Patient / Student]
    participant UI as :[PortalOrUI]<br/>«boundary»
    participant Ctrl as :[MainTx]Controller<br/>«control»
    participant Svc as :[MainTx]Service<br/>«service»
    participant ResRepo as :[Resource]Repository<br/>«repository»
    participant TxRepo as :[MainTx]Repository<br/>«repository»
    participant Ent as :[Resource] & :[MainTx]<br/>«entity»

    Actor->>+UI: submit[MainTx]Request(resourceId, details)
    UI->>+Ctrl: create[MainTx](userId, resourceId, details)
    Ctrl->>+Svc: process[MainTx](userId, resourceId, details)

    Svc->>+ResRepo: checkAvailability(resourceId)
    ResRepo->>+Ent: getStatusAndCapacity(resourceId)
    Ent-->>-ResRepo: status = "Available"
    ResRepo-->>-Svc: isAvailable (boolean)

    alt [isAvailable == true (Resource is Available / Open)]
        Svc->>+Ent: processPaymentOrSecondCheck(userId, amount)
        Ent-->>-Svc: paymentSuccess (boolean)

        alt [paymentSuccess == true (Payment / Validation Succeeded)]
            Svc->>+Ent: create[MainTx](userId, resourceId, "Confirmed")
            Ent-->>-Svc: new[MainTx]Obj

            Svc->>+TxRepo: save(new[MainTx]Obj)
            TxRepo-->>-Svc: savedSuccess

            Svc->>+ResRepo: updateStatus(resourceId, "Booked / Occupied")
            ResRepo->>+Ent: setStatus("Booked / Occupied")
            Ent-->>-ResRepo: updated
            ResRepo-->>-Svc: statusUpdated

            Svc-->>Ctrl: Result(success = true, confirmationData)
            Ctrl-->>UI: HTTP 201 Created ("Confirmed")
            UI-->>Actor: Display confirmation message
        else [else: paymentSuccess == false (Payment Failed)]
            Svc-->>Ctrl: Result(success = false, "Payment Failed")
            Ctrl-->>UI: HTTP 400 Bad Request ("Payment Failed")
            UI-->>Actor: Display payment error message
        end
    else [else: isAvailable == false (Resource Occupied / Full / Closed)]
        Svc-->>-Ctrl: Result(success = false, "Resource Not Available")
        Ctrl-->>-UI: HTTP 409 Conflict ("Resource Unavailable")
        UI-->>-Actor: Display unavailable / rejection notification
    end
```

---

### HÌNH 3: TEMPLATE STATECHART DIAGRAM (CÂU 3A – ĐỦ $\ge 6$ TRANSITIONS + NHÁNH HỦY/LỖI)

```mermaid
stateDiagram-v2
    [*] --> Pending_Or_Draft : 1. create[Entity]()

    Pending_Or_Draft --> Confirmed_Or_Approved : 2. paySuccess / approve [valid]
    Pending_Or_Draft --> PaymentFailed_Or_Rejected : 3. payFail / reject [invalid]
    Pending_Or_Draft --> Cancelled : 4. cancel [by User]

    Confirmed_Or_Approved --> CheckedIn_Or_Open : 5. checkIn / openRegistration
    Confirmed_Or_Approved --> Cancelled : 6. cancel [before start]

    CheckedIn_Or_Open --> InConsultation_Or_Ongoing : 7. startExecution

    InConsultation_Or_Ongoing --> Completed : 8. finishExecution / saveOutcome()

    PaymentFailed_Or_Rejected --> [*]
    Cancelled --> [*]
    Completed --> [*]
```

---

### HÌNH 4: TEMPLATE ACTIVITY DIAGRAM 2 SWIMLANES (CÂU 3B – 3.0 ĐIỂM)

```mermaid
flowchart TD
    subgraph Lane1 ["Swimlane 1: [Host / Customer]"]
        Start((●)) --> Step1["Step 1: Inspect Room / Drive to Exit Gate"]
        Step1 --> Step2["Step 2: Submit Inspection Results / Ticket"]
        Step4["Step 4: Settle Final Invoice / Make Payment"]
        EndNode(((◉)))
    end

    subgraph Lane2 ["Swimlane 2: [System (StayEase / SmartPark)]"]
        Step3["Step 3: Evaluate Report / Calculate Fee"]
        Dec{"Condition?<br/>(Damage Found /<br/>Payment Valid)"}
        BranchA["Calculate Damage Fee &<br/>Add to Final Invoice"]
        BranchB["Generate Standard Invoice<br/>(Remaining Balance Only)"]
        Step5a["Step 5a: Update [Reservation / Ticket]<br/>status = 'Completed'"]
        Step5b["Step 5b: Update [Room / ParkingSlot]<br/>status = 'Cleaning / Available'"]
    end

    Step2 --> Step3
    Step3 --> Dec
    Dec -- "[Yes / Damage Found]" --> BranchA
    Dec -- "[No / No Damage]" --> BranchB
    BranchA --> Step4
    BranchB --> Step4
    Step4 -- "Payment Confirmed" --> Step5a
    Step5a --> Step5b
    Step5b --> EndNode
```

---

### HÌNH 5: TEMPLATE ERD (CONCEPTUAL ERD VS LOGICAL ERD – PART 1.2 & 1.3)

#### 5A. Conceptual ERD (Câu 1.2 – KHÔNG FK, KHÔNG KIỂU DỮ LIỆU)
```mermaid
erDiagram
    CUSTOMER ||--o{ ORDER_BOOKING : "places"
    RESTAURANT_CATEGORY ||--|{ DISH_FLOWER_MOVIE : "offers"
    ORDER_BOOKING }|--|{ DISH_FLOWER_MOVIE : "contains"

    CUSTOMER {
        string customerId "Identifier (Underlined)"
        string fullName
        string email
        string phone
    }
    RESTAURANT_CATEGORY {
        string providerId "Identifier (Underlined)"
        string name
        string location
    }
    DISH_FLOWER_MOVIE {
        string itemId "Identifier (Underlined)"
        string itemName
        string price
        string status
    }
    ORDER_BOOKING {
        string orderId "Identifier (Underlined)"
        string orderDate
        string totalAmount
        string status
    }
```

#### 5B. Logical ERD (Câu 1.3 – CÓ PK, FK, KIỂU DỮ LIỆU & BẢNG TRUNG GIAN)
```mermaid
erDiagram
    CUSTOMER ||--o{ ORDER_BOOKING : "places"
    RESTAURANT_CATEGORY ||--o{ DISH_FLOWER_MOVIE : "offers"
    ORDER_BOOKING ||--|{ ORDER_DETAIL : "includes"
    DISH_FLOWER_MOVIE ||--o{ ORDER_DETAIL : "appears_in"

    CUSTOMER {
        int customerId PK
        varchar fullName
        varchar email
        varchar phone
    }
    RESTAURANT_CATEGORY {
        int providerId PK
        varchar name
        varchar location
    }
    DISH_FLOWER_MOVIE {
        int itemId PK
        int providerId FK
        varchar itemName
        decimal price
        varchar status
    }
    ORDER_BOOKING {
        int orderId PK
        int customerId FK
        datetime orderDate
        decimal totalAmount
        varchar status
    }
    ORDER_DETAIL {
        int orderDetailId PK
        int orderId FK
        int itemId FK
        int quantity
        decimal unitPrice
    }
```

---

### HÌNH 6: TEMPLATE USE CASE DIAGRAM (PART 1.3 ĐỀ CINEMA)

```mermaid
flowchart LR
    Cust(["웃 Customer"])
    Staff(["웃 Staff / Admin"])
    Ext(["웃 «system»<br/>Email / Payment"])

    subgraph SystemBoundary ["[System Name: Cinema Management System]"]
        UC1(["Browse Movies & Showtimes"])
        UC2(["View Movie Details"])
        UC3(["Reserve Ticket Online"])
        UC4(["Select Specific Seat"])
        UC5(["Process Ticket Payment"])
        UC6(["Send Confirmation Email"])
        UC7(["View Booking History"])
        UC8(["Cancel Booking"])
        UC9(["Create Walk-in Ticket Purchase"])
        UC10(["Create & Update Movie Schedule"])
        UC11(["Track Seat Availability"])
    end

    Cust --- UC1
    Cust --- UC3
    Cust --- UC7

    Staff --- UC9
    Staff --- UC10
    Staff --- UC11

    UC5 --- Ext
    UC6 --- Ext

    UC3 -. "«include»" .-> UC4
    UC3 -. "«include»" .-> UC5
    UC3 -. "«include»" .-> UC6
    UC9 -. "«include»" .-> UC4
    UC9 -. "«include»" .-> UC5

    UC2 -. "«extend»" .-> UC1
    UC8 -. "«extend»" .-> UC7
```

---

### HÌNH 7: TEMPLATE 4 DESIGN PATTERNS CLASS DIAGRAM (PART 3.2)

#### 7.1. Observer Pattern (`SU25_Cinema` & `SU25_CyberAI`)
```mermaid
classDiagram
    class Notification {
        <<interface>>
        +update(movieTitle: String, showTime: String, availableSeat: int) void
    }
    class ShowtimeSubject {
        -List~Notification~ notifications
        -String movieTitle
        -String showTime
        -int availableSeat
        +addNotification(n: Notification) void
        +removeNotification(n: Notification) void
        +notifyNotifications() void
        +updateShowtime(title: String, time: String, seat: int) void
    }
    class CustomerNotification {
        +update(movieTitle: String, showTime: String, availableSeat: int) void
    }
    ShowtimeSubject "1" o-- "0..*" Notification : notifies
    Notification <|.. CustomerNotification
```

#### 7.2. Strategy Pattern (`SU25_FlowerShop`)
```mermaid
classDiagram
    class Pricing {
        <<interface>>
        +calculatePrice(basePrice: double, quantity: int, customerType: String) double
    }
    class RegularPricing {
        +calculatePrice(basePrice: double, quantity: int, customerType: String) double
    }
    class SeasonalPricing {
        -double seasonalDiscount = 0.15
        +calculatePrice(basePrice: double, quantity: int, customerType: String) double
    }
    class VIPPricing {
        -double vipDiscount = 0.20
        +calculatePrice(basePrice: double, quantity: int, customerType: String) double
    }
    class FlowerOrder {
        -Pricing pricing
        +setPricing(p: Pricing) void
        +calculateOrderTotal(basePrice: double, quantity: int, customerType: String) double
    }
    FlowerOrder "1" o-- "1" Pricing : uses
    Pricing <|.. RegularPricing
    Pricing <|.. SeasonalPricing
    Pricing <|.. VIPPricing
```

#### 7.3. Decorator Pattern (`Fall25_OnlineFood`)
```mermaid
classDiagram
    class Dish {
        <<interface>>
        +getDescription() String
        +getCost() double
    }
    class BasicDish {
        +getDescription() String
        +getCost() double
    }
    class DishDecorator {
        <<abstract>>
        #Dish decoratedDish
        +DishDecorator(dish: Dish)
        +getDescription() String
        +getCost() double
    }
    class CheeseDecorator {
        +CheeseDecorator(dish: Dish)
        +getDescription() String
        +getCost() double
    }
    class SauceDecorator {
        +SauceDecorator(dish: Dish)
        +getDescription() String
        +getCost() double
    }
    Dish <|.. BasicDish
    Dish <|.. DishDecorator
    DishDecorator o-- "1" Dish : wraps (decoratedDish)
    DishDecorator <|-- CheeseDecorator
    DishDecorator <|-- SauceDecorator
```

#### 7.4. Singleton Pattern (`SU25_Student` & `SU25_Final`)
```mermaid
classDiagram
    class SystemSettings {
        -static SystemSettings instance
        -String academicYear
        -SystemSettings()
        +static getInstance() SystemSettings
        +getAcademicYear() String
    }
```
