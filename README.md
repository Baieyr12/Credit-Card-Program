Computer Science 1 : Java Programming
Dr. David Cline
Program 3: Credit Cards
Being able to control the flow of a program is an important skill. It allows a running program to
customize behavior based on user input or data values. This program is designed to get you working
with control flows by means of "if" statements. Hopefully, it will also start you thinking about the
dangers of credit card debt.
Things you will learn
• If statements
• Nested if statements
• Dealing with Strings and real-valued inputs.
• Handling simple error conditions
• Formatting output
Specification
A credit card company currently has three member levels: Regal, Preferred, and Standard. Each credit
card has a different interest rate:
• VIP member: 1.1% per month
• Elite member: 1.7% per month
• Standard member: 2.0% per month
If VIP level customer makes a late payment, then their interest rate for the month increases by 1%.
Thus, if a VIP member is late, then his interest rate increases from 1.1% to 2.1% for the month.
If an Elite or Standard level customer is late on a payment, their rate increases by 1% as well. In
addition, they are assessed an extra $40 penalty for being late.
For this assignment, you will write a program that calculates the minimum monthly payment for a
credit card customer, which we will define as 2.5% of the principle plus any interest and fees. You will
also need to calculate the percentage of the payment that goes to the principle, and percentage that goes
to Interest and fees. This is given by
percentToPrinciple = 100 * (paymentToPrinciple / totalPayment)
percentToInterest = 100 - percentToPrinciple
In addition, you will have to read in the name of the customer and their credit card level (regal,
preferred, or standard).
Sample Usage:
> java CreditCard
Credit Card program by <Your Name>

Customer name: Marge Simpson
Customer member level: standard
Current balance: 500
Was the payment made late?: Yes
Bill for Standard customer Marge Simpson
Card Balance: $500.00
Interest rate for late payment: 3.0% per month
Late fee: $40.00
Minimum payment to principle: $12.50
Minimum total payment: $67.50
Percent to principle: 18.5%
Percent to interest and fees: 81.5%
> java CreditCard
Credit Card program by <Your Name>

Customer name: Monty Burns
Customer member level: VIP
Current balance: 5000
Was the payment made late?: No
Bill for Regal customer Monty Burns
Card Balance: $5000.00
Interest rate: 1.1% per month
Minimum payment to principle: $125.00
Minimum total payment: $180.00
Percent to principle: 69.4%
Percent to interest: 30.6%
Directions
1. Write the CreditCard.java program as specified above. Make sure to ask the user for the four
inputs, and format the output as shown in the examples.
2. Format money values so that they start with a $ and have 2 digits after the decimal point. You
can use System.out.printf to do this. For percents, print one digit after the decimal point.
3. If any level is given other than the three levels defined above, the program should generate an
error message and exit. Your program must accept upper and lower case for the different credit
card levels. You can do this by using the "equalsIgnoreCase" method of String.
4. Keep in mind that you need to handle 6 cases—3 cutomer levels, and for each of them, whether
the payment was made late. You also need to be able to handle the case where an invalid
customer level is entered.
5. Write your program according to the standards in codingStandardsHandout.pdf.
1. Make sure to include the block comment at the top with your name, section number, etc.
2. Make sure that your program prints out a line stating your name when it starts.
3. Also, make sure to indent properly and name variables according to the coding standard.
6. After you get your program to work on your own machine, transfer it to CSX, and compile and
run it there.
7. Once you have verified that your program compiles and runs from the command line, turn in
your source code to D2L. STOP: Have you made sure that (1) your program runs from the
command line, that (2) it prints your name when it starts, and (3) that it follows the class coding
standards?
Things to keep in mind
• You can use System.out.printf to make sure that the right number of digits are printed after the
decimal point.
• After your program has read in the level, it should use the .equals method of the String class to
compare the different customer levels
 if(level.equals(VIP_LEVEL))
 {
 ...
}
 else if(...)
{
 ...
}
...
Point Breakdown (20 points total)
The program compiles on command line Required for non-zero score
Proper indentation and spacing 4 pts
Including a proper header comment 4 pts
The program prints your name 4 pts
The program asks for proper inputs 4 pts
The program prints the right output 4 pts
As always, keep in mind that your program must compile and run from the command line or it
will get a score near 0, even if it fulfills some of the other requirements.
