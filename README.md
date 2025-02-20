# IRCTC_APP

## Overview
IRCTC_APP is a Java-based ticket booking application designed to streamline the train ticketing process. The application provides an intuitive interface for managing train travel bookings and incorporates modern Java features such as the Stream API and lambda expressions for efficient and concise coding.

## Features
- **Sign Up:** Register a new account.
- **Login:** Securely authenticate with your credentials.
- **Fetch Bookings:** Retrieve all your current bookings.
- **Search Trains:** Find available trains based on your travel criteria.
- **Book a Seat:** Reserve a seat on a chosen train.
- **Cancel Booking:** Cancel an existing booking.
- **Exit the App:** Safely exit the application.

## Architecture

The application is built using a layered architecture that clearly separates concerns:

### Entity Layer
This layer contains the core data models and domain objects:
- **User:** Captures user details including username, encrypted password, and profile information.
- **Booking:** Represents ticket booking details such as booking ID, associated user, train details, seat number, and booking status.
- **Train:** Contains train-related data such as train number, name, available seats, schedule, and route.

These entity classes serve as the primary data holders and are serialized/deserialized to and from a local JSON database.

### Service Layer
The service layer encapsulates the business logic and interacts with both the presentation and entity layers:
- **User Management:** Handles user registration, authentication, and password security using JBCrypt.
- **Booking Management:** Manages operations for fetching, creating, and canceling bookings.
- **Train Management:** Processes train search queries and retrieves train information.
- **Data Handling:** Uses Java’s Stream API and lambda functions to efficiently manage and process data from the local JSON database.

## Technologies Used
- **Java:** Core programming language.
- **Stream API & Lambda Functions:** Employed for efficient data processing.
- **IntelliJ IDEA:** Integrated Development Environment (IDE) for development.
- **Gradle:** Build automation tool for dependency management and project building.

## Database
- **Local DB (JSON File):** The application uses a JSON file to store and manage data locally.

## Tools
- **IntelliJ IDEA:** Primary IDE for development.
- **Gradle:** Tool for building and managing project dependencies.

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
IntelliJ IDEA will detect the Gradle configuration automatically.
Import the project as a Gradle project to resolve all dependencies.
Build the Project:
Open the Gradle tool window in IntelliJ IDEA.
Run the build task to compile the project.
Run the Application:
Locate the main class (with the public static void main(String[] args) method).
Right-click the file and select Run, or execute the Gradle run task if configured.
Usage Instructions
Once the application is running, you can navigate through its features:

Sign Up / Login:
Begin by creating a new account using the sign-up feature.
Once registered, log in using your credentials.
Fetching Bookings:
After logging in, select the "Fetch Bookings" option to view your current bookings.
Searching for Trains:
Use the "Search Trains" feature to find available trains based on your desired criteria.
Booking a Seat:
When a suitable train is found, use the "Book a Seat" feature to reserve your seat.
Canceling a Booking:
If needed, cancel an existing booking by selecting the "Cancel Booking" option.
Exiting the App:
Use the "Exit the App" option to safely close the application.
Dependencies & Libraries
This project uses several external libraries to enhance functionality and ensure security:

Guava: Provides additional utilities and collections.
Jackson Databind (2.12.6): Facilitates JSON serialization and deserialization.
JBCrypt (org.mindrot:jbcrypt:0.4): Implements secure password hashing.
