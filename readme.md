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
