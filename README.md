# TCS_Ninja_Interview_Questions
TCS Ninja Technical Interview Questions

1. Explain ACID properties in DBMS?

 In order for a database to maintain its integrity, all transactions must adhere to the ACID standard. The ACID acronym refers to atomicity, consistency, isolation, and durability, so let's discuss each of them in turn.

Atomicity: An atomic transaction data remains unchanged even after an operation is executed. This means that if an operation is undertaken on the data, either the operation must be completed or it must not be executed at all. A transaction operation should not be split between different parts or executed in stages. It must be completed entirely and not partially.
Consistency: The consistency property defines the level of how the data should be kept unchanged. By keeping the data consistent, the DBMS is not allowing any inconsistency in the data. An example of a level of consistency would be when one table contains the data on which the operation is performed while another table should contain the data before performing the operation.
Isolation: When the transactions are running concurrently, the outcome should be the same as if the transactions were running serially; that is, the result should be the same as if there were no transactions at all.
Durability: The data after an operation is successfully executed is permanent in a DBMS. To ensure the durability of data, the term durability is used. Even if the system fails or crashes, the database may survive. However, if it is lost, the responsibility of the recovery manager is to ensure its durability. Whenever we make changes to values, the COMMIT command must be used.

2. What is the DDL command in MySql explain Create and Alter command?

The Data Definition Language is a set of SQL commands designed to structure databases. It handles database schema descriptions and constructs and modifies database objects' structures in databases. In addition to data, DDL refers to a set of SQL instructions for creating, modifying, and deleting database structures. It does not handle data. Database structures are created, modified, and deleted using DDL commands. All DDL commands are auto-committed, saving all database changes permanently. DDL commands that construct the database structure include:

CREATE: A database or one of its objects is created using this command (like tables, indexes, functions, views, stored procedures, and triggers). You can issue two kinds of SQL statements: one that creates a database and another that creates a table.
Syntax:

To create Database: CREATE DATABASE db_name;

Example: CREATE DATABASE store;

To create Table: 

CREATE TABLE table_name(
Column_name1 data_type(size),
Column_name2 data_type(size),
Column_name3 data_type(size),
…..
);
Example: 

CREATE TABLE product(
Id int(10),
Name varchar(100),
Price varchar(10)
);
ALTER: The ALTER command in SQL lets us add, delete, and modify items in a table, view, or the whole database. We can also modify, add, and delete constraints, columns, and indexes using the ALTER command.
Command to add new Column: 
Syntax: ALTER TABLE table_name ADD column_name column-definition;
Example: ALTER TABLE product ADD category varchar(50);
Command to modify a Column: 
Syntax: ALTER TABLE table_name MODIFY (column-definition);
Example: ALTER TABLE product MODIFY (category varchar2(100));

3. What is the Drop and Truncate command in SQL?

DROP: You may drop a whole database or a table by using the DROP statement. Existing objects such as databases, tables, indexes, and views are destroyed with the DROP command.
Syntax: To drop a table: DROP TABLE table_name;
To drop a database: DROP DATABASE db_name;
Example:  To drop a table: DROP TABLE product;
To drop a database: DROP DATABASE store;
TRUNCATE: Used to indicate the table’s extents for deallocation (empty for reuse). This method is quicker than the usual integrity checking procedures to remove all data from a table. This procedure was introduced in the SQL:2008 standard for the first time. It is somewhat equivalent to the delete command.
Syntax: TRUNCATE TABLE  table_name;
Example: TRUNCATE TABLE product;

4. What is the JIT compiler in java?

The Just-In-Time compiler is a critical component of the Java Runtime Environment. It is primarily responsible for optimizing the efficiency of Java-based programs during runtime or execution. Bytecode is a key element of Java that allows for cross-platform execution. The Java Development Kit (JDK) includes the Java compiler (javac), which is used to compile Java source code into bytecode (.class file). The JVM then loads the .class file at runtime and converts the bytecode to binary code (machine code). The interpreter also makes use of machine code. The JIT compiler improves the performance of Java programs by translating bytecode at run time into native machine code.

5. What is the OOPs concept?

OOPs, or object-oriented programming is based on the idea of creating objects, using them repeatedly throughout the program, and then manipulating them to obtain the desired outcome.

Four basic principles of OOPS are

Abstraction.
Inheritance.
Polymorphism.
Encapsulation.

6. What is Abstraction in OOPS?

Abstraction basically means hiding the background details of a program and showing only the necessary details. Abstract classes and interfaces can be used to accomplish abstraction.To make a class abstract, we simply use the abstract keyword.

