# Bank Management System

## Overview

The Bank Management System is a console-based application developed in Java. This system manages bank operations for two types of customers: VIP and REGULAR. Each customer can hold two types of accounts: SAVINGS and CURRENT. The application provides functionalities to manage customers, accounts, loans, and overall bank finances.

## Features

- **Customer Management:**
    - Add new customers (VIP or REGULAR).
    - Check if a customer exists.
    - Select an existing customer to manage their accounts and loans.

- **Account Management:**
    - View and manage SAVINGS and CURRENT accounts.
    - Perform operations like checking balance, withdrawing money, depositing money, calculating interest, and viewing past transactions.

- **Loan Management:**
    - View existing loans for a customer.
    - Apply for new loans with different limits based on customer type (VIP or REGULAR).

- **Bank Overview:**
    - Print all accounts in the bank.
    - Print all loans sanctioned by the bank.
    - Calculate and print the total money currently deposited in the bank.

## Technologies

- **Programming Language:** Java

## Installation

### Prerequisites

- [Java Development Kit (JDK) 11 or later](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)
- A Java IDE (e.g., IntelliJ IDEA, Eclipse) or a text editor (e.g., VSCode)
- [Apache Maven](https://maven.apache.org/download.cgi) (optional, if using Maven for dependency management)

### Steps

1. **Clone the Repository:**

   ```bash
   git clone https://github.com/yourusername/bank-management-system.git
   cd bank-management-system
   ```

2. **Compile and Build the project:**

    If using Maven:
   ```bash
   mvn compile
   ```
   
    If not using Maven, compile the Java files manually:
    ```bash
   javac src/main/java/com/yourcompany/bankmanagement/*.java
   ```

3. **Run the Application:**

   ```bash
   java -cp target/classes com.yourcompany.bankmanagement.Main
   ```

Replace com.yourcompany.bankmanagement.Main with the fully qualified name of your main class if different.

## Usage
Upon starting the application, the console will display the main menu:

```console
Welcome to - DMI Bank

MAIN MENU - 
1. Customer
2. Get All Accounts
3. Get All Loans
4. Total Money
5. Exit

Select from the above options:
```

### 1. Customer

Now, the console will display this menu:

```console
CUSTOMER MENU -
1. Add New Customer
2. Check Existing Customers
3. Select a customer
4. Back to main menu

Select from the above options:
```

**a. Add New Customer:**

Add a customer by providing their name and type (VIP or REGULAR).

**b. Check Customer Existence:**

Get a list of existing customers in the bank.
For example:
```console
LIST OF CUSTOMERS - 
1. Anurag - VIP
2. Yash - REGULAR
3. Prashant - VIP
```

**c. Select a Customer:**

Now, the console will display this menu:

```console
DETAILS - 
Name: Anurag
Type: VIP

MENU -
1. Accounts
2. Create New Account
3. Existing loans
4. Apply for a new loan
5. Back to previous menu
Select from the above options: 
```
After choosing the customer to manage their accounts and loans, the next menu will display with the following options:

**i. Accounts:**

- **Check Balance:** View the balance of the selected SAVINGS or CURRENT account.
- **Withdraw Money:** Withdraw money within the overdraft limit (SAVINGS) or up to the overdraft limit (CURRENT).
- **Deposit Money:** Deposit money into the selected account.
- **Calculate Interest:** Compute interest for SAVINGS (1.25%) or CURRENT (0.25%) accounts.
- **Get Past Transactions:** View past transactions for the selected account.

**ii. Create a New Account:**

- **Savings Account:** Provide account number and initial balance. VIP accounts have an overdraft limit of 100,000, while REGULAR accounts have a limit of 30,000.
- **Current Account:** Provide account number, initial balance, and overdraft limit.

**iii. Existing Loans:**

View any existing loans for the selected customer.

**iv. Apply for a New Loan:**

- **VIP Customers:** Can apply for up to 6 loans, ranging from 100,000 to 5,000,000.
- **REGULAR Customers:** Can apply for up to 3 loans, ranging from 100,000 to 1,000,000.

**v. Back to Previous Menu:**

Return to the previous menu.

### 2. Get All Accounts

Print a list of all accounts present in the bank. For example:

```Example
1. Account Number - 1099
Owner - Anurag
Type - SAVING
Balance - 5000.0

2. Account Number - 1098
Owner - Anurag
Type - CURRENT
Balance - 7000.0

3. Account Number - 2011
Owner - Yash
Type - SAVING
Balance - 10000.0

4. Account Number - 5400
Owner - Yash
Type - CURRENT
Balance - 10000.0
```

### 3. Get All Loans

Print a list of all loans sanctioned by the bank. For example:

```Example
LIST OF ALL LOANS - 

1. Amount - 200000.0
Interest Rate - 12.5
By - Yash

2. Amount - 300000.0
Interest Rate - 12.5
By - Yash
```

### 4. Total Money in the Bank

Calculate and print the total money currently deposited in the bank. For example:
```Example
Total Money in the bank - Rs.32000.0
```

### 5. Exit

Exit the application.