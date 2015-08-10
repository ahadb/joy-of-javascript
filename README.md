# The Joy of JavaScript

<i>Just getting started</i>

This premise of this repository is simply for budding developers who are looking for "an easy to digest" way to learn modern day JavaScript and have a solid working knowledge of market & industry standards. It's in the beginning stages at this point, but with alot of work it should emerge as a reference with byte-sized easy to swallow and digest information. 

I loathe monolithic learning mechanisms and that was the inspiration and vision behind creating this repository. I opine that it's easier to retain information in simple and clear doses. As you're starting out, don't be too hard on yourself (others might oppose your style of learning, don't listen to them) and learn incrementally.

There will also be a useful section where we can learn by example, which is the best way to actually learn a new language as well as a signal section where you can keep up-to-date with the language from the vibrant community.

Best part is that this side project will keep on growing as the language evolves and programmers from all walks start taking JavaScript more seriously. For the newbie this is a great language to start learning how to program as your can start doing cool stuff relatively quickly as the fruits of your labor unfolds in front of your eyes.

# Table of Contents

* Learn JavaScript
* Test Driven JavaScript (TDD)
* Design Patterns
* Modern JS Tooling
* Micro Libraries
* Frameworks
* NodeJS
* AngularJS
* ReactJS
* Other Resources
* ES6
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

In JavaScript, it is possible to declare multiple variables, like this:

```javascript
var foo = "Hello World";
var bar = "A string...";
var qux = 20;

// ...or like this
var foo = "Hello World",
    bar = "A string...",
    qux = 20;
```

The first way is easier to maintain as each declaration is a single statement on a single line.

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
 
```javascript 
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
 
#### Numbers & Strings
 
Both numbers and strings are very common data types, therefore the introduction and grouping together. They are called primitives or primitive data types by definition. 

A number can be created from a constant value and is prepended with the keyword <code>var</code>:

```javascript
// an example of an integer
var x = 12;

// an example of a float
var y = 1.9
```

With numbers the basic mathematic operations can be done using basic operators:


1. Addition: <code>d = a + b + c</code> 
2. Subtraction: <code>d = a - b - c</code>
3. Multiplication: <code>d = c * b * a</code>
4. Division: <code>c = a / b</code>
5. Using Parens: <code>d = (a + b) * c</code> // this is allowed just like in math

More advanced operations can be used using the following operators:

1. Increment: if we declare <code>z = 10</code>
 * <code>x = z++</code>  
 * <code>x = ++z</code>
2. Decrement: <code>z = 10</code>
 * <code>x = z--</code>
 * <code>x = --z</code>
3. Modulus: This is the remainder operator
```javascript
15 % 6 // 2
NaN % 2 // NaN
```

Similarily a string is also declared using the <code>var</code> keyword. A string represents text and data and is very similar to string implementations from different other languages. An example of a string is: "Hello World, This is JavaScript"

A string is defined using single or double quotes:

```javascript
// Double quotes example
var str = "I am a string";

// Single quotes example
var str = 'I am a string too';

// strings support UTF-8 characters

```

A very useful property of a string is the ability to calculate it's length using <code>.length</code>

```javascript
// Using the length property
var str = "I am a string";
var str_length = str.length;
console.log(str_length);

// Or simply just
var str = "I am a string".length;
```

Lastly, it's important to be able to concatenate two strings together. This means that we add two or more strings together.

```javascript
var firstName = "Jane";
var lastName = "Dough";
var fullName = "Jane" + " Dough"
var sentence = "My name is: " + "Jane" + " Dough" + ".";
```

Notice the whitespace in the string "My name is: " and " Dough". You can also use variables to create the same
 
```javascript
var firstName = "Jane";
var lastName = "Dough";
var fullName = "Jane" + " Dough"
var sentence = "My name is: " + firstName + lastName + ".";
```

Now you're programming! :-)

#### Arrays

Arrays are one of the data types that you will use quite often, so understand it well. We a good amount of data in one variable and that in turn allows us to use functions to perform operations on data. Data holds one or more elements and can simply be defined like so:

```javascript
// define and empty array
var my_arr = [];

