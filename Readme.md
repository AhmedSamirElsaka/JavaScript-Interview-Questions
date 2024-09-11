# JavaScript Interview Questions & Answers

> Click :star: if you like the project and follow [@AhmedSamirElsaka](https://github.com/AhmedSamirElsaka) for more updates

---

### Table of Contents

<!-- TOC_START -->
| No. | Questions |
| --- | --------- |
| 1 | [What are the different data types present in javascript](#What-are-the-different-data-types-present-in-javascript)|
<!-- TOC_END -->

<!-- QUESTIONS_START -->
1. ### What are the different data types present in javascript
   ---
   1.  **Primitive types :**
      
       1. String - It represents a series of characters and is written with quotes. A string can be defined using a single or a double quote.
          
          Example :
          ```javaScript
          var str = "Ahmed Samir Elsaka"; //using double quotes
          var str2 = 'Ahmed Samir Elsaka'; //using single quotes
          ```

       2. Number - It represents a number and can be written with or without decimals.                                                                                            

          Example :                                                                          
          ```javaScript
          var x = 3; //without decimal
          var y = 3.6; //with decimal
          ```

       3. BigInt—This data type is used to store numbers above the limitation of the Number data type. It can store large integers and is represented by adding “n” to an integer literal.               

          Example :
          ```javaScript
          var bigInteger =  234567890123456789012345678901234567890;
          ```

       4. Boolean - It represents a logical entity and can have only two values : true or false. Booleans are generally used for conditional testing.
        
          Example :
          ```javaScript
          var a = 2;
          var b =  3;
          var c =  2;
          (a == b) // returns false
          (a == c) //returns true
          ```
        
       5.  Undefined - When a variable is declared but not assigned, it has the value of undefined and it’s type is also undefined.
       
           Example :
           ```javaScript
           var x; // value of x is undefined
           var y = undefined; // we can also set the value of a variable as undefined
           ```
        
       6.  Null - It represents a non-existent or a invalid value.
                                                                                                                 
           Example :
           ```javaScript
           var z = null;
           ```
        
       7.  Symbol — This is a new data type introduced in the ES6 version of Javascript. It stores an anonymous and unique value.
       
           Example :
           ```javaScript
           var symbol1 = Symbol('symbol');
           ```

        **typeof of primitive types :**
     
          ```javaScript
          typeof "Ahmed Samir" // Returns "string"
          typeof 3.14 // Returns "number"
          typeof true // Returns "boolean"
          typeof 234567890123456789012345678901234567890n // Returns bigint
          typeof undefined // Returns "undefined"
          typeof null // Returns "object" (kind of a bug in JavaScript)
          typeof Symbol('symbol') // Returns Symbol
          ```

   2. **Non-primitive types :**
      Primitive data types can store only a single value. To store multiple and complex values, non-primitive data types are used.
      Object - Used to store collection of data.
      
      Example:
      ```javaScript
      // Collection of data in key-value pairs
      var obj1 = {
         x:  43,
         y:  "Hello world!",
         z: function(){
            return this.x;
         }
      }
            
      // Collection of data as an ordered list
           
      var array1 = [5, "Hello", true, 4.1]; 
      ```
      > **Note- It is important to remember that any data type that is not a primitive data type, is of Object type in javascript.**
2. ### what is the dynamic Typing
   ---
   it means that We do not have to manually define the data type of the value stored in a variable. Instead, data types are determined automatically.

3. ### what is the types of functions and how we can define them
   1. Function declaration : Function that can be used before it’s declared
      ```javaScript
      function printName(name){
      return ("hello" + name)
      }
      ```
   2. Function expression : ssentially a function value stored in a variable
       ```javaScript
      const printName = function (name){
      return ("hello" + name)
      }
      ```
   3. Arrow function : Great for a quick one-line functions. Has no this keyword
      ```javaScript
      const printName = (name) => ("hello" + name)
      ```
      
4. ### What is an Immediately Invoked Function in JavaScript
   ---
   An Immediately Invoked Function ( known as IIFE and pronounced as IIFY) is a function that runs as soon as it is defined.

   Syntax of IIFE :
   ```javaScript
   (function(){ 
   // Do something;
   })();
   ```
   To understand IIFE, we need to understand the two sets of parentheses that are added while creating an IIFE :

   The first set of parenthesis:
   ```javaScript
   (function (){
   //Do something;
   })
   ```
   While executing javascript code, whenever the compiler sees the word “function”, it assumes that we are declaring a function in the code. Therefore, if we do not use the first set of parentheses, 
   the compiler throws an error because it thinks we are declaring a function, and by the syntax of declaring a function, a function should always have a name.

   ```javaScript
   function() {
   //Do something;
   }
   // Compiler gives an error since the syntax of declaring a function is wrong in the code above.
   ```
   To remove this error, we add the first set of parenthesis that tells the compiler that the function is not a function declaration, instead, it’s a function expression.

   The second set of parenthesis:

   ```javaScript
   (function(){ 
   // Do something;
   })();
   ```
   From the definition of an IIFE, we know that our code should run as soon as it is defined. A function runs only when it is invoked. If we do not invoke the function, the function declaration is 
   returned:
   
   ```javaScript
   (function (){
   // Do something;
   })
   // Returns the function declaration
   ```
   Therefore to invoke the function, we use the second set of parenthesis.

5. ### Explain Higher Order Functions in javascript
   ---
   Functions that operate on other functions, either by taking them as arguments or by returning them, are called higher-order functions.
   
   Higher-order functions are a result of functions being first-class citizens in javascript.

   Examples of higher-order functions:
   ```javaScript
   function higherOrder(fn) {
   fn();
   }
   higherOrder(function() { console.log("Hello world") }); 
   ```
   
   ```javaScript
   function higherOrder2() {
    return function() {
    return "Do something";
      }
    }      
    var x = higherOrder2();
    x()   // Returns "Do something"
   ``` 
   
