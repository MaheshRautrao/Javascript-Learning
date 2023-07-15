# JavaScript Callbacks

```
 "I will call back later!"

A callback is a function passed as an argument to another function

This technique allows a function to call another function

A callback function can run after another function has finished
```

## Function Sequence

JavaScript functions are executed in the sequence they are called. Not in the sequence they are defined.

## JavaScript Callbacks

A callback is a function passed as an argument to another function.

Example
```
function myDisplayer(some) {
  document.getElementById("demo").innerHTML = some;
}

function myCalculator(num1, num2, myCallback) {
  let sum = num1 + num2;
  myCallback(sum);
}

myCalculator(5, 5, myDisplayer);
```

# Asynchronous JavaScript

``` "I will finish later!"

Functions running in parallel with other functions are called asynchronous

A good example is JavaScript setTimeout()
```
In the real world, callbacks are most often used with asynchronous functions. <br>

A typical example is JavaScript setTimeout(). <br> 

## Waiting for a Timeout

When using the JavaScript function setTimeout(), you can specify a callback function to be executed on time-out: <br>

```
Example
setTimeout(myFunction, 3000);

function myFunction() {
  document.getElementById("demo").innerHTML = "I love You !!";
}
```
Note : 
```
When you pass a function as an argument, remember not to use parenthesis.

Right: setTimeout(myFunction, 3000);

Wrong: setTimeout(myFunction(), 3000);
```
Instead of passing the name of a function as an argument to another function, you can always pass a whole function instead:
```
Example
setTimeout(function() { myFunction("I love You !!!"); }, 3000);

function myFunction(value) {
  document.getElementById("demo").innerHTML = value;
}
```
In the example above, function(){ myFunction("I love You !!!"); } is used as a callback. It is a complete function. The complete function is passed to setTimeout() as an argument.

## Callback Alternatives

With asynchronous programming, JavaScript programs can start long-running tasks, and continue running other tasks in paralell.<br>

But, asynchronus programmes are difficult to write and difficult to debug. <br>

Because of this, most modern asynchronous JavaScript methods don't use callbacks. Instead, in JavaScript, asynchronous programming is solved using Promises instead. <br>

## JavaScript Promises
## JavaScript Async

Read them at w3 schools.
