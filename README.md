# Hotel Management System

## Introduction

This project is a **Hotel Management System** developed using **Spring Boot and Spring Data JPA**. The purpose of this application is to manage hotel operations such as room management and customer bookings in a simple and organized way.

The system allows a hotel administrator to add rooms, view available rooms, manage bookings made by customers, and update or cancel bookings when required.

---

## Technologies Used

* Java
* Spring Boot
* Spring Data JPA
* MySQL Database
* Maven
* REST APIs
* Postman (for testing APIs)

---

## Project Structure

The application follows a **3-layer architecture**:

**Controller Layer**
Handles incoming HTTP requests and sends responses.

**Service Layer**
Contains the business logic of the application.

**Repository Layer**
Responsible for interacting with the database using Spring Data JPA.

Package structure:


com.hotelmanagement
controller
service
service.impl
repository
entity


 Modules Implemented
 1. Room Management

This module allows the administrator to manage hotel rooms.

Operations performed:

* Add a new room
* View all rooms
* Get room details by ID
* Update room information
* Delete a room

Room fields:

* roomId
* roomNumber
* roomType
* price
* status


 2. Booking Management

This module allows customers to book rooms in the hotel.

Operations performed:

* Create a new booking
* View all bookings
* Get booking details by ID
* Update booking information
* Cancel a booking

Booking fields:

* bookingId
* customerName
* customerPhone
* checkInDate
* checkOutDate
* roomId

 Database Configuration

The project uses **MySQL database**.

Create the database using the following command:

```id="h2poh1"
CREATE DATABASE hotel_db;
```

Database configuration in `application.properties`:

```id="lqk7pv"
spring.datasource.url=jdbc:mysql://localhost:3306/hotel_db
spring.datasource.username=root
spring.datasource.password=root
spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
```

---

## How to Run the Project

1. Clone or download the project.
2. Import it as a **Maven Project** in Eclipse or Spring Tool Suite.
3. Create the database in MySQL.
4. Run the main class `HotelManagementApplication.java`.
5. Use **Postman** to test the REST APIs.

---
 Conclusion

This project demonstrates how a simple **Hotel Management System** can be built using Spring Boot with a clean layered architecture.
It provides basic CRUD operations for managing rooms and customer bookings and helps in understanding how Spring Boot applications interact with databases.
