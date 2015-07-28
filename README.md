# The Joy of JavaScript

This premise of this repository is simply for people who are looking for a good resource about everything JavaScript. It's in the beginning stages at this point, but with alot of work it should emerge as a great reference for people to learn about and be inspired about the language of JavaScript. There will also be a useful section where we can learn by example, which is the best way to actually learn a new language (depending on your learning style).

# Table of Contents

* Learn JavaScript
* Test Driven JavaScript (TDD)
* Design Patterns
* Modern JS Tooling
* Learning By Example
* AngularJS
* ReactJS
* Micro Libraries
* Other Resources
* Signal 

## Learn JavaScript

### Basics

#### Variables

JavaScript is a loosely typed language - like Java or C# you don't have to explicitly declare what types of data the variables will hold. The only thing you need to do is to use the `var` keyword.

The most common types of variables in JavaScript are:

* Strings: lines of text. /ie: "hello", "hello world", "The Joy of JavaScript"
* Numbers: numbers include floats and integers. /ie: 22, 5, 140, 3.21, 0.11, 1, 5.02342
* Boolean: simply a true or false and nothing else
* Arrays: a collection of values
* Objects: one of the most common data types, represents more complex data
* undefined: when you use an object property that does not exist, or a variable that has been declared, nor assigned a value
* null: a variable that contains no valid data type

#### Comments

Comments help the developer to explain JavaScript code, make it more readable or to prevent execution.
JavaScript supports two types of comments:

Single Line:

``` javascript
var a = "I am string";
//this line will be ignored by the interpreter
var b = 32.1
```

Multiline:
 
``` javascript 
/* this is a multiline comment and will
be ignored by the interpreter
*/
var foo = function (num) {...};
```

#### Equality

Checking for equality as very common for JavaScript programmers, matter of fact all programmers rely heavily on equality checks throughout their code. For newbies, it's important to remember that `=` is an assignment operator and doesn't perform equality checking. 
 
 The basic equality operator is `==` and determines if two variables are equal. That has it's caveats as it doesn't determine if they are the same type of variable. Let's take the following variable definitions:
 
 ```javascript
 var foo = 11;
 var bar = 11;
 var quz = "11";
 var norf = "javascript";
```

Give the above code some thought. Quite obviously `foo == bar` will evaluate to `true` and `foo == norf` will evaluate to `false`. However `bar == qux` will also evaluate to true (notice they are different types). The `==` operator forces it's operands to the same type. 
 
 There is another operator called the `===` operator which determines that two variables are equal only if they are of the smae type and value. So, in the above code `foo == bar` evaluates to true, but now `bar === qux` will evaluate to false.

#### Console & Developer Tools

One of the best parts about JavaScript is that unlike other programming languages, with minimal effort an individual can start making things happen. In other words you can start seeing your code work with minimal effort within a browser environment. 

In my opinion as a budding developer having a fundamental understanding of the console using Developer Tools in your browser will help you tinker around with the language. Every browser has some form of developer tools pre-packaged, and one of the first-born versions of this tool was Firebug which integrated with Mozilla.
 
 In Chrome you can right click on a page to `inspect element', or use the hamburger menu and navigate to tools > developer tools or simply press <kbd>F12</kbd> in Windows or <kbd>Cmd</kbd> + <kbd>Opt</kbd> + <kbd>I</kbd> on the Mac.


## Test Driven JavaScript

As developers we want to be able to feel confident our code won't break in different browsers and in different environments - all to often do we overlook testing by guessing at what code is required - a strategy that can easily lead to bloated and tightly coupled situations. Each line of code is tested by a representative sample code and therefore TDD will produce less buggy code and more robust functionality. 

As a novice developer, not only should you be focusing on learning core aspects of the JavaScript language but also unit testing in your iterative development process.