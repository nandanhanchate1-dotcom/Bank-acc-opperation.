# Bank-acc-opperation.

💰 BankAccount SMS Notification System (with Twilio)

This Python script simulates a basic banking system where users can deposit and withdraw money from their account. Upon each operation, the system sends an SMS notification to the user's phone using the Twilio API.

📜 Features

Custom Exception Handling: Uses a custom exception InvalidAccountError to handle invalid operations like overdrafts or negative deposits.

SMS Notifications: Automatically sends an SMS for every successful or failed transaction.

Twilio Integration: Uses twilio.rest.Client to send messages to the user’s phone.

User Interaction: Takes input from the user for deposit and withdrawal operations.

🧾 Class & Function Overview
InvalidAccountError

A custom exception class for invalid account operations such as:

Insufficient funds

Invalid deposit amounts

BankAccount

Represents a simple bank account.

Attributes:

account_number: Account identifier

balance: Current account balance

phone_number: User’s phone number (used for SMS alerts)

account_sid, auth_token, twilio_number: Twilio credentials

Methods:

send_sms(message): Sends an SMS via Twilio

withdraw(amount): Withdraws money and sends SMS. Raises InvalidAccountError if funds are insufficient.

deposit(amount): Deposits money and sends SMS. Raises InvalidAccountError for non-positive deposits.

🔄 Workflow

User is prompted to enter a withdrawal amount.

If the amount is valid, the balance is updated, and an SMS is sent.

User is prompted to enter a deposit amount.

If valid, the balance is updated, and an SMS is sent.

Any custom exceptions are caught and displayed, along with SMS alerts
