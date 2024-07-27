# Project-1 Bank System  (Python)
## Summary
This project features a comprehensive system for secure money transfers and electronic payments, functioning as a bridge between the user's bank account and the payee, such as stores or service providers. It enhances security and protects funds by allowing users to create temporary accounts that are automatically deleted after each transaction. The system includes various account management operations and services.

In addition, the project includes the basic banking operations that the user needs. It allows users to create and manage accounts, handle virtual cards, deposit and transfer funds, view account information, and process transactions efficiently.

The following image illustrates the basic structure of the system:
<img src="https://github.com/AbdullahSoli/Project-1/blob/2f02bebe7f8a246162c2dde9cb1f78c37307bdea/Temp.%20Bank.png" alt="Project Overview" width="800" height="500"/>
## Features
- __Account Creation__: Create a new account with personal details and a randomly generated account number.
- __Virtual Card Management__: Generate and manage virtual card details, including card number, CVV, and expiration date.
- __Deposit and Transfer__: Deposit money into the account or transfer money to another account.
- __Display Information__: Display account and virtual card details.
- __Transaction History__: Record and display transaction history.
- __Data Persistence__: Save account and transaction data to a JSON file.
- __Account Deletion__: Delete the account and remove personal data.
## Code Description
#### _Here's a detailed explanation of the code :_ 
### Import Statements
- __random__: This library is used to generate random numbers, which are used to create unique account and card numbers.
- __datetime & timedelta__: These libraries are used to manage dates and times, such as calculating the expiration date of a virtual card.
- __os__: This library provides functions to interact with the operating system, including file and directory operations.
- __json__: This library is used to read and write JSON data, allowing for the storage and retrieval of account and transaction information.

### Global Variables
- __bank_account__: A dictionary that holds the details of a bank account, including the account holder's name, phone number, birth date, email, password, account number, balance, and transaction history.
- __transactions__: A dictionary that stores the transaction history for each account.
- __virtual_card__: A dictionary that contains the details of a virtual card, such as the card number, cardholder's name, CVV, and expiration date.
- __file_name__: A string that holds the name of the JSON file where the account data will be saved.
- __folder_path__: A string that specifies the directory path where the data files will be stored.

  ### Lambda Functions
- __balance_add__: A lambda function that adds two numbers, used for adding amounts to the account balance.
- __balance_deduct__: A lambda function that subtracts the second number from the first, used for deducting amounts from the account balance.

### Helper Functions
- __date_4_years_from_today__: This function calculates a date that is four years from the current date and returns it in the format MM/YY.
- __account_does_not_exist__: This function checks if the bank_account dictionary is empty, indicating whether an account has been created. It can operate in two modes: normal or removal.

### Core Functions
- __create_account__: This function prompts the user to enter personal details and generates a random account number. It initializes the bank_account dictionary with these details and creates a virtual card. It also saves the account data to a JSON file.
- __display_account_info__: This function prints the account details, excluding the password and transaction history.
- __create_card__: This function generates a virtual card with a random card number, CVV, and an expiration date four years from today.
- __display_card_info__: This function prints the details of the virtual card.
- __save_data__: This function creates a JSON file to store the account details, transactions, and virtual card details. It ensures the file is saved in the specified directory.
- __update_file_transactions__: This function updates the JSON file with the latest transaction data.
- __remove_data__: This function removes personal data from the JSON file, such as phone number, birth date, email, password, and balance.

### Balance Management
- __display_balance__: This function prints the current balance of the account.
- __deposit__: This function allows the user to deposit money into their account by entering an IBAN and deposit amount. It updates the account balance and records the transaction.
- __transfer__: This function allows the user to transfer money to another account by entering an IBAN and transfer amount. It checks if the user has sufficient funds, updates the account balance, and records the transaction.
### Transaction Management
- __record_transaction__: This function records deposit and transfer transactions in a specific format, including the date, transaction type, and amount.
- __show_transactions__: This function prints all recorded transactions for the account.
### Account Deletion
- __delete_account__: This function deletes the account by clearing the bank_account dictionary and removing personal data from the JSON file.
### Main Function and Program Loop
- __main__: This function provides a menu for the user to select different services, such as creating an account, depositing money, transferring money, displaying card information, displaying balance, showing transactions, displaying account information, and deleting the account.
- The program runs in an infinite loop, repeatedly displaying the menu and executing the selected service until the user chooses to exit.




### Group Member
- Salman Gassem
- Naif Ghannam
- Firas Almoqhim
- Abdullah Thabet
