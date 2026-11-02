# OIBSIP-JavaDevelopment-Task1-OnlineReservationSystem-

A Java Swing desktop application for managing train ticket reservations.

## Overview

This project is a simple online reservation system that allows users to sign in, book train tickets, and cancel existing bookings. It uses SQLite for persistent storage and Java Swing for the graphical user interface.

## Features

- User login and authentication
- Demo accounts for testing
- Ticket booking form with validation
- Automatic train lookup using the train number
- PNR generation for each reservation
- Reservation cancellation by PNR
- Local SQLite database initialization on startup

## Demo Accounts

The system seeds default users into the database:

- Username: `admin`
- Password: `admin123`

- Username: `student`
- Password: `pass123`

## Tech Stack

- Java
- Swing GUI
- SQLite JDBC
- SHA-256 password hashing

## Project Structure

- `Main.java` – startup point and database initialization
- `Database.java` – SQLite connection, table creation, and demo data seeding
- `LoginFrame.java` – login screen
- `MainFrame.java` – main application window with tabs
- `BookingPanel.java` – booking form and validation logic
- `CancelPanel.java` – PNR lookup and cancellation
- `ReservationDAO.java` – database operations for authentication, booking, and cancellation
- `Reservation.java` – reservation model

## How to Run

1. Make sure Java and SQLite JDBC are installed.
2. Compile the project:

   ```bash
   javac -d out $(find . -name "*.java")
   ```

3. Run the app:

   ```bash
   java -cp out com.reservation.Main
   ```

## Notes

- The app creates a local `reservation.db` file automatically when it starts.
- The database and demo records are initialized on first launch.
- This project is intended as a Java desktop reservation system for learning and demonstration purposes.
