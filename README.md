# ✈️ Airline Reservation System — Java

A **Java-based desktop Airline Reservation System** built with a graphical user interface (GUI) using **Java Swing**, backed by a **MySQL database** via JDBC. This project demonstrates real-world application of Object-Oriented Programming (OOP) principles in a practical, multi-module system.

---

## 📸 Overview

This system simulates core functionalities of an airline booking platform, allowing users to register, log in, search for flights, book tickets, generate boarding passes, and cancel reservations — all through a clean Swing-based GUI.

---

## ✨ Features

### 👤 User Management
- Register a new customer account (`AddCustomer.java`)
- Secure login with credential validation (`Login.java`)
- User-friendly home dashboard after login (`Home.java`)

### 🛫 Flight & Booking Management
- Browse and view available flight information (`FlightInfo.java`)
- Book a flight with seat selection (`BookFlight.java`)
- View detailed journey information (`JourneyDetails.java`)
- Cancel an existing booking (`Cancel.java`)

### 🎫 Boarding Pass
- Generate and display a boarding pass for a confirmed booking (`BoardingPass.java`)

### 🗄️ Database Integration
- Centralized MySQL database connection handler (`Conn.java`)
- Persistent storage of customer, flight, and booking data (`db.txt` — DB schema/setup)

---

## 🧰 Tech Stack

| Technology        | Purpose                                      |
|-------------------|----------------------------------------------|
| **Java (JDK 8+)** | Core programming language                    |
| **Java Swing**    | GUI components and windows                   |
| **JDBC**          | Java Database Connectivity                   |
| **MySQL**         | Relational database for persistent storage   |
| **OOP Principles**| Encapsulation, Inheritance, Polymorphism      |

---

## 📂 Project Structure

```
AirlineReservationSystemWithJAVA/
│
├── AddCustomer.java      # New customer registration form
├── BoardingPass.java     # Boarding pass generation and display
├── BookFlight.java       # Flight booking interface
├── Cancel.java           # Booking cancellation
├── Conn.java             # MySQL database connection utility
├── FlightInfo.java       # View available flights
├── Home.java             # Main dashboard after login
├── JourneyDetails.java   # View journey/booking details
├── Login.java            # User login screen
└── db.txt                # Database schema / SQL setup queries
```

---

## ⚙️ Prerequisites

Before running this project, make sure you have the following installed:

- [Java JDK 8 or above](https://www.oracle.com/java/technologies/downloads/)
- [MySQL Server](https://dev.mysql.com/downloads/mysql/)
- [MySQL Connector/J (JDBC Driver)](https://dev.mysql.com/downloads/connector/j/)
- An IDE like [IntelliJ IDEA](https://www.jetbrains.com/idea/) or [Eclipse](https://www.eclipse.org/), or a terminal

---

## 🚀 Installation & Setup

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/dev-pritam-2005/AirlineReservationSystemWithJAVA.git
cd AirlineReservationSystemWithJAVA
```

### 2️⃣ Set Up the Database

1. Open **MySQL Workbench** or your MySQL client.
2. Open and run the SQL commands from `db.txt` to create the required database and tables.
3. Note down your MySQL **host**, **port**, **username**, and **password**.

### 3️⃣ Configure the Database Connection

Open `Conn.java` and update your credentials:

```java
Connection con = DriverManager.getConnection(
    "jdbc:mysql://localhost:3306/airlinereservation",
    "your_username",
    "your_password"
);
```

### 4️⃣ Add the JDBC Driver to Classpath

Download `mysql-connector-j-x.x.x.jar` and place it in your project directory or add it to your IDE's build path.

### 5️⃣ Compile the Project

```bash
javac -cp .;mysql-connector-j-x.x.x.jar *.java
```

> On Linux/macOS, replace `;` with `:` in the classpath separator.

### 6️⃣ Run the Application

```bash
java -cp .;mysql-connector-j-x.x.x.jar Login
```

---

## 💡 Usage Workflow

```
Launch App (Login.java)
    │
    ├── New User? → AddCustomer.java → Register → Login
    │
    └── Existing User? → Login → Home.java (Dashboard)
                                      │
                        ┌─────────────┼─────────────┐─────────────┐
                        │             │             │             │
                  FlightInfo    BookFlight   JourneyDetails    Cancel
                        │             │
                        └─────────────┘
                              │
                        BoardingPass.java
```

---

## 🎯 Learning Objectives

This project is a great hands-on exercise for learning:

- **Java Swing GUI** development (frames, panels, buttons, text fields, tables)
- **JDBC** for database connection and CRUD operations
- **OOP Design** — class separation by responsibility
- **Event-driven programming** using action listeners
- **Database schema design** for a real-world application

---

## 🚀 Future Improvements

- [ ] Add an **Admin Panel** for managing flights and users
- [ ] Implement **password hashing** for secure login
- [ ] Add **search/filter** functionality for flights by date, destination, or price
- [ ] Integrate **online payment simulation**
- [ ] Migrate to a **Spring Boot + React** web version
- [ ] Add **email confirmation** for bookings using JavaMail API
- [ ] Write **unit tests** using JUnit

---

## 👨‍💻 Author

**Pritam Dutta**

- GitHub: [@dev-pritam-2005](https://github.com/dev-pritam-2005)

---

## 📜 License

This project is open-source and available under the [MIT License](LICENSE).

---

> ⭐ If you found this project helpful, consider giving it a star on GitHub!