// an array of strings
var cities = ["Washington DC", "Moscow", "London", "New York City", "New Dehli"];
 
// an array of numbers
var numbers = [10, 9, 8, 7, 6, 5, 0]
```

You might be asking yourself, so what can I do with these elements and how do I access them. An array starts of with an <code>index</code> or indices and points to a particular position in an array. It's important to note that Indices progress one by one and the first index in an array is 0 and not 1.

Let's try out a practical example:

```javascript
var dt = ["Numbers", "Strings", "Arrays", "Null", "Undefined", "Boolean", "Object"];

// find the first element in or array
dt[0];

// declare variables that holds a reference to a position in our array of elements
var str = dt[1];
var arr = dt[2];
var null = dt[3];
var obj = dt[6];

// you can also use the <code>length</code> prop to find the last el of an array
var lastEl = dt.length - 1;
```

An important property of an array is the <code>length</code> property:

```javascript
var myArr = [1, 2, 3, 4, 5];
var len = myArr.length; // 5
```

There is a lot you can do with arrays, and their are several built in methods like empty, clone, join and many more that you can use to perform surgery on arrays.

&rarr; View More on Arrays

#### Program Structure (Conditionals, Loops & Control Flow)

#### Objects

#### Functions

#### Console & Developer Tools

One of the best parts about JavaScript is that unlike other programming languages, with minimal effort an individual can start making things happen. In other words you can start seeing your code work with minimal effort within a browser environment. 

In my opinion as a budding developer having a fundamental understanding of the console using Developer Tools in your browser will help you tinker around with the language. Every browser has some form of developer tools pre-packaged, and one of the first-born versions of this tool was Firebug which integrated with Mozilla.
 
 In Chrome you can right click on a page to `inspect element', or use the hamburger menu and navigate to tools > developer tools or simply press <kbd>F12</kbd> in Windows or <kbd>Cmd</kbd> + <kbd>Opt</kbd> + <kbd>I</kbd> on the Mac.
 
 As a beginner and to become a decent developer you need to know the console, I recommend starting to hack away at it to get further acquainted. Note that you will have to know how to debug JavaScript applications using developer tools; it's crucial to be able to use this tool and use it well for debugging purposes.
 
 ```javascript
console.log("Hello World");
$('a'); // even if you're not using jQuery you can pass any css selector to $.
$('a').length;
document.body.contentEditable = true; // now edit anything on your page
getEventListeners($('#clickFn"));
monitorEvents($('#myInput'), ['click', 'keyup', 'focus']); // this will log all click, keyup and focus event fired
console.table();
dir($('#clickFn); // then expand and see all the properties
```
You can also use <code>console.log</code> and <code>debugger</code> statements for debugging your own code.


## Test Driven JavaScript

As developers we want to be able to feel confident our code won't break in different browsers and in different environments - all to often do we overlook testing by guessing at what code is required - a strategy that can easily lead to bloated and tightly coupled situations. Each line of code is tested by a representative sample code and therefore TDD will produce less buggy code and more robust functionality. 

As a novice developer, not only should you be focusing on learning core aspects of the JavaScript language but also unit testing in your iterative development process.

Note: Complete TDD and just writing unit tests are different, there are options if you want to remain fully TDD compliant.

Look at the example below:

