# C-operators-lab

                                                                                                                 Day => 1 
__________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________

1) Write a c program to swap two number without using 3rd variable input as a =10; b=20; output as a=20; b=10;

#include<stdio.h>

void main(){
    int a =10, b=20;
      
    a = a+b;
    b= a-b;
    a = a-b;
    printf("a=%d b=%d", a, b);
  
}
=====================================================================================================================

2) Write a c program to swap two number with using 3rd variable input as a =10; b=20; output as a=20; b=10;

#include<stdio.h>

void main(){
 int a =10, b=20, c ;
 c=a;
 a=b;
 b=c;
 printf("a=%d b=%d", a,b);
  
}

=====================================================================================================================

3) Write a c program to make sum of a two digit number without using "+" operator 
intput a=5, b=6
output- 11

#include<stdio.h>

void main(){
int a=10, b=20;
printf("sum is without using + operator: %d", a-(-b));

}

=====================================================================================================================
 
4) Write a c program to make sum of two digit number 
input n=34
output- 7

#include<stdio.h>

void main(){
 int n=34, a,b;
 a=n%10;
 b=n/10;
 printf("value of sum: %d",a+b);
}

_____________________________________________________________________________________________________________________________
_____________________________________________________________________________________________________________________________                      
                                                                                                                          
                                                                                                                    Day => 2

1) Write a c program to previous multiple of 10 given 2 digit number only.
------
sample input : int a=26
sample output: 20

#include<stdio.h>

void main(){
    int n =98;
    n=n/10;
    printf("%d",n*10);

}

=====================================================================================================================
2) Write a c program to next multiple of 10 given 2 digit number only.
input : 34
outut : 40

#include<stdio.h>

void main(){
    int n =26;
    n=n%10;
    printf("%d",n*10);

}

=====================================================================================================================



3) Without using control statement write a c program to determine the next or previous multiple of 10 for a given two-digit number.
--------------
conditon-
if the last digit of given number is greater than or equal to 5, the program should print the next multiple of 10.

if the last digit of given number is less than 5 the program should print the previous multiple of 10..


sample input1 : int a=34;
sample output : 30

sample input2 : int a=25
output2: 30

sample input3 : int a=86
output3: 90

#include<stdio.h>

void main(){
    int n =25,rem;
    rem = n%10;
    n= n/10;
    rem>=5 && printf("%d",(n+1)*10) || n<5 && printf("%d", n*10);
 
    // printf("%d", ((a%10)/5 + a/10)*10);
}

=====================================================================================================================



4) Write a c program to check and print that given number is even or odd without using ternary operator and control statement.
-------------

sample input: int a=10
sample output : Even

sample input : int a=125
sample output : Odd

#include<stdio.h>

void main(){
    int a=3;
    a%2==0 && printf("Even") || printf("odd");
}

=====================================================================================================================



5) Write a c program to find maximam number among two number without using ternary operator and control satements 
-------

Sample input : int a=10, b=20;
Sample output : 20

#include<stdio.h>

void main(){
    int a=2,b=2;
    a>b && printf("a is big") || b>a && printf("b is big") || printf("both are equal"); 
}

__________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________
                                         
                                                                                                            Day- 3


1) Add 1st and Last

Write a c program to take input of 3 digit number from the user , and add the 1st digit and last digit of that given number
input :- 345
output :- 8

#include <stdio.h>
 
void main()
{
   int n,t,sum;
   printf("Enter a three digit number: ");
   scanf("%d", &n);
   t = n%10;
   sum = t;
   n= n/10;
   t= n/10; 
   sum = sum + t;
   printf("%d", sum); 
}

=====================================================================================================================

2) Write a program to take input for seconds from the user , And convert it into Hour, Minutes , Second format.

Enter the number of seconds: 3671

3671 seconds is equivalent to 
1 hours
 1 minutes
 and 11 seconds.

