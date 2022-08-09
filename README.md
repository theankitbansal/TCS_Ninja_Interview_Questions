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