```javascript
'use strict';

// simple test suite for strings using Jasmine
// just making sure describe, it and spec are working....
describe("A suite is just a function", function() {
    var a;
    it("and so is a spec", function() {
        a = true;
        expect(a).toBe(true);
    });
});
// they work!

// simple tests for strings
describe('Strings', function() {
    it("You can create a string by surrounding text with quotes", function () {
        expect("First" + "Second").toEqual("FirstSecond");
    });
    it("Concatenation works with numbers", function() {
        expect("52" + "String").toEqual("52String");
    });
    it('Concatenation evaluates expressions', function () {
        expect("Multiply 8*2 =" + 8 * 2).toEqual("Multiply 8*2 =16");
    });
    it('You can escape quotation marks with backslash', function () {
        expect("Escape\"Quotes\"").toEqual("Escape" + '"' + "Quotes" + '"');
    });
    it('Double equals will compare exact contents', function () {
        expect("String" == "String").toBe(true);
    });
    it('Double equals on strings is case sensitive', function () {
        expect("String" == "string").toBe(false);
    });
    it('Length of strings can be accessed with the .length property', function () {
        expect("ThisStringIsVeryLong".length).toBe(20);
    });
});
```

Get used to writing unit tests for your code - not only will it help you become a better developer but it will increase your chances of finding your dream where the compensation is over $100k. I suggest you look at some of the most common testing libraries and frameworks out there:

* Protractor or Karma
** Protractor is a JavaScript test-runner built with Node.js and meant for unit testing
** Protractor is for end to end testing, and uses Selenium Web Drive to drive tests
* TestSwarm
* QUnit
* Jasmine
* Mocha 

&rarr; View More Tests

## Design Patterns

You will find patterns in everyday things, occurrences and especially in software design and development. With the world of JavaScript evolving at the churn rate that it is today it will prove advantageous for us to take a look at these patterns as they have answered common problems by developers that came well before us.

So the definition of a pattern is a reusable solution that can be applied to commonly occurring problems in software design, and in our case JavaScript web applications. If you're a novice developer thrown into the ocean trying to swim in code you should feel grateful that there are templates that might solve your problems even though they are not the exact solution you are looking for.

Let's have a look at some design patterns:

* Singleton Pattern
* Mixin Pattern
* Decorator Pattern
* Flyweight Pattern
* Constructor Pattern
* Module Pattern
* Revealing Module Pattern
* Observer Pattern
* Mediator Pattern
* Prototype Pattern
* Command Pattern
* Facade Pattern
* Factory Pattern

Of course there are other patterns like jQuery patterns, general patterns, object creation patterns code reuse, DOM and browser patterns.

&rarr; View Design Patterns

## Modern JS Tooling

## NodeJS

## AngularJS & Single Page Applications

Single page applications have gained in popularity to the extent that they rule the web development world to date - everyone is talking about their fluid experience especially when navigating from page to page, scrolling on history, cacheable screens and a rapid fire back button. Unlike MPW's (multi page websites) SPA's are based on MVC, MVVM, XHR, and DOM manipulation. The most distinct feature besides two-way binding, dependency injection, templating, etc is routing as it's handled by the client-side application using JavaScript and not the server. Simply put, it means that the application handles browsing instead of the browser.

The first framework that is listed here is Angular, and if you haven't tried it you're missing out. Angular is what HTML should have been if it were designed to develop apps with. It's a JavaScript MVC framework developed by Google that let's you build well structured, easily testable and maintainable front-end applications. It also implements two way data binding while connecting your views directly to your model without much fuss. What that means is any change in your view will be immediately reflected in your model; very powerful, yes indeed.

Most importantly Angular is flexible with server communication and let's you work with any server side technology if you server your app through a RESTful web API. There is certainly alot more to learn about Angular, we'll get into some code in this repo and explain the basics - I hope that will want you to learn more about this superheroic framework.

A good start is to go straight to the source and start [reading the docs](https://angularjs.org/) on the Angular website. Whilst you're at it, it won't hurt to look at the newer version of Angular that will be released soon. Keep in mind that Angular JS tutorials can be quite difficult to follow for people with no previous MVC/TDD experience and especially if you have no JavaScript experience whatsoever. My personal opinion is to learn the basics of the framework by working incrementally and then you can apply more advanced techniques and form your development style. 

&rarr; View Learning Examples

## ReactJS

## Other Resources
 
## ES6

## Signal
