Inventory Manager App
Project Overview

The Inventory Manager app was developed to provide users with a simple and effective way to manage and track inventory items. The main goal was to design a user-centered mobile application that allows individuals or small businesses to record, update, and monitor items in their inventory. This app addresses the need for a lightweight, accessible tool to help users stay organized without requiring complex software.

Requirements and Goals

The app was designed to meet several key requirements:

Allow users to create an account and securely log in.

Store user accounts and inventory data in a persistent SQLite database.

Provide CRUD functionality for inventory data: users can create, read, update, and delete items.

Display stored inventory data in a grid format for easy readability.

Request SMS permissions and send alerts via SMS when triggered (e.g., after new data is added). If denied, the app continues functioning without SMS notifications.

These features ensure the app supports both new and returning users while maintaining usability and flexibility.

Screens and Features

The app includes the following screens:

Login Screen: Allows users to log in with existing credentials or create a new account if they are first-time users.

Main Inventory Screen (Grid): Displays a grid of all stored inventory items and provides options to add, delete, or update entries.

Add Item Screen: Provides input fields for item details (title, description, quantity, etc.).

User interface design was centered on simplicity, readability, and minimizing the number of taps needed to perform actions. Text inputs, buttons, and lists were styled to be clear and intuitive. This approach ensured a successful design because it considered first-time users and prioritized clarity over complexity.

Coding Approach

The coding process began with database design using SQLite. Separate tables were created for user credentials and inventory data. Once the database schema was in place, I implemented the CRUD operations and connected them to UI elements through Java code. RecyclerView was used to display the inventory in a dynamic and responsive grid.

To handle SMS notifications, I integrated runtime permission requests and ensured the application could continue running smoothly if the user denied permission. My coding strategy emphasized building feature by feature and testing after each implementation. This incremental approach helped reduce bugs and made debugging easier.

Testing Process

Testing was conducted using the Android Emulator. I tested login validation with both valid and invalid credentials, created new accounts, and ensured persistence by closing and reopening the app. I also tested CRUD functionality in the grid by adding, updating, and deleting items. For SMS notifications, I tested both granting and denying permission to verify the app’s behavior in both cases.

This process was essential to confirm the app worked under different scenarios and to reveal edge cases, such as attempting to log in with incorrect credentials or adding items with missing fields.

Challenges and Innovation

One challenge was ensuring the app handled denied SMS permissions gracefully. By designing fallback behavior, I made sure the user experience was not disrupted even without SMS alerts. Another challenge was implementing the database logic in a way that kept the app responsive. Using RecyclerView with targeted updates rather than full refreshes was an innovative choice that improved performance and usability.

Strengths and Successes

A particularly successful component of this project was the login and account creation system. By implementing proper validation against the database and providing account creation for first-time users, the app met the critical requirement of secure user access. Another strength was the integration of CRUD operations in the inventory grid, which demonstrated my knowledge of RecyclerView, database interaction, and dynamic UI design.