#include<stdio.h>
int main(){
    int seconds = 0;
    int minutes = 0;
    int hours = 0;

    printf("Enter the seconds: ");
    scanf("%d", &seconds);

    hours = seconds / 3600;

    minutes = (seconds - 3600) / 60;

    seconds = (seconds - 3600 - 60);

    printf("%d hours\n %d minutes\n %d seconds", hours, minutes, seconds);
}

=====================================================================================================================

3) Write a C program to convert temperature from Fahrenheit to Celsius.

C= (F - 32) * (5.0 / 9.0)


Input as :

Enter temperature in Fahrenheit: 100

Expected output:

100.00 Fahrenheit is 37.78 Celsius.

#include<stdio.h>
int main(){
    float fahrenheit = 0;
    float celsius = 0;

    printf("Enter the fahrenheit: ");
    scanf("%f", &fahrenheit);

    celsius = (fahrenheit - 32) * (5.0 / 9.0);

    printf("%.2f fahrenheit is %.2f celsius.", fahrenheit, celsius);
}

=====================================================================================================================

4) Write a C program to convert a lowercase character to uppercase take the lowercase character and convert into in a uppercase

Input as :

Enter a lowercase character: u

Expected output :

Uppercase equivalent: U
--------------------------------------------

#include<stdio.h>

void main(){
    char lower, upper;
    printf("Enter a charcter: ");
    scanf("%c", &lower);
    upper = lower - 32;
    printf("%c",upper);
}

=====================================================================================================================


5) Write a  c Program to find the biggest number among three numbers. without using loops and control flow statement

Ex:- 1

input :- 10 20 30

output:- 30


Ex:- 2

input :- 100 20 340

output:- 340

----------------------------------------

#include<stdio.h>

void main(){
    int a,b,c;
    printf("enter the value of a , b, c: ");
    scanf("%d%d%d", &a, &b, &c);
    a>b && a>c && printf(" it is big number %d",a) || 
    b>a && b>c && printf(" it is big number %d", b)||
    c>a && c>b && printf(" it is big number %d",c) ;

}
__________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________
                                                                                                                                 Day - 4

1) Program:
Sum of Natural Number
Description:
Write a C program to calculate the sum of natural numbers from 1 to a given positive integer by the user,take the input from the user by using scanf(). 
Constraints:
SampleInput:
Input as :

Enter a positive integer: 10
SampleOutput:
Expected output:

The sum of natural numbers from 1 to 10 is: 55
Explanation:
Develop it without using loops.
---------------------------------------------------------------------------

#include<stdio.h>

void main(){
    int n,sum;
    printf("Enter a number: ");
    scanf("%d",&n);
    sum = n*(n+1)/2;
    printf("value of sum: %d",sum);
}

=====================================================================================================================

2)Program:
Convert Centimeter to Inches
Description:
Write a program that takes input from the user, take some input for centimeter and convert that into inches .
Constraints:
SampleInput:
1 
SampleOutput:
0.3937
Explanation:
By using the formula.

----------------------------------------------------------------------

#include<stdio.h>

void main(){
    int cen ;
    float inch;
    printf("Enter a num: ");
    scanf("%d",&cen);

    inch = cen * 0.3937 ;
    printf("%.4f", inch);
    
}

=====================================================================================================================

3)Program:
ASCII Sum
Description:
Write a C program to take two character input from the user and print the ASCII value of that two character and display its sum.
Constraints:
SampleInput:
Enter a character: a b

SampleOutput:
ASCII value of a is : 97

ASCII value of b is : 98

ASCII sum of a & b is : 195
Explanation:
Not Required
----------------------------------------------------------------

#include<stdio.h>

void main(){
 char a, b;
 printf("Enter a two character: ");
 scanf("%c %c",&a, &b);
 printf("ASCII value of a: %d\n",a);
  printf("ASCII value of a: %d\n",b);
 printf("ASCII sum of a & b is : %d",a+b);
}

=====================================================================================================================

4) Program:
Area of Different Shape
Description:
Write a C program that takes 2 number as input and store that number in a variable, First input for radius of a Circle and 2nd input for side of a Square.
Constraints:
SampleInput:
Enter radius of Circle : 12

