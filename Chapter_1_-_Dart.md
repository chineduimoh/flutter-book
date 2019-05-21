# Chapter 1 - Dart
 Dart is a purely object-oriented, new language in the C tradition, designed to be familiar to the vast majority of programmers. This Hello World example shows how familiar Dart syntax is -
 

    main(){
      print('Hello World'); 
    } 

 Unless you have an unsound background in programming and computer science in general you should be familiar with this code and it should be self explanatory. As we move along together we will of course elaborate on the above example and more interesting ones. 
 
  With that been said, this book is intended as a tutorial for programmers with basic knowledge of programming, the reader is expected to have the basic knowledge  of the concept of programming and computer science in general so cheer up take your time learn the concept and feel free to come back to any concept you don't remember at any time.
  
 This book will give u a solid introduction to the dart language and also the frame work called flutter, flutter is an open-source mobile development framework created by google, it is used to develop applications for android and iOS, flutter is also the primary method of creating applications for google fuchsia.

##   **Comments**

 Before we begin, in computer programming, a comment is a programmer-readable explanation or annotation in the source code of a computer program. They are added with the purpose of making the source code easier for humans to understand, and are generally ignored by compilers and interpreters. Comments are used for various purpose -
 

- To provide information about project, variable, or an operation
- Let the compiler or interpreter to not execute the commented code.

There are three main types of Dart comments -


1. DO format comments (Single Line comment)
2. Block Comments (Multi Line Comment)
3. Doc Comments 
## How To Write Comments In Dart

As we have three different comment types in Dart. We have different ways to write these comments.


