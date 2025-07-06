
# Bus Booking System (Java)

This is a simple console-based Bus Booking System written in Java using JDBC to connect with a MySQL database.

## Features

- View available buses
- Book a seat on a bus
- View bookings by date
- Prevents overbooking

## Technologies Used

- Java
- JDBC
- MySQL

## How to Run

1. Set up the MySQL database:

```sql
CREATE DATABASE busbooking;

USE busbooking;

CREATE TABLE bus (
    id INT PRIMARY KEY,
    ac BOOLEAN,
    capacity INT,
    departTime VARCHAR(20)
);

CREATE TABLE booking (
    id INT AUTO_INCREMENT PRIMARY KEY,
    passengerName VARCHAR(50),
    bus_no INT,
    date DATE,
    FOREIGN KEY (bus_no) REFERENCES bus(id)
);
```

2. Update database credentials in `DbConnection.java`.

3. Compile and run:

```bash
javac *.java
java BusDemo
```

## Files

- `Bus.java` - Bus model
- `Booking.java` - Booking model
- `BusDAO.java` - Bus database access
- `BookingDAO.java` - Booking database access
- `DbConnection.java` - Database connection
- `BusDemo.java` - Main program

## Author

Created by shanmugpandiyan
