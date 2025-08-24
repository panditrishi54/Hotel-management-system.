Hotel Management System

Overview

This project is a Java-based Hotel Management System designed to manage hotel room bookings, food orders, billing, and room deallocation. It supports different room types (Luxury and Deluxe, Single and Double) and includes features such as room availability checks, customer details management, and serialization for persistent data storage.

Features

Room Types: Supports Luxury Double, Deluxe Double, Luxury Single, and Deluxe Single rooms with varying charges and amenities.
Booking System: Allows users to book rooms by providing customer details and selecting available room numbers.
Food Ordering: Customers can order food items (Sandwich, Pasta, Noodles, Coke) with associated prices.
Billing: Generates bills based on room charges and food orders.
Room Deallocation: Supports checking out and deallocating rooms with bill generation.
Room Availability: Displays the number of available rooms for each room type.
Data Persistence: Uses serialization to save and load hotel data to/from a file (backup).
Exception Handling: Includes custom NotAvailable exception for invalid room bookings.

Project Structure
Classes:
Food: Represents food items with item number, quantity, and price calculation.
Singleroom: Stores details for single room occupants (name, contact, gender, food orders).
Doubleroom: Extends Singleroom to support two occupants.
NotAvailable: Custom exception for unavailable rooms.
holder: Manages arrays of Doubleroom and Singleroom objects for different room types.
Hotel: Contains core functionality for booking, ordering, billing, and deallocation.
write: Implements Runnable to handle serialization of hotel data.
Main: Entry point with a menu-driven interface for user interaction.

Prerequisites
Java Development Kit (JDK) 8 or higher
A Java IDE (e.g., IntelliJ IDEA, Eclipse) or command-line environment for compilation and execution

How to Run
Clone the Repository:

git clone https://https://github.com/panditrishi54/Hotel-management-system.git
cd hotel-management-system

Compile the Code:
javac Main.java

Run the Application:
java Main



Interact with the Menu:

Choose from options:




Display room details



Display room availability



Book a room



Order food



Checkout



Exit



Follow prompts to input customer details, room numbers, or food orders.

Usage





Room Numbers:





Luxury Double: 1–10



Deluxe Double: 11–30



Luxury Single: 31–40



Deluxe Single: 41–60



Food Menu:





Sandwich: ₹50



Pasta: ₹60



Noodles: ₹70



Coke: ₹30



Billing: Room charges are fixed (e.g., ₹4000/day for Luxury Double, ₹1200/day for Deluxe Single) and added to food costs.



Data Storage: The system saves data to a backup file using serialization and loads it on startup if available.

Example Workflow





Select option 3 to book a room.



Choose a room type (e.g., 1 for Luxury Double).



View available room numbers and enter a valid one.



Provide customer details (name, contact, gender; second customer for double rooms).



Order food using option 4, specifying the room number and menu items.



Check out using option 5 to generate a bill and deallocate the room.

Notes





The system uses a Scanner for user input and supports basic error handling for invalid inputs.



Room numbers are offset for user display (e.g., Deluxe Single rooms are shown as 41–60 but stored as 0–19 in the array).



Serialization ensures data persists between program runs, stored in the backup file.

Future Improvements





Add a graphical user interface (GUI) for better user experience.



Implement user authentication and role-based access (e.g., admin vs. customer).



Enhance food menu with dynamic pricing and additional items.



Add support for multiple-day bookings with date tracking.
