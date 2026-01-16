package task3;


import java.util.Scanner;

class BankAccount {
    double bal;

    BankAccount(double bal) {
        this.bal = bal;
    }

    void deposit(double amount) {
        if (amount > 0) {
            bal = bal + amount;
            System.out.println("Amount deposited succesfully");
        } else {
            System.out.println("Invalid amount");
        }
    }

    void withdraw(double amount) {
        if (amount > 0 && amount <= bal) {
            bal = bal - amount;
            System.out.println("Withdrawal successful");
        } else {
            System.out.println("Insufficient balance or invalid amount");
        }
    }

    void checkBalance() {
        System.out.println("Current Balance: " + bal);
    }
}

public class ATMInterface {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        BankAccount account = new BankAccount(1000);

        boolean run = true;

        while (run) {
            System.out.println("\n1. Deposit");
            System.out.println("2. Withdraw");
            System.out.println("3. Check Balance");
            System.out.println("4. Exit");
            System.out.print("Choose option: ");

            int choice = sc.nextInt();

            if (choice == 1) {
                System.out.print("Enter amount to deposit: ");
                double amount = sc.nextDouble();
                account.deposit(amount);
            } else if (choice == 2) {
                System.out.print("Enter amount to withdraw: ");
                double amount = sc.nextDouble();
                account.withdraw(amount);
            } else if (choice == 3) {
                account.checkBalance();
            } else if (choice == 4) {
                run = false;
                System.out.println("Thank you for using ATM");
            } else {
                System.out.println("Invalid option");
            }
        }
    }
}

