public class Account {
    private static int idCounter = 1001;
    private int accountId;
    private String customerName;
    private double balance;

    public Account(String customerName, double initialDeposit) {
        this.accountId = idCounter++;
        this.customerName = customerName;
        this.balance = initialDeposit;
    }

    public void deposit(double amount) {
        balance += amount;
    }

    public boolean withdraw(double amount) {
        if (amount > balance) return false;
        balance -= amount;
        return true;
    }

    public void showDetails() {
        System.out.println("Account ID: " + accountId);
        System.out.println("Customer Name: " + customerName);
        System.out.println("Balance: $" + balance);
    }

    public int getAccountId() {
        return accountId;
    }

    public double getBalance() {
        return balance;
    }
}