Enter side of Square : 5
SampleOutput:
Area of Circle is : 452.16

Area of Square is : 25
Explanation:
calculate the area of Circle and Square by using the formula.
---------------------------------------------------------------------------------------------

#include<stdio.h>

int main(){
    int radius, side, square;
    float area;

    printf("Enter radius of Circle: ");
    scanf("%d", &radius);

    printf("Enter side of square: ");
    scanf("%d", &side);

    area = 3.14 * radius * radius;
    square = side * side;

    printf("Area of Circle is: %.2f\n", area);
    printf("Area of Square is: %d\n", square);

    return 0;
}

=====================================================================================================================

5) Program:
Convert days in Y-M-D
Description:
Write a program in C to input number of days. Find and display number of years, weeks, months and days.
Constraints:
SampleInput:
Input as : 390
SampleOutput:
Output as : 1 Year, 3 Weeks, 0 Month, 4 Days
Explanation:
By using the operator.
--------------------------------------------------------------------------------

#include <stdio.h>

int main() {
    int days, years, months, weeks, remaining_days;

    
    printf("Enter the number of days: ");
    scanf("%d", &days);


    years = days / 365;
    days = days % 365;

    
    months = days / 30;
    days = days % 30;

    
    weeks = days / 7;

    
    remaining_days = days % 7;

    
    printf("Years: %d\n", years);
    printf("Months: %d\n", months);
    printf("Weeks: %d\n", weeks);
    printf("Days: %d\n", remaining_days);

    return 0;
}

__________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________
                                         
                                                                                                                           Day- 5

1) Program:1
Calculate simple interest
Description:
Create a program that takes the principal amount, interest rate, and time in years from the user and calculates the simple interest. Print the result with appropriate messages.
Constraints:
SampleInput:
principal amount: 4000



interest rate (in percentage): 5



time in years: 3
SampleOutput:
Simple Interest is: 600.00
Explanation:
By using the formula.

-------------------------------------------------------

#include<stdio.h>

int main(){
    int time;
    float pa, ir, simpleInterest;

    printf("Enter principal amount interest rate and time in year: "); 
    scanf("%f %f %d",&pa, &ir,&time);
    float irp = ir/100;

    simpleInterest = pa * irp * time;
    printf("Simple Interest is %.2f",simpleInterest);
  
    return 0;
}

=====================================================================================================================
2) Program:
Find Even or Odd
Description:
Write a C program to find the given number is even or odd. Take the input from the console by using scanf().
Constraints:
SampleInput:
Enter a number : 12

Enter a number : 13

SampleOutput:
12 is an Even number.

13 is an Odd number.
Explanation:
Don't use any control flow statement or ternary operator.

---------------------------------------------------------------------------------------------------

#include<stdio.h>

int main(){
    int num1,num2  ;
    printf("Enter a number\n");
    scanf("%d %d",&num1,&num2);

    num1%2 == 0 && printf("%d is Even number.",num1) || printf("%d is an odd number", num1);
    num2%2 == 0 && printf("%d is Even number.", num2) || printf("%d is an odd number", num2);
}

=====================================================================================================================

3)Program:
Split the Bill
Description:
Write a program that takes the total bill amount and the number of people from the user. Calculate and print the amount each person needs to pay, assuming an equal split of the bill.
Constraints:
SampleInput:
Input :

-------

total bill( in float) ->1200.00

number of people(in int)-> 5
SampleOutput:
Output :

--------

amount each person needs to pay ->240
Explanation:
Note : you have to print the msg as it is shown in the example.

------------------------------------------------------------------------------------------

#include<stdio.h>
int main(){
    float Totalbill;
    int Numberofpeople;
    scanf("%f%d",&Totalbill,&Numberofpeople);
    printf("Amount each person needs to pay - >%.0f",Totalbill/Numberofpeople);
    return 0;
}

=====================================================================================================================
4)  Welcome to Tasty Treats Cafe: Bill Calculator

