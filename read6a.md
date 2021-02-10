 #javaScript Functions




![](https://www.google.com/url?sa=i&url=https%3A%2F%2Fwww.frontamentals.com%2Ffunctions%2F&psig=AOvVaw1IJyH-6O94ne2AhVmT6lbn&ust=1612962663379000&source=images&cd=vfe&ved=0CAIQjRxqFwoTCJD456jw3O4CFQAAAAAdAAAAABAD)


{A JavaScript function is a block of code designed to perform a particular task.

A JavaScript function is executed when "something" invokes it (calls it).{}

**Example**
function myFunction(p1, p2) {
  return p1 * p2;   // The function returns the product of p1 and p2
}

##Function expressions
{While the function declaration above is syntactically a statement, functions can also be created by a function expression.

Such a function can be anonymous; it does not have to have a name. For example, the function square could have been defined as:

const square = function(number) { return number * number }
var x = square(4) // x gets the value 16
However, a name can be provided with a function expression. Providing a name allows the function to refer to itself, and also makes it easier to identify the function in a debugger's stack traces:}


const factorial = function fac(n) { return n < 2 ? 1 : n * fac(n - 1) }

console.log(factorial(3))
Function expressions are convenient when passing a function as an argument to another function. The following example shows a map function that should receive a function as first argument and an array as second argument. 

function map(f, a) {
  let result = []; // Create a new Array
  let i; // Declare variable
  for (i = 0; i != a.length; i++)
    result[i] = f(a[i]);
  return result;
}
In the following code, the function receives a function defined by a function expression and executes it for every element of the array received as a second argument. 

function map(f, a) {
  let result = []; // Create a new Array
  let i; // Declare variable
  for (i = 0; i != a.length; i++)
    result[i] = f(a[i]);
  return result;
}
const f = function(x) {
   return x * x * x;
}
let numbers = [0, 1, 2, 5, 10];
let cube = map(f,numbers);
console.log(cube);
Function returns: [0, 1, 8, 125, 1000].

In JavaScript, a function can be defined based on a condition. For example, the following function definition defines myFunc only if num equals 0:

var myFunc;
if (num === 0) {
  myFunc = function(theObject) {
    theObject.make = 'Toyota';
  }
}
In addition to defining functions as described here, you can also use the Function constructor to create functions from a string at runtime, much like eval().

A method is a function that is a property of an object. Read more about objects and methods in Working with objects.