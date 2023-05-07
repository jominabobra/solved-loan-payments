Download Link: https://assignmentchef.com/product/solved-loan-payments
<br>
5/5 - (9 votes)

A bank has been asked to go back and reprocess the loan payments for a car loan. A customer does not believe the bank has the correct outstanding balance for the loan.



The loan characteristics are:

a. Total amount of loan: $18,875a. Term of loan: 60 monthsa. Loan interest rate: 0%a. Remaining loan balance: $12,500

($12,500). of $18,875. The car loan is a 0% interest loan. The loan is for 60 months and the bank records indicate that the customer’s remaining balance is $12,500. The customer does not believe the bank has the correct outstanding balance for her loan.

The customer’s records indicate that the remaining loan balance is $11,427. The customer has receipts that show that 20 loan payments have been paid in the following whole dollar amounts: 315, 451, 315, 374, 353, 315, 450, 484, 412, 315, 495, 476, 321, 315, 406, 329, 326, 356, 315, 325.

First, using the following “BankAccount” class as the base class (superclass), create a “CarLoan” derived class (subclass) that extends the BankAccount class. The “CarLoan” class will use an overloaded constructor to initialize the car loan balance (using “super” in the subclass constructor to set the balance).

Second, create a text file that contains the whole dollar customer payment amount values (315, 451, 315, 374, 353, 315, 450, 484, 412, 315, 495, 476, 321, 315, 406, 329, 326, 356, 315, 325).

Finally, create a CarLoanClient class that:a. Creates a “CarLoan” class object, named “cl01”.b. Read the customer payment values from the text file, one payment at a time. Include the use of exception handling during the reading of the text file values, exception handling code, “IllegalPaymentAmountException”, that displays the following string to the user, “Invalid payment amount. Please enter valid payment amount “, and allows the user to manually enter a payment amount.c. Passes the payment values read from the text file to a method that calculates the outstanding balance. (Hint: Use the withdrawal method).d. Outputs the following for each payment amount value:– A payment sequence number, starting at “1” and ending at “20”;– The payment amount value that corresponds to the appropriate payment number, and;– The outstanding loan balance, after the application of the corresponding payment amount value.e. Processes each payment amount value Continues to process each payment amount value until the end of the file is reached.

———————————————————————————–import java.text.DecimalFormat;

public class BankAccount{public final DecimalFormat MONEY = new DecimalFormat(“$#,##0.00”);public double balance;

//Default Constructor: Sets balance to 0.0.public BankAccount(){balance = 0.0;}

/*Overloaded Constructor@param startBalance beginning balance*/public BankAccount( double startBalance ){deposit( startBalance );}

/*Accessor for Balance@return current account balance*/public double getBalance(){return balance;}

/*Deposit amount to account.@param amount amount to deposit;amount must be = 0.0*/public void deposit(double amount){if( amount = 0.0)balance += amount;elseSystem.err.println( “Deposit amount must be positive and cannot be”+ “greater than the balance.” );}

/*Withdraw amount to account.@param amount amount to withdraw;amount must be = 0.0amount must be &lt;= balance*/public void withdraw(double amount){if( amount = 0.0 &amp;&amp; amount &lt;= balance)balance -= amount;elseSystem.err.println( “Withdrawal amount must be positive and cannot ”+ ” be greater than the balance.” );}