Develop below scenario program and take all the input from the user by using scanf().



Title: "Tasty Treats Cafe: Bill Calculator"



Introduction:

Welcome to Tasty Treats Cafe! We provide a delightful selection of beverages and snacks to satisfy your cravings. Today, you are our esteemed customer, and we are eager to serve you! Let's calculate your bill based on your preferences.



Question:

How many cups of tea, cups of coffee, and biscuits would you like to order?


=====================================================================================================================                            

                                                                                                              Day = 6
1)  Program 1:
Profit and Loss Calculator
Description:
You are tasked with creating a C program to calculate the profit and loss for a given transaction using the following formulas. Take the cost price and selling price from the user by using scanf().



Profit (P) = Selling Price (SP) - Cost Price (CP)

Loss (L) = Cost Price (CP) - Selling Price (SP)

Profit Percentage (PP) = Profit * 100 / cost Price

Loss Percentage (LP) = Loss * 100 / cost Price

Write a C program that prompts the user for the Cost Price (CP) and the Selling Price (SP) of an item. Calculate and display the profit or loss, as well as the corresponding profit percentage or loss percentage based on the provided formulas.



Your program should:



Prompt the user to enter the Cost Price (CP) and Selling Price (SP) as input.



Calculate the profit (P) or loss (L) based on the given formulas.



Calculate the profit percentage (PP) or loss percentage (LP) based on the given formulas.



Display the calculated profit or loss, as well as the profit percentage or loss percentage.
Constraints:
SampleInput:
Read the following input from user

Cost Price: [CP]

Selling Price: [SP]

Profit/Loss: [P/L]

Profit Percentage: [PP]%

Loss Percentage: [LP]%
SampleOutput:
Cost Price: 1500

Selling Price: 1800

Profit/Loss: [calculatedProfitOrLoss]

Profit Percentage: [calculatedProfitPercentage]%

Loss Percentage: [calculatedLossPercentage]%
Explanation:
Not Required

-----------------------------------------------------------------------------
#include <stdio.h>

int main()
{
    float costPrice, sellingPrice, profit_Percentage, loss_percentage;
    float profit=0;
    float loss =0;

    printf("Enter cost price: ");
    scanf("%f", &costPrice);

    printf("Enter sellingPrice: ");
    scanf("%f", &sellingPrice);

    profit = sellingPrice - costPrice ;
    loss =    costPrice - sellingPrice;

    printf("profit=%.2f\nloss=%.2f\n", profit, loss);

    profit_Percentage = profit * 100 / costPrice;
    loss_percentage = loss * 100 /costPrice;

   printf("Profit Percentage= %.2f\nLoss Percentage= %.2f",profit_Percentage, loss_percentage);
}

                                                             OR
                                                         -----------
#include<stdio.h>
int main () {

  int  sellingprice ,costprice ,Profit, loss ,profitpercentage, losspercentage;

  printf("Enter a selling price (sp)");
  scanf("%d",&sellingprice);

  printf("Enter a cost price (cp)");
  scanf("%d",&costprice);

Profit = sellingprice - costprice;

loss = costprice - sellingprice;

profitpercentage = Profit * 100 / costprice;

losspercentage  = loss * 100 / costprice;

printf("selling price: %d\n",sellingprice);
printf("cost price: %d\n",costprice);
printf("profit: %d\n",Profit);
printf("loss : %d\n",loss);
printf("profit percentage:%d\n",profitpercentage);
printf("loss percentage :%d",losspercentage);

return 0;


}


=====================================================================================================================
2) Program  2:
Cycle Selling Price Calculator
Description:
Rohan purchased an old cycle for Rs. 1200 and spent Rs. 250 on repairs, Rs. 350 on coloring, and added new accessories worth Rs. 500. Rohan wants to make a profit of Rs. 1500 on selling the cycle.



Write a C program that calculates and displays the selling price of the cycle based on the given information.



Your program should:



Declare and initialize variables for the following costs:



costPrice: The initial cost of the cycle (Rs. 1200)

