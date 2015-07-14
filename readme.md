#Javascript Cheatsheet

####5 Primitives
* strings
* Boolean
* numbers
* null
* undefined

####Functions-
* expression syntax
    *  Setting a variable equal to a function-
the variable becomes the function
var greet = function()

* declaration syntax;
    * Moves this code to the top of the page,
so greet(); could be placed before and it would still run

```javascript
function greetDeclaration() {
console.log(“Hello!”);
}
greetDeclaration();
Hello!
```
* return vs console.log
    * console.log prints it to the screen without saving it
    * Great for testing and debugging
    * return can used throughout the function
    * return also takes the info out of the function


####Loops - while, for
*Iterates!  Saves time!  Goes through all the things!
*While- does something as long as something is true
while (true) {  }
*For- do for amount defined
for (var i = 0; i < array.length; i++) {
array[i] }

####Conditionals
if (true) {
}else if (true) {
}else {
}
}

####Variables
* Defining variables- var name = thing (string, number, function, etc.)
* Calling- enacting the function

####Alerts/prompts
* Prompt- asks for response, inputs original data
* Alert- ok or cancel

####Scope
* What is it- Where the variable lives within a range
    *  global
        *  accessible from anywhere
    * local
        * accessible within the function
* Hoisting
-BAD. always use var to define them at the top of scope

####String concatenation
* putting strings together
* use the + operator




#Classwide JavaScript Cheat Sheet

### Primitives
Primitives are the basic building blocks of JavaScript.
* `null` - intentionally valueless
* `undefined` - value has yet to be defined
* string
* boolean - `true` and `false`
* number

### Variables
* Variables function as containers for values.
* Allow you to pass values around and refer to them with a set ID.
* Should have meaningful and preferably unique names that follow the JavaScript naming conventions.
* Declaration syntax: `var varName = varValue`
* Variables can have their values reassigned later with another assignment statement: `varName = newValue`

### Math Operators

* addition (`+`)
* subtration (`-`)
* multiplication (`*`)
* division (`/`)
* modulus (`%`)
* The mathematical operators can be combined with the assignment operator (`=`). - ex: `+=`

### Logical Operators
* and (`&&`)
* or (`||`)

###Comparison Operators
* greater-than (`>`)
* less-than (`<`)
* greater-than or equal (`>=`)
* less-than or equal (`<=`)
* equal (`==`)
* not equal (`!=`)
* strict equal (`===`)
* strict not equal (`!==`)
* [More on operators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Expressions_and_Operators)

### Conditionals
* Conditional statements control the flow of a program.
* Conditionals are done with `if...else if...else` blocks
      if (condition) {
        //some code
      }
      else if (condition) {
        //some code
      }
      else {
        //some more code
      }
* The `else` block is usually your catch-all or default behavior block.
* `switch` statements can also be used to control program flow based on the value of a sentinel variable.
      switch (expression) {
        case someVal:
          //do things
          break;
        case 1:
          //do things
          break;
        case "blue":
          //do things
          break;
        default:
          //default behavior
      }
* The `default` block gets executed if `expression` doesn't match any of the cases.

### Loops
* Allows you to keep running a certain piece of code for a certain number of iterations.
* `while` loops:
  1. Will execute and continue to execute as long as the Boolean expression given to the loop evaluates to `true`.

         while (someBooleanExpression) {
           //do stuff
         }
* `for` loops:
  1. `for` loops are useful for when you know how many times you want to iterate because you are explicitly setting the number of iterations with either a primitive value or a variable.

         for (var i = 0; i < stop; i++) {
            //do stuff
         }
  2. In the above, `var i = 0` is the expression that defines where you want to start the `for` loop.
  3. `i < stop` defines where you want to stop the loop.
  4. `i++` defines how you want to change `i` after each iteration.
  5. The general pattern is: `for (start; stop; change)`.
  6. The `start` expression is executed before the first iteration of the loop.

### Functions
* Allow us to capture and reuse blocks of code.
* Should have a single defined purpose.
* Can be defined using either _expression syntax_ or _declaration syntax_.
* Expression syntax:
        var myFunction = function(){
              //do stuff
      }
* Declaration syntax:
      function myFunction() {
        //do stuff
      }
* When you use declaration syntax to define a function, it's
* JavaScript functions can take zero arguments, or as many arguments as you want.
* Functions can take and deal with optional arguments as well. If you do not give a parameter that the function is expecting, JavaScript will set that parameter to `undefined`.
* Will return `undefined` unless you use a `return` statement in the function body.
* When a `return` statement is executed, control breaks out of the function.
* __Parameters__ are the variable names you use when defining a function - ex: `function myFunction(thing1, thing2)`.
* __Arguments__ are the values that you supply to a function when you call it - ex: `myFunction(32, true);`

### Scope
* Variables that are defined outside of any functions are part of the _global_ scope.
* Global variables can be accessed by any other piece of the script.
* Variables defined within a function are part of that function's _local_ scope.
* Local variables are created each time a function is called. The values are not shared between function calls.
* Descendant scopes are always aware of the variables within their ancestors' scope.
* Ancestor scopes are _not_ aware of the variables within their descendants' scopes.
* You can pass variable values outside of the function by returning its value.
* __Hoisting__ is when you reassign a global variable's value  within a function.
* You can avoid hoisting by always using `var` when declaring variables.
* Hoisting example:
      var someVar = 0;
      console.log(someVar);
      >> 0

      function myFunction() {
        //hoisting
        someVar = "cat";
        return "No problems here. Move along, move along."
      }
      myFunction();
      console.log(someVar);
      >> cat

### String Concatenation
* Joining two or more strings together.
* Example:
      var lastName = "Williams";
      var midName = "Dee"
      var fullName = "Billy " + midName + " " + lastName;
* You can build strings with the += operator:
      var someString = "Mary";
      someString += " had a little lamb";
      //the above means the same as:
      someString = someString + "had a little lamb";
* You can concatenate different types of primitives together into one string.

### `alert`, `prompt`, and `confirm`
* The `alert` function allows you to show the user pop-up messages in an OK or Cancel message box.
* The `prompt` function works in a similar way, but provides a text input field for the user to enter input.
* Text received by the `prompt` function is received as a string.
* `confirm` produces a message box as well, but when OK is clicked it returns `true` otherwise it returns `false`.

### Useful Methods
* `str.length`: the length of the string `str`.
* `str.toUpperCase()`: returns the uppercase version of `str`.
* `str.toLowerCase()`: returns the lowercase version of `str`.
* `str.parseInt()`: convert a valid string into an integer.
* `str.charAt(i)`: returns the character in a string at index `i`.
* `obj.toString()`: returns the string representation of an object.
* `data.length`: the number of elements in the array `data`.
* [The JavaScript methods index](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Methods_Index)
