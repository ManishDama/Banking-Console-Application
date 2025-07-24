<h2>EasyBank Console</h2><br>
A modular console-based banking system built with Java that simulates core banking operations like
account creation, deposit, withdrawal, and balance checking. This project leverages object-oriented
programming principles and JDBC for seamless integration with a MySQL database.

<h4>Features</h4>
- Account creation with unique ID
- Deposit and withdrawal operations
- Balance inquiry<br>
- Command-line interface for smooth user interaction
- MySQL integration using JDBC
- Modular and maintainable OOP-based architecture

<h4>Technologies Used</h4>
- Java Core programming language<br>
- JDBC (Java Database Connectivity) For connecting Java with MySQL<br>
- MySQL Database to persist account and transaction data<br>
- OOP (Object-Oriented Programming) For clean modular structure<br>

<h4>Prerequisites</h4>
- Java JDK 8 or above
- MySQL Server
- Any IDE (e.g., IntelliJ IDEA, Eclipse)
- JDBC driver for MySQL

<h4>Steps to Run</h4>
1. Clone the Repository<br>
     - git clone https://github.com/your-username/BankingSystem.git<br>
2. Set up the MySQL Database<br>
      - Create the database and table using the schema.sql script provided.<br>
3. Update JDBC Config in DBConnection.java<br>
        String url = "jdbc:mysql://localhost:3306/banking_db";<br>
        String username = "root"; // your MySQL username<br>
        String password = "your_password";<br>
4. Compile and Run<br>
        - Use your IDE or terminal to compile and run Main.java<br>


<h4>OOP Design Overview – org.connection Package</h4>
The org.connection package is responsible for managing the database connection layer of your banking system. It follows key object-oriented principles such as abstraction, encapsulation, modularity, and interface-driven development.

<h4>OOP Design Overview – org.customer.Customer Class</h4>
The Customer class is a core part of your banking system that models a bank customer. It encapsulates the customer's identity and validation logic, demonstrating strong object-oriented programming principles.

<h4>Package: org.exception</h4>
Custom exceptions that make the system domain-aware and more descriptive when handling errors.
    <h5>PhoneNumberLenthMisMatchException extends Exception</h5><br>
          •	Purpose: Thrown when the phone number is not exactly 10 digits.<br>
          •	OOP Benefit: Clear, domain-specific error separation instead of using generic Exception.<br>
     <h5>EmailFormatException extends Exception</h5><br>
          •	Purpose: Thrown when the email format does not match a valid pattern.<br>
          •	OOP Benefit: Better debugging and validation tracking.<br>
      <h5>AadharLengthException extends Exception</h5><br>
           (Assumed from your earlier Customer code; not shown again here)<br>
          •	Purpose: Thrown when the Aadhar number is not 12 digits.<br>


<h4>Package org.services</h4>
Each class in this package encapsulates a specific banking operation, following the Single Responsibility Principle.<br>
OpenAccount	Handles ---> new account creation	openAccount()<br>
Withdraw	Manages ---> withdrawal logic	getWithdraw()<br>
Deposit	Manages---> deposits	getDeposit()<br>
CheckBalance	Displays ---> current balance	checkBalance()<br>
•	These services likely interact with the database using connection logic from the org.connection package.<br>
•	Separation of Concerns is observed: UI input → service logic → DB layer.<br>

<h4>Sample output:</h4>
1.When you first time run the code<br>
 <img width="353" height="173" alt="image" src="https://github.com/user-attachments/assets/9f322f17-7854-44f6-bbd3-f226b5f35f82" /><br>

 
2.If you select open account option you have enter name, phone number, email, aadhar number and you will get return with a unique account number and other details like below<br>
![WhatsApp Image 2025-07-24 at 19 11 27_76d8d325](https://github.com/user-attachments/assets/0adb7385-a733-46df-833d-d564d2edc6f8)
<br>

3.If you select yes then operations will be reshowed like what you see above like<br>
 <img width="353" height="173" alt="image" src="https://github.com/user-attachments/assets/4c21fe34-31eb-4f65-8fbe-8dc463816741" /><br>

4.If you enter no you will see like<br>
 <img width="547" height="126" alt="image" src="https://github.com/user-attachments/assets/126678e2-dc6c-46cb-9fe9-a063b0a5091a" /><br>

5.want to withdraw?<br>
![WhatsApp Image 2025-07-24 at 19 14 43_caae4b28](https://github.com/user-attachments/assets/162e2bd8-5055-46d2-a895-e0fc0855b753)
<br>


6.want to diposit?<br>
![WhatsApp Image 2025-07-24 at 19 16 55_f6188f0f](https://github.com/user-attachments/assets/565a64c9-c8e9-44ba-99eb-80c7483c5a93)
<br>


7.want to check Balance?<br>
 ![WhatsApp Image 2025-07-24 at 19 17 33_ef0fe070](https://github.com/user-attachments/assets/18c4618c-e11e-49a1-9496-438b40343510)
<br>


8.Exit<br>
 ![WhatsApp Image 2025-07-24 at 19 18 11_bba1d4aa](https://github.com/user-attachments/assets/9b7dcab6-67cf-4bc0-8d99-55f79c76efa0)
<br>

