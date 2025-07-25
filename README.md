# ChatWave

# Description
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

# Installation

# Demo
Here is a quick look into some of ChatWave's prominent features!

![Demo](chatwaveDemo.gif)
# Authors
K Anishka , *SSN College of Engineering , Tamil nadu , India*

Anne Jacika J , *SSN College of Engineering , Tamil nadu , India*
