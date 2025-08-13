This is a simple secure chat application written in Java that stores messages in a local MySQL database. Messages are encrypted before storage and decrypted when retrieved, ensuring privacy.

Features
-> Send and receive chat messages locally
-> AES encryption for secure message storage
-> MySQL database backend for storing chat history

Works on any OS with Java and MySQL installed

Requirements
Java JDK 8 or later

MySQL Server installed locally

MySQL JDBC driver (mysql-connector-java.jar) in the project folder

Setup & Run Locally
Clone or download this repository to your computer.

Place mysql-connector-java.jar in the same directory as the Java files.

Create a database in MySQL (for example securechat).

Run the following in MySQL to create the chat table:

sql
Copy
Edit
CREATE TABLE messages (
    id INT AUTO_INCREMENT PRIMARY KEY,
    sender VARCHAR(50),
    receiver VARCHAR(50),
    message TEXT,
    timestamp TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
Open the Java source files and update the database details:

java
Copy
Edit
String url = "jdbc:mysql://localhost:3306/securechat";
String user = "root";
String password = "root";
Replace with your MySQL username, password, and database name.

Compile the Java files with the MySQL connector in the classpath.

Run the compiled classes and start chatting securely.
