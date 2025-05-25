# Banking-Management-System
This is a basic Bank Account Management System implemented in Java. It demonstrates the use of encapsulation, static members, and basic banking operations such as deposit and withdrawal.

📌 Features
Auto-incrementing accountId for every new account.

Secure deposit and withdrawal functionality with balance checks.

Encapsulated account data (name, ID, balance).

Method to display account details.

🛠️ Technologies Used
Java (Standard Edition)

No external dependencies

📁 Class Overview
java
Copy
Edit
public class Account {
    private static int idCounter = 1001;
    private int accountId;
    private String customerName;
    private double balance;

    // Constructor
    public Account(String customerName, double initialDeposit) { ... }

    // Deposit method
    public void deposit(double amount) { ... }

    // Withdraw method
    public boolean withdraw(double amount) { ... }

    // Show account details
    public void showDetails() { ... }

    // Getters
    public int getAccountId() { ... }
    public double getBalance() { ... }
}
🚀 How to Use
Create a new account:

java
Copy
Edit
Account acc = new Account("Alice Johnson", 500.0);
Deposit money:

java
Copy
Edit
acc.deposit(150.0);
Withdraw money:

java
Copy
Edit
if (acc.withdraw(200.0)) {
    System.out.println("Withdrawal successful.");
} else {
    System.out.println("Insufficient balance.");
}
Display account details:

java
Copy
Edit
acc.showDetails();
🧾 Sample Output
yaml
Copy
Edit
Account ID: 1001
Customer Name: Alice Johnson
Balance: $500.0
📚 Concepts Demonstrated
Encapsulation: All fields are private and accessed through public methods.

Static Variables: idCounter ensures each account has a unique ID.

Object-Oriented Programming: Each Account is an independent object with its own state and behavior.
