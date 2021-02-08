**Today's summary**

#*Comparison and Logical Operators* 

<Use this article as a reference sheet for JavaScript comparison and logical operators.>
<Use this article as a reference sheet for JavaScript comparison and logical operators>

**Comparison operators — operators that compare values and return true or false. The operators include: >, <, >=, <=, ===, and !==.
Logical operators — operators that combine multiple boolean expressions or values and provide a single boolean output. The operators include: &&, ||, and !.
Comparison Operators
You may be familiar with comparison operators from math class. Let’s make sure there aren’t any gaps in your knowledge.**

Less than (<) — returns true if the value on the left is less than the value on the right, otherwise it returns false.
Greater than (>) — returns true if the value on the left is greater than the value on the right, otherwise it returns false.
Less than or equal to (<=) — returns true if the value on the left is less than or equal to the value on the right, otherwise it returns false.
Greater than or equal to (>=) — returns true if the value on the left is greater than or equal to the value on the right, otherwise it returns false.
Equal to (===) — returns true if the value on the left is equal to the value on the right, otherwise it returns false.
Not equal to (!==) — returns true if the value on the left is not equal to the value on the right, otherwise it returns false.
Logical Operators
Comparison operators allow us to assert the equality of a statement with JavaScript. For example, we can assert whether two values or expressions are equal with ===, or, whether one value is greater than another with >.

There are scenarios, however, in which we must assert whether multiple values or expressions are true. In JavaScript, we can use logical operators to make these assertions.

&& (and) — This operator will be truthy (act like true) if and only if the expressions on both sides of it are true.
|| (or) — This operator will be truthy if the expression on either side of it is true. Otherwise, it will be falsy (act like false).
var isTrue = ('yellow' === 'green') && (4 >= 4);
In the example above, we check if the string 'yellow' is equal to the string 'green' and (&&) if 4 is greater than or equal to 4. Let’s break this down into the two comparison expressions.
The first expression is false, because the string 'yellow' is not the same (equal) as the string 'green'.
The second expression is true, because the number 4 is greater than or equal to 4.
The && operator requires that both expressions be true in order for the expression to be truthy. Because one expression is false and the other is true, the expression is falsy and evaluates to false.

##The While Loop
The while loop loops through a block of code as long as a specified condition is true.

*Syntax*
while (condition) {
  // code block to be executed
}
*Example*
In the following example, the code in the loop will run, over and over again, as long as a variable (i) is less than 10:

*Example*
while (i < 10) {
  text += "The number is " + i;
  i++;
}

**The Do/While Loop**
The do/while loop is a variant of the while loop. This loop will execute the code block once, before checking if the condition is true, then it will repeat the loop as long as the condition is true.

Syntax
do {
  // code block to be executed
}
while (condition);
*Example*
The example below uses a do/while loop. The loop will always be executed at least once, even if the condition is false, because the code block is executed before the condition is tested:

*Example*
do {
  text += "The number is " + i;
  i++;
}
while (i < 10);

**Comparing For and While**
If you have read the previous chapter, about the for loop, you will discover that a while loop is much the same as a for loop, with statement 1 and statement 3 omitted.

The loop in this example uses a for loop to collect the car names from the cars array:

*Example*
var cars = ["BMW", "Volvo", "Saab", "Ford"];
var i = 0;
var text = "";

for (;cars[i];) {
  text += cars[i] + "<br>";
  i++;
}
