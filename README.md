# ChatWave

ChatWave is a real-time chatting application built using Java, JavaFX, and HTML/CSS for the UI. It allows users to communicate seamlessly by sending text messages and images, either in one-to-one chats or through group conversations. The application is backed by a MySQL database for secure and efficient storage of user data, messages, and group information.

# Features
User Authentication – Secure login with credentials

Private and Group Chat – Send text and images to individuals or groups

Broadcast Messaging – Send messages to all contacts at once

Chat History – View and load previous conversations

Contact Management – Add, delete, or block contacts

Image Sharing – Send and delete images in chats

Group Management – Create groups and chat with multiple users

Real-Time Communication – Instant messaging via TCP sockets

Robust Server Handling – Multi-client server with session and message management

Error Handling – Graceful feedback on connection, message, and authentication failures

Responsive UI – Clean, styled JavaFX interface using HTML/CSS

MySQL Integration – Stores messages, user data, and group metadata

# Project Scope
1.  Functional Scope
   
- Client-Side Features
  - User Authentication: Secure login system using username and password, with appropriate error handling.
  - Private Chat: One-to-one messaging with contacts.
  - Group Chat: Create and participate in group conversations with multiple users.
  - Broadcast Messages: Send a message to all contacts at once.
  - Add Contacts: Add other users to your contact list (only if they exist in the system).
  - Contact List Management: View, update, and manage contact lists in real time.
  - Chat History: Retrieve and display past conversations on selecting a contact.
  - Delete Messages: Support for deleting messages for self or all participants.
  - Block Users: Ability to block contacts to avoid communication.
  - Delete Contacts: Remove users from the contact list.
  - Send Images: Share images in both private and group chats, with delete functionality.
  - Responsive UI: Built using JavaFX for a clean and dynamic user experience.
  - Error Handling: Informative messages for login failures, message delivery issues, or connection problems.

- Server-Side Features
  - Multi-Client Handling: Handles multiple users concurrently using multithreading.
  - Message Routing: Routes messages to intended recipients based on socket connections.
  - User Management: Maintains connected users, active sessions, and authentication handling.
  - Message Persistence: Stores messages in a database for chat history access.
  - Connection Management: Manages online/offline status updates and disconnections.
  - Error Handling: Detects and handles issues like message delivery failures or broken connections.

- Database Features
  - User Info Storage: MySQL tables to store username, password, and email.
  - Chat History Storage: Messages saved to the database for future reference.
  - Contact List Management: Store and retrieve user contact lists.
  - Group Data Management: Save group metadata like name, members, and message logs.

2. Technical Scope
  - Programming Language: Java

  - User Interface: JavaFX for desktop-based responsive UI

  - Networking: TCP/IP sockets used for client-server communication
  
  - Database: MySQL used for persistent storage of users, contacts, messages, and groups

  - Multithreading: Server uses Java multithreading to manage simultaneous client connections

  - UI Styling: JavaFX with integrated HTML and CSS for a polished frontend appearance


# Tech Stack

  - Programming Language	:  Java (JDK 8 or above)

  - User Interface  :	JavaFX + HTML/CSS

  - Networking  :	Java Socket Programming (TCP/IP)

  - Database  :	MySQL

  - Multithreading  :	Java Thread

    
# Installation

## Prerequisites
   
  - Java Development Kit (JDK) – Version 8 or above

  - MySQL Server – Running locally or on your server

  - JavaFX SDK – Add to your classpath (if not using JDK with JavaFX bundled)

  - An IDE like IntelliJ IDEA / Eclipse / VSCode (recommended)

## Database Setup
1. Create the Database
  Open your MySQL client and run:

        CREATE DATABASE mydemo;
   
        USE mydemo;
   
2. Create Tables
  Run the following SQL commands to create the necessary tables:

        CREATE TABLE users (
   
        id INT NOT NULL AUTO_INCREMENT PRIMARY KEY,
   
        username VARCHAR(50) NOT NULL UNIQUE,
   
        password VARCHAR(255) NOT NULL,
   
        email VARCHAR(255)
        );

        CREATE TABLE contactlist (
   
        contact_id INT NOT NULL AUTO_INCREMENT PRIMARY KEY,
   
        id INT,
   
        name VARCHAR(100),
   
        user_id INT
        );

        CREATE TABLE contacts (
   
        id INT NOT NULL AUTO_INCREMENT PRIMARY KEY,
   
        sender_id INT NOT NULL,
   
        receiver_id INT NOT NULL,
   
        message VARCHAR(255) NOT NULL,
   
        timestamp DATETIME DEFAULT CURRENT_TIMESTAMP,
   
        status VARCHAR(20) DEFAULT 'sent',
   
        deleted_by_sender TINYINT(1) DEFAULT 0,
   
        deleted_by_receiver TINYINT(1) DEFAULT 0,
   
        image_path VARCHAR(255)
        );

        CREATE TABLE group_messages (
   
        message_id INT NOT NULL AUTO_INCREMENT PRIMARY KEY,
   
        group_id INT NOT NULL,
   
        user_id INT NOT NULL,
   
        message TEXT NOT NULL,
   
        timestamp DATETIME DEFAULT CURRENT_TIMESTAMP
        );

        CREATE TABLE user_groups (
   
        group_id INT NOT NULL AUTO_INCREMENT PRIMARY KEY,
   
        group_name VARCHAR(255) NOT NULL,
   
        group_members TEXT NOT NULL
       );

        CREATE TABLE blocked_users (
   
        blocker_id INT NOT NULL,
   
        blocked_id INT NOT NULL,
   
        PRIMARY KEY (blocker_id, blocked_id)
        );

5. Update your database connection credentials

        String url = "jdbc:mysql://localhost:3306/mydemo";
   
        String user = "your_mysql_username";
   
        String password = "your_mysql_password";

6. Compile and Run the Project
   
  Start the Server

        javac Server.java
        java Server
   
Make sure the server is running before starting clients.

  Start the Client
  
        javac Main.java
        java Main
  
# Demo
Here is a quick look into some of ChatWave's prominent features!

![Demo](chatwaveDemo.gif)
# Authors
K Anishka , *SSN College of Engineering , Tamil nadu , India*

Anne Jacika J , *SSN College of Engineering , Tamil nadu , India*
