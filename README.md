# IRCTC_APP

## Overview
IRCTC_APP is a Java-based ticket booking application designed to streamline the train ticketing process. It provides an intuitive interface for managing train travel bookings while leveraging modern Java features like the Stream API and lambda expressions for efficient coding.

## Features
- **Sign Up:** Register a new account.
- **Login:** Securely authenticate using your credentials.
- **Fetch Bookings:** Retrieve all your current bookings.
- **Search Trains:** Find available trains based on your travel criteria.
- **Book a Seat:** Reserve a seat on a chosen train.
- **Cancel Booking:** Cancel an existing booking.
- **Exit the App:** Safely exit the application.

## Architecture

### Entity Layer
This layer contains the core data models and domain objects:
- **User:** Contains user details such as username, encrypted password, and profile information.
- **Booking:** Represents ticket booking details including booking ID, user association, train information, seat number, and booking status.
- **Train:** Stores train-related data like train number, name, available seats, schedule, and route.

These classes are responsible for managing and storing data in the local JSON database.

### Service Layer
The service layer encapsulates the business logic and connects the presentation layer to the entity layer. Its responsibilities include:
- **User Management:** Handling registration, authentication, and secure password management using JBCrypt.
- **Booking Management:** Managing operations such as fetching, creating, and canceling bookings.
- **Train Management:** Processing train search queries and retrieving train data.
- **Data Handling:** Utilizing the Java Stream API and lambda functions for efficient data processing and CRUD operations with the local JSON database.

## Technologies Used
- **Java:** Core programming language.
- **Stream API & Lambda Functions:** For concise and efficient data processing.
- **IntelliJ IDEA:** Primary Integrated Development Environment.
- **Gradle:** Build automation tool for dependency management and project building.

## Database
- **Local DB (JSON File):** Data is stored and managed locally using a JSON file.

## Tools
- **IntelliJ IDEA:** The main IDE used for developing the application.
- **Gradle:** Used for building the project and managing dependencies.

## Installation

Follow these steps to set up the project on your local machine:

1. **Clone the Repository:**
   ```bash
   git clone <repository_url>
   cd IRCTC_APP
Open the Project in IntelliJ IDEA:
Launch IntelliJ IDEA.
Click on Open and select the cloned repository folder.
Import the Gradle Project:
IntelliJ IDEA should automatically detect the Gradle configuration.
Import the project as a Gradle project to resolve all dependencies.
Build the Project:
Open the Gradle tool window in IntelliJ IDEA.
Run the build task to compile the project.
Run the Application:
Locate the main class (the one with the public static void main(String[] args) method).
Right-click the file and select Run, or execute the Gradle run task if configured.
Usage Instructions
After launching the application, use the following guidelines to navigate through its features:

Sign Up / Login:
Start by creating a new account via the sign-up feature.
Once registered, log in with your credentials.
Fetching Bookings:
After logging in, select the "Fetch Bookings" option to view your current bookings.
Searching for Trains:
Use the "Search Trains" option to look for available trains that meet your travel criteria.
Booking a Seat:
When you identify a suitable train, use the "Book a Seat" feature to reserve a seat.
Canceling a Booking:
To cancel a booking, select the "Cancel Booking" option.
Exiting the App:
Use the "Exit the App" option to safely close the application.
Dependencies & Libraries
This project leverages several external libraries to enhance functionality and ensure security:

Guava: Provides additional utilities and collections.
Jackson Databind (2.12.6): Facilitates JSON serialization and deserialization.
JBCrypt (org.mindrot:jbcrypt:0.4): Implements secure password hashing.