7. What are inheritance and its types in Java?

The process of inheriting features of an existing class into a new class is referred to as inheritance. There are two kinds of classes in inheritance. the class which inherits the properties of a class is called a child class, and the class from which we are inheriting is called the Base or Parent class. Extends is the keyword used for Inheritance.

Example: A Cylinder class can have properties of a Circle class and it also can have extra features.

class Circle {
 float radius;
 function area(){
  return 3.14*radius*radius;
 }
}
class Cylinder extends Circle{

 float height;
 function volume(){
  return 3.14*radius*radius*height;
 }
}
There are Three types of Inheritance in Java:

Single Inheritance: When a class is derived from another class, this is known as single inheritance.
Multilevel Inheritance: When a class is derived from a class which is also derived from another class, it is known as multi-level inheritance.
Hierarchical Inheritance: When a class has more than one parent class then it is called hierarchical inheritance.

8. What is Method Overloading?

Method overloading is a technique that is used to achieve the polymorphism. When a class has multiple methods with the same name but with different parameters or signatures then it is called method overloading.

Example: 

class Example {
 function sum(int num1, int num2){
  return num1+num2;
 }
 function sum(int num1, int num2, int num3){
  return num1+num2+num3;
 }
 function sum(float num1, float num2){
  return num1+num2;
 }
}

9. Explain Insertion sort?

Insertion Sort is a comparison-based sorting algorithm. In each iteration of insertion sort, it picks one element from the unsorted side and finds the current place for it on the sorted side of the list. It works similarly to card sorting.

It is adaptive in nature.

// Insertion sort code in Java
// This sorting algorithm will sort the array in ascending order
import java.util.Arrays;
class InsertionSort {
 void sort(int arr[]) {
   int sizeOfArray = arr.length;
   for (int i= 1; i< sizeOfArray ; i++) {
     int key = arr[i];
     int j = i- 1;
     while (j >= 0 && temp < arr[j]) {
       arr[j + 1] = arr[j];
       --j;
     }
     arr[j + 1] = temp;
   }
 }
 // Driver code
 public static void main(String args[]) {
   int[] unSortedArray = { 12, 10, 31, 4, 13 };
   InsertionSort s = new InsertionSort();
   s.sort(unSortedArray);
   System.out.println("Sorted Array: ");
   System.out.println(Arrays.toString(unSortedArray));
 }
}
Time Complexity:

The worst case of insertion sort will be when the given list is in descending order and the time complexity will be O(n^2).
The average case time complexity of the insertion sort will also be O(n^2).
The best case of Insertion Sort will be when the list is sorted in Ascending order and the time complexity will be O(n).
Space Complexity: Space complexity will be O(1).

10. What is a linked list explain with an example?

A linked list is a linear data structure. Unlike a conventional sequential data structure, a linked list maintains its elements at non-contiguous memory locations. A linked list is composed of nodes interconnected by pointers. A node in the Linked List consists of two parts: data and a pointer. The pointer points to the next node in the list.

The head always points to the first node of the linked list, and the last node will always point to null.

Example: music or video player, next and previous buttons in the browser.

Types of Linked List:

Singly Linked List.
Doubly Linked List.
Circular Linked List.

11. What is an operating system?

An OS acts as the bridge between a computer's users and its hardware. The goal of an OS is to offer a setting where a user may conveniently and effectively run a program. The distribution of services and resources, including memory, processors, hardware, and data, maybe a responsibility of an operating system. Programs sort of a traffic controller, a scheduler, a memory management module, I/O programs, and a filing system are among the operating system's programs that are responsible for managing these resources.

12. What is a firewall? How does it work?

A firewall is a network protection system that regulates internet traffic coming into, leaving, and inside a private network. Firewalls may be thought of as controlled borders or portals that control the flow of authorized and restricted web traffic in a private network. The phrase derives from the notion of physical walls acting as barriers to impede the spread of fire until emergency personnel can extinguish it. Similarly, network security firewalls are used for online traffic control, often to slow the spread of web dangers.

How a firewall works:

Based on a set of pre-established rules, a firewall system examines network traffic. Following that, it filters the traffic to stop any of that traffic from originating from untrustworthy or unreliable sources. Only inbound traffic that is set to accept is permitted.

13. What is the stack data structure and its operations?

The Last In First Out (LIFO) concept is used by stacks, which are dynamic data structures. The first thing to be removed from a stack is the last thing that was added to it. The addition and removal of items are limited in stacks. Only one end of the stack, i.e., the top, can have items added or removed. The top item is the one at the very top. Push() and pop() are the names of the operations that add and remove items, respectively.