- Do format comment (//This is a single line comment)
- Block comment (/*………*/)
- Doc comment (///Lets doc it) 

Note: When you use doc comments in place of regular comments it gives you the power of dart-doc. It finds the relevant information and generates the documentation for it.
With all that being said let's dive into dart.

## **Variables**

  Data type means type of data that can be represented and manipulated in a programming language. Variables act as "storage locations" for those data in a program. They are a way of naming information for later usage. In dart variables can store data of different types, and different data types can be used to do different things. Just like in javascript you can use the var keyword to define variables.
Example:

     main(List<String> args){
     var number = 42;
     var name = 'Kenny_io';
     var salary = 150434.65;
     var isMarried = false;
    }

 In Dart 2, unlike javascript, once a type is assigned you cant reassign a value with new type to the variable. The data type is automatically Inferred from the right hand side. You can also assign values to variables by explicitly providing the types of data as shown below -
 

    main(List<String> args){
     int number = 42;
     String name = 'Kenny_io';
     double salary = 150434.65;
     bool isMarried = false;
    }

 If you don't intend to change the value assigned to a variable, then you can declare it with a final or a const - 


    main(List<String> args) {
      final int number = 42;
      const String name = 'Kenny_io';
    }

 
 The difference between a final and a const variable is that const variables must have a value during compile time for example  const PI = 3.14; whereas variables that are final can only be assigned once, they don't need to be assigned during compile time and can be assigned during runtime.

## **Built In Data Types**

 In computer science and computer programming, a data type or simply type is an attribute of data which tells the compiler or interpreter how the programmer intends to use the data. Dart provides all the basic data types that you can expect from a modern language like -

## Numbers

 in dart programming language numbers come in two flavours integers and double, integers and double are a subset of numbers.Integers are whole numbers while doubles are numbers with decimal point.
 

     //Assigning an integer
    int x = 100;
    
    //Assigning a double 
    double y = 1.1;
## String

 String represents a sequence of characters. For example if you want to store some data like name, address, country name, etc. Then you can use string data type, you can use single or double quotes for embed string. We will discover more about strings in dedicated post.
 

     //Assigning a string
    string name = 'kenny_io';
## Booleans

  For Boolean values, Dart has a type named bool. A Dart Boolean allows two variables either 1 or 0 or true or false. Here 1 is for true and 0 is for false.
  

    void main() {
    bool istrue = true;
    bool isfalse = false;
    print(istrue); // returns true
    print(isflase); // returns false
    }
## List

 Declaring a list is very simple, use can simple use square brackets [] to define a list. Below are some common operations on a list. A list index starts from 0 so in the list below 1,2,3,4 has an index of 0,1,2,3 respectively -
 

    main(List<String> args) {
      var list = [1,2,3,4];
     
      print(list); //Output: [1, 2, 3, 4]
      //Length
      print(list.length);
     
      //Selecting single value
      print(list[1]);    //Output: 2
     
      //Adding a value
      list.add(10);
     
      //Removing a single instance of value
      list.remove(3);
     
      //Remove at a particular position
      list.removeAt(0);
    }

If you want to define a List that is compile time constant i.e. the content of lists are unchangeable then use the const keyword.


    main(List<String> args) {
      var list = const [1,2,3,4];    //Cannot alter elements of this list
    }


## Maps

A map is an object that associates keys and values, defining maps is equally straight forward. Use the curly brackets { } to define a map.


    main(List<String> args) {
      var map = {
        'key1': 'value1',
        'key2': 'value2',
        'key3': 'value3'
      };
     
      //Fetching the values
      print(map['key1']);    //Output: value1
      print(map['test']);    //Output: null
     
      //Add a new value
      map['key4'] = 'value4';
      
      //Length  
      print(map.length);
     
      //Check if a key is present
      map.containsKey('value1');
     
      //Get entries and values
      var entries = map.entries;
      var values = map.values;
    }

You can also define a map using the Map constructor, we will cover constructors later in this chapter.


    main(List<String> args) {
      var squares = new Map();
      squares[4] = 16;
    }

If you want to define a Map that is compile time constant i.e. the content of map are unchangeable then use the const keyword.


    main(List<String> args) {
      var squares = const {    //Cannot change the content of this map
        2: 4,
        3: 9,
        4: 16,
        5: 25
      };
    }

That is all for data-types lets move on to operators.

## **Dart Operators**

 An expression is a special kind of statement that evaluates to a value. Every expression is composed of an operand (represents the data) and an operator (defines how the operand will be processed to produce a value). Consider the following expression "2 + 3". In the expression,2 and 3 are operands and the symbol "+" (plus) is the operator. We will discuss the operators that are available in Dart.

##  Arithmetic Operator

 Dart supports the usual arithmetic operator, as shown in the table below. 

| Operator | Meaning                                              | Example                                     |
| -------- | ---------------------------------------------------- | ------------------------------------------- |
| +        | Add                                                  | assert(2 + 3 == 5);                         |
| -        | Subtract                                             | assert(2 - 3 == -1);                        |
| *        | Multiply                                             | assert(2 * 3 == 6);                         |
| /        | Divide                                               | assert(5 / 2 == 2.5); // Result is a double |
| %        | Modulo(returns the remainder of an integer division) | assert(5 % 2 == 1); // Remainder            |

Dart also supports both increment and decrement operators.

| Operator | Meaning   | Example                                                                                              |
| -------- | --------- | ---------------------------------------------------------------------------------------------------- |
| ++       | Increment | var a, b;<br>a = 0;<br>b = a++; // Increment a AFTER b gets its value.<br>assert(a != b); // 1 != 0  |
| --       | Decrement | var a, b;<br>a = 0;<br>b = a--; // Decrement a AFTER b gets its value.<br>assert(a != b); // -1 != 0 |

## Equality And Relational Operator

The following table lists the meaning of equality and relational operators.

| Operator | Meaning                  | Example         |
| -------- | ------------------------ | --------------- |
| ==       | Equal                    | assert(2 == 2); |
| !=       | Not equal to             | assert(2 != 3); |
| >        | Greater than             | assert(3 > 2);  |
| <        | Less than                | assert(2 < 3);  |
| >=       | Greater than or equal to | assert(3 >= 3); |
| <=       | Less than or equal to    | assert(2 <= 3); |


To test whether two objects x and y represent the same thing, use the == operator. (In the rare case where you need to know whether two objects are the exact same object, use the identical() function instead). Here is how the == operator works - 

1.  If x or y is null, return true if both are null, and false if only one is null.
2. Return the result of the method invocation x.==(y). (That is right, operators such as == are methods that are invoked on their first operand. You can even override many operators, including ==, as you'll see in Overridable operators.)
## Type Test Operator

 These operators are best for checking types at runtime. There are two type-test operator.

##  is

 Returns true if the object has the specified type for example.

     void main() { 
       int n = 2; 
       print(n is int); 
    }//This will output True
## is!

Returns false if the object has the specified type for example.

    void main() { 
       double  n = 2.20; 
       var num = n is! int; 
       print(num); 
    }//This will output False


## Assignment Operator

The table below shows the assignment operators available in dart.

| Operator                    | Meaning                                                                                          | Example                                         |
| --------------------------- | ------------------------------------------------------------------------------------------------ | ----------------------------------------------- |
| =(simple assignment)        | Assigns values from the right side operand to the left side operand                              | C = A + B will assign the value of A + B into C |
| +=(Add and Assignment)      | It adds the right operand to the left operand and assigns the result to the left operand         | C += A is equivalent to C = C + A               |
| -=(Subtract and Assignment) | t subtracts the right operand from the left operand and assigns the result to the left operand   | C -= A is equivalent to C = C – A               |
| *=(Multiply and Assignment) | It multiplies the right operand with the left operand and assigns the result to the left operand | C *= A is equivalent to C = C * A               |
| /=(Divide and Assignment)   | It divides the left operand with the right operand and assigns the result to the left operand    | C /= A is equivalent to C = C / A               |

## Logical Operators

 Logical operators are used to join two or more conditions. Logical operators return a Boolean value. There are three types of logical operators.

| Operator | Meaning                                                                            | Example                      |
| -------- | ---------------------------------------------------------------------------------- | ---------------------------- |
| && And   | The operator returns true only if all the expressions specified return true        | (A > 10 && B > 10) is False. |
| || OR    | The operator returns true if at least one of the expressions specified return true | (A > 10 || B > 10) is True   |
| ! NOT    | The operator returns the inverse of the expression’s result                        | !(A > 10) is True.           |

## Conditional Expressions

 Dart has two operators that let you evaluate expressions that might otherwise require if-else statements -

-  **condition ? expr1 : expr2** : If condition is true, then the expression evaluates expr1 (and returns its value); otherwise, it evaluates and returns the value of expr2.

Example:

    EX: void main() { 
       var a = 10; 
       var res = a > 12 ? "value greater than 10":"value lesser than or equal to 10"; 
       print(res); 
    } 

The output is -

    value lesser than or equal to 10


- **expr1 ?? expr2** :If expr1 is non-null, returns it value; otherwise, evaluates and returns the value of expr2.

Example:

    EX: void main() { 
       var a = null; 
       var b = 12; 
       var res = a ?? b; 
       print(res); 
    } 

The output is -

    12


## **Dart Loops**

 Looping in programming languages is a feature which facilitates the execution of a set of instructions/functions repeatedly while some condition evaluates to true. In dart loop represents a set of instructions that must be repeated. Most of the time , certain instructions require repeated execution. Loops are an ideal way to do the same.  In a loop’s context, a repetition is termed as an iteration. Loops can be classified into definite and indefinite - 

## Definite Loop

A loop whose number of iterations are definite/fixed is termed as a definite loop. Types of definite loop are.

-  For loop :The for loop is an implementation of a definite loop. The for loop executes the code block for a specified number of times. It can be used to iterate over a fixed set of values, such as an array.

Example:

    void main() { 
       var num = 5; 
       var factorial = 1; 
       
       for( var i = num ; i >= 1; i-- ) { 
          factorial *= i ; 
       } 
       print(factorial); 
    } 

The output is -

    120


- For…in loop :The  for...in loop is used to loop through an object's properties.

Example:

    void main() { 
       var obj = [12,13,14]; 
       
       for (var prop in obj) { 
          print(prop); 
       } 
    }

The output is -

    12
    13
    14


## Indefinite Loop

An indefinite loop is used when the number of iterations in a loop is indeterminate or unknown. Types of indefinite loops are -

- While loop :The while loop executes the instructions each time the condition specified evaluates to true. In other words, the loop evaluates the condition before the block of code is executed.

Example:

    void main() { 
       var num = 5; 
       var factorial = 1; 
       
       while(num >=1) { 
          factorial = factorial * num; 
          num--; 
       } 
       print("The factorial  is ${factorial}"); 
    }

The above code uses a while loop to calculate the factorial of the value in the variable num. The output is -

    the factorial is 120


- Do while loop :The do…while loop is similar to the while loop except that the do...while loop doesn’t evaluate the condition for the first time the loop executes.

Example:

    void main() { 
       var n = 10; 
       do { 
          print(n); 
          n--; 
       }
       while(n>=0); 
    }  // the output is '10 9 8 7 6 5 4 3 2 1 0'

The output is -

    10
    9
    8
    7
    6
    5
    4
    3
    2
    1
    0


## Loop Control Statement

 In dart loop has control statement -

- **break statement**:The break statement is used to take the control out of a construct. Using break in a loop causes the program to exit the loop. Following is an example of the break statement.

Example:

    void main() { 
       var i = 1; 
       while(i<=10) { 
          if (i % 5 == 0) { 
             print("The first multiple of 5  between 1 and 10 is : ${i}"); 
             break ;    
             //exit the loop if the first multiple is found 
          } 
          i++; 
       }
    }

The above code prints the first multiple of 5 for the range of numbers within 1 to 10. The output is -

    The first multiple of 5 between 1 and 10 is: 5

 If a number is found to be divisible by 5, the if construct forces the control to exit the loop using the break statement. The following output is displayed on successful execution of the above code.


- **continue statement** :The continue statement skips the subsequent statements in the current iteration and takes the control back to the beginning of the loop. Unlike the break statement, the continue statement doesn’t exit the loop. It terminates the current iteration and starts the subsequent iteration.

Example:

    void main() { 
       var num = 0; 
       var count = 0; 
       
       for(num = 0;num<=20;num++) { 
          if (num % 2==0) { 
             continue; 
          } 
          count++; 
       } 
       print(" The count of odd values between 0 and 20 is: ${count}"); 
    }

The output is -

    The count of odd values between 0 and 20 is: 10

 In dart we can use label to control the flow. A label is simply an identifier followed by a colon (:) that is applied to a statement or a block of code. A label can be used with break and continue to control the flow more precisely.
 
 Line breaks are not allowed between the ‘continue’ or ‘break’ statement and its label name. Also, there should not be any other statement in between a label name and an associated loop. 
 
 Example:label with break

     void main() { 
       outerloop: // This is the label name 
       
       for (var i = 0; i < 5; i++) { 
          print("Innerloop: ${i}"); 
          innerloop: 
          
          for (var j = 0; j < 5; j++) { 
             if (j > 3 ) break ; 
             
             // Quit the innermost loop 
             if (i == 2) break innerloop; 
             
             // Do the same thing 
             if (i == 4) break outerloop; 
             
             // Quit the outer loop 
             print("Innerloop: ${j}"); 
          } 
       } 
    } 

The following output is displayed on successful execution of the above code -

    Innerloop: 0
    Innerloop: 0
    Innerloop: 1
    Innerloop: 2
    Innerloop: 3
    Innerloop: 1
    Innerloop: 0
    Innerloop: 1
    Innerloop: 2
    Innerloop: 3
    Innerloop: 2
    Innerloop: 3
    Innerloop: 0
    Innerloop: 1
    Innerloop: 2
    Innerloop: 3
    Innerloop: 4

Example:label with continue

    void main() { 
       outerloop: // This is the label name 
       
       for (var i = 0; i < 3; i++) { 
          print("Outerloop:${i}"); 
          
          for (var j = 0; j < 5; j++) { 
             if (j == 3){ 
                continue outerloop; 
             } 
             print("Innerloop:${j}"); 
          } 
       } 
    }

The following output is displayed on successful execution of the above code -

    Outerloop: 0 
    Innerloop: 0 
    Innerloop: 1 
    Innerloop: 2 
    
    Outerloop: 1 
    Innerloop: 0 
    Innerloop: 1 
    Innerloop: 2 
    
    Outerloop: 2 
    Innerloop: 0 
    Innerloop: 1 
    Innerloop: 2 


## **Dart Functions**

 A function is a block of organised, reusable code that is used to perform a single, related action. Functions provide better modularity for your application and a high degree of code reusing. A function declaration tells the compiler about a function's name, return type, and parameters, while a function definition provides the actual body of the function.

## Defining A Function

 A function definition specifies what and how a specific task would be done. Before using a function, it must be defined. The syntax for defining a standard function is given below -

      void function_name() { 
       //statements 
    }

Note:The void keyword indicates that the function does not return any value to the caller.
Example:

    test() { 
       //function definition 
       print("function called"); 
    }
## Calling A Function

 A function must be called to execute it. This process is termed as function invocation. The following example illustrates how a function can be invoked −
 Example:

     void main() { 
       test(); 
    }  
    test() { 
       //function definition 
       print("function called"); 
    } 

The output is -

    function called
## Returning Function

Functions may also return value along with the control, back to the caller. Such functions are called as returning functions. The return_type can be any valid data type and can also be void to return nothing to the caller, the data type of the value returned must match the return type of the function.
Example:

    void main() { 
       print(test()); 
    }  
    String test() { 
       // function definition 
       return "hello world"; 
    }

The output is -

    hello world
## Parameterised Function

Parameters are a mechanism to pass values to functions. Parameters form a part of the function’s signature. The parameter values are passed to the function during its invocation. Unless explicitly specified, the number of values passed to a function must match the number of parameters defined.
Note:It is mandatory to pass values to required parameters during the function call.
Example:

    void main() { 
       test_param(123,"this is a string"); 
    }  
    test_param(int n1,String s1) { 
       print(n1); 
       print(s1); 
    } 

The above code snippet declares a function test_param with two parameters namely, n1 and s1 -

1. It is not mandatory to specify the data type of the parameter. In the absence of a data type, the parameters type is determined dynamically at runtime.
2. The data type of the value passed must match the type of the parameter during its declaration. In case the data types don’t match, the compiler throws an error.

The output is -

    123
    This is a string
## Recursive Dart Functions

Recursion is a technique for iterating over an operation by having a function call to itself repeatedly until it arrives at a result. Recursion is best applied when you need to call the same function repeatedly with different parameters from within a loop.
Example:

    void main() { 
       print(factorial(6));
    }  
    factorial(number) { 
       if (number <= 0) {         
          // termination case 
          return 1; 
       } else { 
          return (number * factorial(number - 1));    
          // function invokes itself 
       } 
    }

The output is -

    720
## Lambda Functions

Lambda functions are a concise mechanism to represent functions. These functions are also called as Arrow functions.
Example:

    void main() { 
       printMsg(); 
       print(test()); 
    }  
    printMsg()=>
    print("hello"); 
    
    int test()=>123; // returning function

The output is -

    hello 123


## **Dart Interfaces**

 An interface defines the syntax that any entity must adhere to. Interfaces define a set of methods available on an object. Dart does not have a syntax for declaring interfaces. Class declarations are themselves interfaces in Dart.

 Classes should use the implements keyword to be able to use an interface. It is mandatory for the implementing class to provide a concrete implementation of all the functions of the implemented interface. In other words, a class must redefine every function in the interface it wishes to implement. The syntax for implementing an interface is -

     class identifier implements interface_name

Example:

    void main() { 
       ConsolePrinter cp= new ConsolePrinter(); 
       cp.print_data(); 
    }  
    class Printer { 
       void print_data() { 
          print("__________Printing Data__________"); 
       } 
    }  
    class ConsolePrinter implements Printer { 
       void print_data() {  
          print("__________Printing to Console__________"); 
       } 
    }

The output is -

    __________Printing to Console__________


## Implementing Multiple Interfaces

 A class can implement multiple interfaces. The interfaces are separated by a comma. The syntax for the same is given below −

     class identifier implements interface-1,interface_2,interface_4…

Example:How to implement multiple interfaces in dart 

      void main() { 
       Calculator c = new Calculator(); 
       print("The gross total : ${c.ret_tot()}"); 
       print("Discount :${c.ret_dis()}"); 
    }  
    class Calculate_Total { 
       int ret_tot() {} 
    }  
    class Calculate_Discount { 
       int ret_dis() {} 
    }
    class Calculator  implements Calculate_Total,Calculate_Discount { 
       int ret_tot() { 
          return 1000; 
       } 
       int ret_dis() { 
          return 50; 
       } 
    }

It should produce the following output respectively -

    The gross total: 1000 
    Discount:50 


## **Dart Classes**

 Dart is an object-oriented language. It supports object-oriented programming features like classes, interfaces, etc. A class in terms of OOP is a blueprint for creating objects. A class encapsulates data for the object. Dart gives built-in support for this concept called class.

##  Declaring a Class

Use the class keyword to declare a class in Dart. A class definition starts with the keyword class followed by the class name; and the class body enclosed by a pair of curly braces. The syntax for the same is given below −

    class class_name {  
       <fields> 
       <getters/setters> 
       <constructors> 
       <functions> 
    }

The class keyword is followed by the class name. The rules for identifiers must be considered while naming a class. A class definition can include the following −

- **Fields**: A field is any variable declared in a class. Fields represent data pertaining to objects.
- **Setters and Getters** − Allows the program to initialise and retrieve the values of the fields of a class. A default getter/ setter is associated with every class. However, the default ones can be overridden by explicitly defining a setter/ getter.
- **Constructors** − responsible for allocating memory for the objects of the class.
- **Functions** − Functions represent actions an object can take. They are also at times referred to as methods.

These components put together are termed as the data members of the class.
Example:Declaring a class

       // field 
       String engine = "E1001";  
       
       // function 
       void disp() { 
          print(engine); 
       } 
    }

The example above declares a class Car. The class has a field named engine. The disp() is a simple function that prints the value of the field engine.

## Creating Instance of the class

To create an instance of the class, use the new keyword followed by the class name. The syntax for the same is given below −

    var object_name = new class_name([ arguments ])

 

- The new keyword is responsible for instantiation.
-  The right-hand side of the expression invokes the constructor. The constructor should be passed values if it is parameterised.

Example:Instantiating a class

    var obj = new Car("Engine 1")


## Accessing Attributes and Functions

A class’s attributes and functions can be accessed through the object. Use the ‘.’ dot notation (called as the period) to access the data members of a class.

    //accessing an attribute 
    obj.field_name  
    
    //accessing a function 
    obj.function_name()

Example: Take a look at the following example to understand how to access attributes and functions in Dart −

    void main() { 
       Car c= new Car(); 
       c.disp(); 
    }  
    class Car {  
       // field 
       String engine = "E1001";  
       
       // function 
       void disp() { 
          print(engine); 
       } 
    }

The output is -

    E1001
## Dart Constructor

Dart provides named constructors to enable a class define multiple constructors. The syntax of named constructors is as given below −

    Class_name.constructor_name(param_list)

Example:

    void main() {           
       Car c1 = new Car.namedConst('E1001');                                       
       Car c2 = new Car(); 
    }           
    class Car {                   
       Car() {                           
          print("Non-Parameterised constructor invoked");
       }                                   
       Car.namedConst(String engine) { 
          print("The engine is : ${engine}");    
       }                               
    }

The output is -

    The engine is : E1001 
    Non-Parameterised constructor invoked


## The This Keyword

The this keyword refers to the current instance of the class. Here, the parameter name and the name of the class’s field are the same. Hence to avoid ambiguity, the class’s field is prefixed with the this keyword. The following example explains the same −
Example:

    void main() { 
       Car c1 = new Car('E1001'); 
    }  
    class Car { 
       String engine; 
       Car(String engine) { 
          this.engine = engine; 
          print("The engine is : ${engine}"); 
       } 
    } 

The output is -

    The engine is : E1001
## Dart Class - Getters and Setters

 Getters and Setters, also called as accessors and mutators, allow the program to initialise and retrieve the values of class fields respectively. Getters or accessors are defined using the get keyword. Setters or mutators are defined using the set keyword.

A default getter/setter is associated with every class. However, the default ones can be overridden by explicitly defining a setter/ getter. A getter has no parameters and returns a value, and the setter has one parameter and does not return a value.

    Defining a getter -
    Return_type  get identifier 
    { 
    } 
    
    Defining a setter -
    set identifier 
    { 
    }

 
 Example: The following example shows how you can use getters and setters in a Dart class −

     class Student { 
       String name; 
       int age; 
        
       String get stud_name { 
          return name; 
       } 
        
       void set stud_name(String name) { 
          this.name = name; 
       } 
       
       void set stud_age(int age) { 
          if(age<= 0) { 
            print("Age should be greater than 5"); 
          }  else { 
             this.age = age; 
          } 
       } 
       
       int get stud_age { 
          return age;     
       } 
    }  
    void main() { 
       Student s1 = new Student(); 
       s1.stud_name = 'MARK'; 
       s1.stud_age = 0; 
       print(s1.stud_name); 
       print(s1.stud_age); 
    } 

The output is -

    Age should be greater than 5 
    MARK 
    Null 
## Class Inheritance

 Dart supports the concept of Inheritance which is the ability of a program to create new classes from an existing class. The class that is extended to create newer classes is called the parent class/super class. The newly created classes are called the child/sub classes.
 
 A class inherits from another class using the ‘extends’ keyword. Child classes inherit all properties and methods except constructors from the parent class.
Note:Dart doesn’t support multiple inheritance.
Example:

    oid main() { 
       var obj = new Circle(); 
       obj.cal_area(); 
    }  
    class Shape { 
       void cal_area() { 
          print("calling calc area defined in the Shape class"); 
       } 
    }  
    class Circle extends Shape {}

The output is -

    calling calc area defined in the Shape class

 In the above example, we are declaring a class Shape. The class is extended by the Circle class. Since there is an inheritance relationship between the classes, the child class, i.e., the class Car gets an implicit access to its parent class data member.

##  Types Of Inheritance

Inheritance can be of the following three types −

1. **Single**: Every class can at the most extend from one parent class.
2. **Multiple**: A class can inherit from multiple classes. Dart doesn’t support multiple inheritance.
3. **Multi-level**: A class can inherit from another child class.

Example:

    void main() { 
       var obj = new Leaf(); 
       obj.str = "hello"; 
       print(obj.str); 
    }  
    class Root { 
       String str; 
    }  
    class Child extends Root {}  
    class Leaf extends Child {}  
    //indirectly inherits from Root by virtue of inheritance

The class Leaf derives the attributes from Root and Child classes by virtue of multi-level inheritance. The output is as −

    hello
## The Static Keyword

The static keyword can be applied to the data members of a class, i.e., fields and methods. A static variable retains its values till the program finishes execution. Static members are referenced by the class name.
Example:

    class StaticMem { 
       static int num;  
       static disp() { 
          print("The value of num is ${StaticMem.num}")  ; 
       } 
    }  
    void main() { 
       StaticMem.num = 12;  
       // initialize the static variable } 
       StaticMem.disp();   
       // invoke the static method 
    }

The output is -

    The value of num is 12
## The Super Keyword

The super keyword is used to refer to the immediate parent of a class. The keyword can be used to refer to the super class version of a variable, property, or method. The following example illustrates the same −
Example:

    void main() { 
       Child c = new Child(); 
       c.m1(12); 
    } 
    class Parent { 
       String msg = "message variable from the parent class"; 
       void m1(int a){ print("value of a ${a}");} 
    } 
    class Child extends Parent { 
       @override 
       void m1(int b) { 
          print("value of b ${b}"); 
          super.m1(13); 
          print("${super.msg}")   ; 
       } 
    }

The output is -

    value of b 12 
    value of a 13 
    message variable from the parent class


## **Dart Object**

 Object-Oriented Programming defines an object as “any entity that has a defined boundary.” An object has the following −

1. **State**: Describes the object. The fields of a class represent the object’s state.
2. **Behaviour**: Describes what an object can do.
3. **Identity :** A unique value that distinguishes an object from a set of similar other objects. Two or more objects can share the state and behaviour but not the identity.

The period operator (.) is used in conjunction with the object to access a class’ data members.
Example:

    class Student { 
       void test_method() { 
          print("This is a  test method"); 
       } 
       
       void test_method1() { 
          print("This is a  test method1"); 
       } 
    }  
    void main()    { 
       Student s1 = new Student(); 
       s1.test_method(); 
       s1.test_method1(); 
    }

The output is -

    This is a test method 
    This is a test method1

 Dart represents data in the form of objects. Every class in Dart extends the Object class. Given above is a simple example of creating and using an object.

## The Cascade Operator(..)

 The above example invokes the methods in the class. However, every time a function is called, a reference to the object is required. The cascade operator can be used as a shorthand in cases where there is a sequence of invocations.

The cascade ( .. ) operator can be used to issue a sequence of calls via an object. The above example can be rewritten in the following manner.
Example:

    class Student { 
       void test_method() { 
          print("This is a  test method"); 
       } 
       
       void test_method1() { 
          print("This is a  test method1"); 
       } 
    }  
    void main() { 
       new Student() 
       ..test_method() 
       ..test_method1(); 
    }

The output is -

    This is a test method 
    This is a test method1
## The toString() Method

his function returns a string representation of an object. Take a look at the following example to understand how to use the toString method.
Example:

    void main() { 
       int n = 12; 
       print(n.toString()); 
    } 

The output is -

    12


## **WHY DART IS USED FOR FLUTTER**

 Flutter has a couple of language requirement -

- AOT and JIT compilation for fast reload and fast released code.
- A good garbage collector to clean up after creating and destroying many objects.
- Single threaded to avoid locks and therefore jank.
- An arm compiler to avoid having another engine running the code on the device (aka React Native).

 Dart meets all these requirements. JS (I think) meets all the above pretty closely too, apart from the AOT and JIT compiler part. Saying all of that I can imagine that a JS solution could happen but it might be costly and a more complicated solution. Dart is pretty good and Dart2 has really improved things with inherent type safety. So lets dive into flutter and explore the framework and begin our mobile app journey.

