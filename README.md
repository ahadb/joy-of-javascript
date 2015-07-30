# The Joy of JavaScript

This premise of this repository is simply for budding developers who are looking for a good resource to get up to speed *quickly with modern day JavaScript and have a working knowledge of market and industry standards. It's in the beginning stages at this point, but with alot of work it should emerge as a great reference for people to learn and be inspired by. There will also be a useful section where we can learn by example, which is the best way to actually learn a new language (depending on your learning style) as well as a signal section where you can keep up-to-date with the language from the vibrant community.

Best part is that this side project will keep on growing as the language evolves and programmers from all walks start taking JavaScript more seriously. For the newbie this is a great language to start learning how to program as your can start doing cool stuff relatively quickly as your work unfolds in front of your eyes.

# Table of Contents

* Learn JavaScript
* Test Driven JavaScript (TDD)
* Design Patterns
* Modern JS Tooling
* NodeJS
* Learning By Example
* AngularJS
* ReactJS<br />
* <strike>Micro Libraries</strike>
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

#### Console & Developer Tools

One of the best parts about JavaScript is that unlike other programming languages, with minimal effort an individual can start making things happen. In other words you can start seeing your code work with minimal effort within a browser environment. 

In my opinion as a budding developer having a fundamental understanding of the console using Developer Tools in your browser will help you tinker around with the language. Every browser has some form of developer tools pre-packaged, and one of the first-born versions of this tool was Firebug which integrated with Mozilla.
 
 In Chrome you can right click on a page to `inspect element', or use the hamburger menu and navigate to tools > developer tools or simply press <kbd>F12</kbd> in Windows or <kbd>Cmd</kbd> + <kbd>Opt</kbd> + <kbd>I</kbd> on the Mac.


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

## Design Patterns

## Modern JS Tooling

## NodeJS

## AngularJS & Single Page Applications

Single page applications have gained in popularity to the extent that they rule the web development world to date - everyone is talking about their fluid experience especially when navigating from page to page, scrolling on history, cacheable screens and a rapid fire back button. Unlike MPW's (multi page websites) SPA's are based on MVC, MVVM, XHR, and DOM manipulation. The most distinct feature besides two-way binding, dependency injection, templating, etc is routing as it's handled by the client-side application using JavaScript and not the server. Simply put, it means that the application handles browsing instead of the browser.

The first framework that is listed here is Angular, and if you haven't tried it you're missing out. Angular is what HTML should have been if it were designed to develop apps with. It's a JavaScript MVC framework developed by Google that let's you build well structured, easily testable and maintainable front-end applications. It also implements two way data binding while connecting your views directly to your model without much fuss. What that means is any change in your view will be immediately reflected in your model; very powerful, yes indeed.

Most importantly Angular is flexible with server communication and let's you work with any server side technology if you server your app through a RESTful web API. There is certainly alot more to learn about Angular, we'll get into some code in this repo and explain the basics - I hope that will want you to learn more about this superheroic framework.

A good start is to go straight to the source and start [reading the docs](https://angularjs.org/) on the Angular website. Whilst you're at it, it won't hurt to look at the newer version of Angular that will be released soon.


## ReactJS

## Other Resources
 
## ES6

## Signal