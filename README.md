# OOP-Assignment2-BankSystem
# Banking System

Model, design, and develop a banking application. The banking application allows the user, i.e., the bank employee, to perform various operations on bank accounts for specific clients. It supports creating bank accounts, listing all available accounts, displaying account details, withdrawing money, and depositing money.

## BankAccount Class

There are two types of bank accounts. The first type is the basic `BankAccount`, which holds the following data:

- Account ID
- Balance

The following methods apply to this class:

- Constructor: There are 2 constructors. The first sets the balance to a given value, and the second is a no-argument constructor that sets the balance to 0.
- Setters and getters: These methods allow accessing the private data fields.
- `withdraw`: It withdraws an amount of money from the account if the balance is sufficient.
- `deposit`: It deposits an amount of money into the account.

## SavingsBankAccount Class

The second type of account extends the basic `BankAccount` and may have some extra data fields and operations. It is called `SavingsBankAccount`. This account requires the user to keep a minimum amount of money in the account (minimum balance) as long as the account is open. It also requires deposits that are not less than 100 at a time. In addition to the inherited data fields, it has the following additional data field:

- `minimumBalance`: This minimum balance takes a default value of 1000 L.E.

It has the following methods plus those inherited from the parent class:

- Constructor: The constructor sets the value of the initial balance and the minimum balance. The initial balance should be greater than or equal to the minimum balance.
- Setters and getters: These methods allow accessing the private data fields.
- `withdraw`: It overrides the `withdraw` method to allow withdrawing money, but not below the minimum balance.
- `deposit`: It deposits an amount of money into the account but only if the amount is greater than or equal to 100 LE.

## Client Class

There is also a `Client` class which holds the basic information of a client, such as name, address, and phone number. It holds a pointer to the client's bank account. An account also points to its owner.

## BankingApplication Class

The main class that runs the application is `BankingApplication`. This class displays the main menu and accepts the user's choice. It maintains a list of accounts and clients. It allows the user to perform operations on a bank account.

## Team members
| Name | ID |
|------|----|
| Mohamed Essam Mahmoud Osman | 20210346 |
| Salah Eddin Mohamed Salah | 20210187 | 
| Abdelrahman Gamal Ali | 20210233 |
