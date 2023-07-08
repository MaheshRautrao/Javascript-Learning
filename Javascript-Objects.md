# Javascript Objects

- It is a common practice to declare objects with the const keyword.

- Objects are mutable: They are addressed by reference, not by value. <br>
  If person is an object, the following statement will not create a copy of person: <br>
  const x = person;  // Will not create a copy of person. <br>
  The object x is not a copy of person. It is person. Both x and person are the same object. <br>
  Any changes to x will also change person, because x and person are the same object <br>

- The delete operator should not be used on predefined JavaScript object properties. It can crash your application.
- JavaScript objects inherit the properties of their prototype.<br>
   The delete keyword does not delete inherited properties, but if you delete a prototype property, it will affect all objects inherited from the prototype.

- |In an object method, this refers to the object.|
  |-----------------------------------------------|
  | Alone, this refers to the global object.|
  | In a function, this refers to the global object.|
  |In a function, in strict mode, this is undefined.|
  | In an event, this refers to the element that received the event.|
  | Methods like call(), apply(), and bind() can refer this to any object.|

- You access an object method with the following syntax: <br>
  objectName.methodName()
- If you access the methodName property, without (), it will return the function definition:
- and if you use it with () it will execute.

- JavaScript can secure better data quality when using getters and setters.
- It is considered good practice to name constructor functions with an upper-case first letter.
- In a constructor function this does not have a value. It is a substitute for the new object. The value of this will become the new object when a new object is created.
- Only modify your own prototypes. Never modify the prototypes of standard JavaScript objects.
- In javascript maps the key is an object (apples), not a string ("apples"):

- A function expression can be stored in a variable:
  const x = function (a, b) {return a * b};
  ```
       const x = function (a, b) {return a * b};
       let z = x(4, 3);
  ```
- Functions defined using an expression are not hoisted.
- Function expressions can be made "self-invoking". <br>
     (function () {
      let x = "Hello!!";  // I will invoke myself
    })();
- Arrow functions are not hoisted. They must be defined before they are used.
- Using const is safer than using var, because a function expression is always constant value.
- If a function is called with missing arguments (less than declared), the missing values are set to undefined.
- ES6 allows function parameters to have default values. myFunction(x, y = 10) {}