repairCost: The cost of repairs (Rs. 250)

coloringCost: The cost of coloring (Rs. 350)

accessoriesCost: The cost of new accessories (Rs. 500)

desiredProfit: The desired profit (Rs. 1500)

Calculate the total cost by adding up all the costs.



Calculate the selling price by adding the total cost and the desired profit.



Display the individual costs (cost price, repair cost, coloring cost, accessories cost, and desired profit) along with the calculated selling price.

Constraints:
SampleInput:
costPrice: The initial cost of the cycle (Rs. 1200)

repairCost: The cost of repairs (Rs. 250)

coloringCost: The cost of coloring (Rs. 350)

accessoriesCost: The cost of new accessories (Rs. 500)

desiredProfit: The desired profit (Rs. 1500)

Calculate the total cost by adding up all the costs.
SampleOutput:
Display the individual costs (cost price, repair cost, coloring cost, accessories cost, and desired profit) along with the calculated selling price.

Explanation:
Take the Required input from user.


_________________________________________________________
#include<stdio.h>
int main () {

  int costprice, repaircost, coloringcost,accessoriescost,desiredprofit , totalcost;


  printf("The initial cost of the cycle =");
  scanf("%d",&costprice);
  printf(" The cost of repairs =");
  scanf("%d",&repaircost);
  printf(" The cost of coloring =");
  scanf("%d",&coloringcost);
  printf(" The cost of new accessories  =");
  scanf("%d",&accessoriescost);
   printf(" The desired profit =");
  scanf("%d",&desiredprofit);

  int sellingprice = costprice+repaircost+ coloringcost+accessoriescost+desiredprofit;

  totalcost= sellingprice-desiredprofit;

  printf("cost price:Rs.%d\n",costprice);
  printf("repair cost:Rs. %d\n",repaircost);
  printf("coloring cost:Rs. %d\n",coloringcost);
  printf("new accessories cost :Rs.%d\n",accessoriescost);
  printf("desired profit:Rs.%d\n",desiredprofit);
  printf("selling price:Rs.%d\n",sellingprice);
  printf("total cost:Rs. %d\n",totalcost);

}

=====================================================================================================================

Program 3:
Surface Area Of Cylinder
Description:
Write a C program to find the surface area of a cylinder.Take the height and radius as a input from the user by using scanf().



The surface area of a cylinder can be calculated using the formula:



A = 2PIr^2 + 2PIrh



Find the surface area and print the radius, height and also the surface area.

Constraints:
SampleInput:
Enter the radius of the cylinder: 5
Enter the height of the cylinder: 10
SampleOutput:
Radius: 5.00
Height: 10.00
Surface Area: 471.24
Explanation:
use the formula
==============================================

solve :

#include<stdio.h>
int main () {

  float radius, height, surfacearea;

  printf("Enter the radius of the cylinder:");
  scanf("%f",&radius);

  printf("Enter the height of the cylinder :");
  scanf("%f",&height);

  surfacearea = 2 * 3.14159 * radius*radius  + 2 * 3.14159 * radius * height;

 printf("Radius: %.2f\n", radius);
 printf("Height: %.2f\n", height);
 printf("Surface Area: %.2f\n", surfacearea);

    return 0;
}

================================================================================================================================================

                                                                       Day = 7

1) Bitwise Operators
ead 2 numbers(a,b) from user using scanf and perform below operations and print output.

Bitwise Operators

1) a & b

2) a | b

3) a ^ b

4) ~a 

5) a << 1
-------------------------------------------------------------------------

#include<stdio.h>

int main(){
    int a;
   int  b;

   printf("Enter a and b value: \n");
   scanf("%d %d",&a, &b);

   printf("a & b = %d\n", a & b);
   printf("a | b = %d\n", a | b);
   printf("a ^ b = %d\n", a ^ b);
   printf("~a = %lu\n",  ~a );
   printf("a << 1 = %d\n", a<<1);
   printf("a >> 1 = %d\n", a>>1);

    return 0;
}