Some common operations used on stacks include the following:

push(): Push operation is used to insert an item at the top of the stack.
pop(): Pop operation is used to remove the element from the top of the stack.
isEmpty(): This method is used to know if the stack is empty or not.
isFull(): This method is used to know if the stack is full or not.
peek(): This method returns the element at any given index in the stack.

14. What is a constructor in java?

A class's member function with the same name as the class is the constructor.

The initialization of objects belonging to a class is done by a particular kind of member function called a constructor. When an object (a class instance) is formed, the constructor is automatically invoked.

A constructor does not have a return type.

Virtual constructors are not a thing; only member functions can be virtual.

Types of Constructors in Java:

No-argument Constructor: A constructor with no parameter is called a no-argument or default constructor. If a constructor is not defined in a class then the compiler automatically creates a default constructor.
Example:
Class Interviewbit {
Int num1, num2;
    Interviewbit(){
    num1 = 20;
    num2 = 30;
    {
}
Interviewbit ib =new Interviewbit();
Parameterized Constructor: Parameterized constructors are constructors that take parameters. Use a parameterized constructor if you wish to initialize class fields with your values.
Example:
Class Interviewbit {
Int num1, num2;
    Interviewbit(int num1, int num2){
    this.num1 = num1;
    this.num2 = num2;
    {
}
Interviewbit ib =new Interviewbit();

15. Explain the TCP/IP model?

TCP/IP stands for Transmission Control Protocol/Internet Protocol. It assists us in figuring out the best way to connect a particular computer to the internet and the best way to transfer data between them. When several computer networks are linked together, we can more easily establish a virtual network. To enable communication across large distances, the TCP/IP protocol was created.

It is a connection-oriented protocol.

Layers in the TCP/IP model: There are four layers in the TCP model:

Application Layer: It manages the standards for user interfaces and is responsible for node-to-node communication.
Transport Layer: It is in charge of ensuring a seamless end-to-end connection and error-free data transfer.
Internet Layer: It specifies the protocols that control the logical transmission of data throughout the whole network.
Network Access Layer: The protocols available in this layer enable the physical transport of data while keeping an eye out for hardware addressing.

![image](https://user-images.githubusercontent.com/81725794/183565393-37bfb61b-4ce0-41b7-ae6a-0cd265525f50.png)

16. What is cloud computing?

The term "cloud computing" refers to the storage and access of data and computing services via the internet. It does not save any information on your computer. It refers to the on-demand availability of computer services such as servers, data storage, networking, and databases. The primary goal of cloud computing is to provide numerous users with access to data centers. Users can also gain access to data stored on a distant server.

Cloud computing reduces the user's hardware and software requirements. The only program that the user needs to be able to operate is the cloud computing platforms interface software, which can be as simple as a Web browser, and the Cloud network handles the rest. We have all encountered cloud computing at some point in our lives; some of the major cloud services we have used or continue to use include mail services such as Gmail, Hotmail, and yahoo, among others.

Example: AWS, Azure, Google.

17. What is Machine Learning?

Machine Learning is a collection of computer algorithms that can learn from examples and improve themselves without being explicitly programmed by a person. Machine learning is an artificial intelligence component that integrates data with statistical methods to predict an output that can be utilized to produce actionable insights. A common machine learning challenge is to make a recommendation. For individuals who have a Netflix account, all movie or series recommendations are based on the user's past data. Unsupervised learning is being used by tech companies to improve the customer experience by personalizing recommendations.

Machine learning is also utilized for tasks such as fraud detection, predictive maintenance, portfolio optimization, task automation, and so on.

TCS Ninja Coding Questions

18. Write a Program to print the Half Pyramid Number Pattern?
Pattern: 

1
22
333
4444
55555
Code:

class PyramidPattern{
   public static void main(String[] args) {
       //to control how many rows we have to print
       int noOfRows=5;
       for(int num=1;num<=noOfRows;++num){
           for(int j=1;j<=num;++j){
               System.out.print(num);
           }
           System.out.println();
       }
   }
}

We have used nested loops to print the pattern. The outer loop is used to control the no of rows we want to print and what number will be printed on each row. An inner loop is used to control the number of types that number will be printed. 

Time Complexity: O(n^2)
Space Complexity: O(1)

19. Write a program to print the left triangle start pattern?

          * 
        * * 
      * * * 
    * * * * 
  * * * * *

Code:

public class LeftTrianglePattern
{
public static void main(String[] args) {
 int i=0,noOfRows=5,j;
       for(; i<noOfRows; i++)
       { 
           //Inner loop1
           for(j=2*(noOfRows-i); j>=0; j--)
           {           
               System.out.print(" ");
           } 
           //Inner loop2
           for(j=0; j<=i; j++)
           {       
               System.out.print("* ");
           }           
           System.out.println();
       } 
}
}
An outer loop will run to control the number of rows to print. Inner loop1 will control the number of spaces before the pattern in each row. Inner loop2 will print the * in each row after the space.

Time Complexity: O(n^2)
Space Complexity: O(1)

20. Write a program to check if a number is prime or not?

A number is said to be the prime number if it is divisible by itself or 1. If the number is divisible by any other number then it is not a prime number.

Code:

public class Main {
   static boolean primeNumberChecker(int number){
       int i = 2;
       boolean flag = false;
       while (i <= number / 2) {
         //Check if number is divisible by i
         if (number % i == 0) {
           //set flag to true and breakout of the loop
           flag = true;
           break;
         }
         i++;
       }
       if (!flag)
         return true;
       else
        return false;
   }
 public static void main(String[] args) {
   int numberToCheck = 11;
   //Call the function and store the result
   boolean result = primeNumberChecker(numberToCheck);
   //Check if result is true then number is prime
   if (result)
     System.out.println(numberToCheck + " is a prime number.");
   else
     System.out.println(numberToCheck + " is not a prime number.");
 }
}
Take a boolean variable as and set it to by default false.

Start the loop from 2 because a number is always divisible by 1.

Now check if the number is divisible by any other number.

If the number is divisible by the other number then set the flag variable as true and break the loop.

Now check if a flag is true means the number is not a prime number.

Time Complexity: Loop is running only half times of number so the time complexity would be O(n).
Space Complexity: O(1)

21. Write a recursive function to print the factorial of a number?

The definition of a factor of a number n is the multiplication of all positive descending integers; the factor of n is represented by the symbol n!.

Code:

public class Factorial{
   static long factorial(int number){
      //Base condition when recursive call will stop
       if(number==0 || number == 1)
           return 1;
       return number * factorial(number-1);
   }
 public static void main(String[] args) {
   //Number to calculate factorial
   int number = 10;
  System.out.println(factorial(number));
 }
}
Time Complexity: Time complexity would be O(n).
Space Complexity: In each recursive call, it uses stack internally so space complexity would be O(n).

22. Write a program to check if there exist a duplicate key in the array?

import java.util.*;
class Duplicate {
   public static boolean checkDuplicate(int[] arr) {
       // create a hashmap to store the occurrence of the number
       Map<Integer,Integer> container = new HashMap<>();
      //Loop through the array
       for(int i=0;i<arr.length;i++){
           //Check if number already exist in the hashmap
           if(container.containsKey(arr[i])){
               return true;
           }
           else
               container.put(arr[i],1);
       }
       return false;
   }
   public static void main(String[] args){
       //Input array
       int []arr = {10,20,30,40,10};
       System.out.println(checkDuplicate(arr));
   }
}
Output:

true
To solve this problem we will use the HashMap. First, we will check if the key exists in the map or not if it exists means there is a duplicate key in the array. If the key does not exist in the array then we will put the key in the array with value 1. Keep doing this till the last element of the array.

If key exists return false otherwise return true.

Time Complexity: Time complexity would be O(n).
Space Complexity: We are using additional space to keep a count of the occurrence of each number so space complexity would be O(n).

23. Write a program to calculate the sum of diagonal of a matrix?

Include only the total of the primary diagonal elements and the secondary diagonal elements that are not a part of the primary diagonal.

class Solution {
   public static int diagonalSum(int[][] matrix) {
       int row=0,col,leftSum=0,rightSum=0,n=matrix.length;
       col=n-1;
       while(row<n){
          //Calculate sum of left diagonal
           leftSum += matrix[i][i];
           //Check if row and column are not same 
           if(row!=col)
               //Calculate the sum of right diagonal
               rightSum += matrix[i][j];
               //update row and col
           row++;
           col--;
       }
       return (leftSum + rightSum);
   }
   public static void main(String []args){
       //Input matrix
       int [][]matrix = {{10,20,30},
                     {40,50,60},
                     {70,80,90}};
       int result = diagonalSum(matrix);
       System.out.println(result);
   }
}
Output:

250
Take two variables to store the sum of the left and right diagonal.

Take two pointers row, col to traverse the matrix. If row and col are equal then we have to add that element only once either in leftSum or rightSum.

Time Complexity: O(n), as we are running a loop to n times.
Space Complexity: O(1)

24. Write a program to check if given number is palindrome or not?

When a number reads the same both forward and backward, it is a palindrome.