=====================================================================================================================

2) Operation Using Scanf Function
 Write a C program that takes two integers and operator (+,-,*,/) as input from the user using scanf and perforom calculates their sum, substraction, multiplication, and division.
-------------------------------------------------------------
#include <stdio.h>

int main() {
    int num1, num2;
    char operator;

    printf("Enter 1st number: ");
    scanf("%d", &num1);
    printf("Enter 2nd number: ");
    scanf("%d", &num2);
    printf("Enter operator (+,-,*,/): ");
    scanf(" %c", &operator);

    
    int addition = (operator == '+') && printf("addition = %d\n", num1 + num2);
    int subtraction = (operator == '-') && printf("subtraction = %d\n", num1 - num2);
    int multiplication = (operator == '*') && printf("multiplication = %d\n", num1 * num2);
    int division = (operator == '/') && (num2 != 0) && printf("division = %d\n", num1 / num2);
    int division_error = (operator == '/') && (num2 == 0) && printf("Error: Division by zero is not allowed.\n");
    int invalid_operator = !(operator == '+' || operator == '-' || operator == '*' || operator == '/') && printf("Error: Invalid operator.\n");

    return 0;
}

=====================================================================================================================

3) Relational Operators
read 2 numbers(x,y) from user using scanf and perform below operations and print output.

Relational Operators

1) x==y

2) x!=y

3) x>y

4) x<y

5) x>=y

6) x<=y
------------------------------------------------------------


#include<stdio.h>

int main(){
    int x;
   int  y;

   printf("Enter x xnd y vxlue: \n");
   scanf("%d %d",&x, &y);

   printf("x == y = %d\n", x == y);
   printf("x != y = %d\n", x != y);
   printf("x > y = %d\n", x > y);
   printf("x<y = %lu\n",  x<y );
   printf("x >= 1 = %d\n", x>=1);
   printf("x <= 1 = %d\n", x<=1);

    return 0;
}

=====================================================================================================================
4) read 2 numbers(a,b) from user using scanf and perform below operations and print output.

Assignment Operators

1) a += b

2) a -= b

3) a *= b

4) a /= b

5) a %= b
-----------------------------------------------------------------
#include<stdio.h>

int main(){
    int a;
   int  b;

   printf("Enter a and b value: \n");
   scanf("%d %d",&a, &b);

   printf("a += b = %d\n", a += b);
   printf("a -= b = %d\n", a -= b);
   printf("a *= b = %d\n", a *= b);
   printf("a/=b = %lu\n",  a/=b );
   printf("a %% b = %d\n", a%1);

    return 0;
}
=====================================================================================================================

5) takes details of an employee from the user
Write a program that takes details of an employee from the user, including name, employee ID, designation, and salary. Then, print the details of the employee.


#include<stdio.h>
int main()
{
    char Name[20],Designation[50];
    int ID , Salary;
    printf("Enter employee Name: ");
    scanf("%s",Name);
    printf("Enter employee ID: ");
    scanf("%d",&ID);
    printf("Enter employee Designation:");
    scanf("%s",Designation);
    printf("Enter employee Salary:");
    scanf("%d",&Salary);

    printf("Employee Details\n");
    printf("Name: %s\n",Name);
    printf("Employee ID: %d\n",ID);
    printf("Designation: %s\n",Designation);
    printf("Salary:$ %d\n",Salary);
       return 0;
}
=====================================================================================================================

6) Logical Operators
read 2 numbers(a,b) from user using scanf and perform below operations and print output.



Logical Operators

1) a && b

2) a || b

3) !a

4) !b
--------------------------------------------------------------------------
#include<stdio.h>
int main(){
    int a;
    int b;
    printf("Enter a and b: ");
    scanf("%d %d", &a, &b);
    printf("\n");

    printf("a && b = %d\n", a && b);
    printf("a || b = %d\n", a || b);
    printf("!a = %d\n", !a);
    printf("!b = %d\n", !b);

    return 0;
}


================================================================================================================================================================================================================================================================================================
