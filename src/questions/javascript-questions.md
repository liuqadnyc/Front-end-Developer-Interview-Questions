---
title: JavaScript Questions
layout: layouts/page.njk
permalink: /questions/javascript-questions/index.html
---

* Explain event delegation.
  * 實作方法是將 click 事件綁在 parent 上，藉由 Event Bubbling 傳遞給 child，而非直接將事件綁定在 child 上。
  * https://cythilya.github.io/2015/07/08/javascript-event-delegation/
* Explain how `this` works in JavaScript.
  * this在method中的「第一層」會指向該物件，還有用new產生object時也是，除此之外都是指向Window ，另外非同步時也會指向Window。
  * Can you give an example of one of the ways that working with `this` has changed in ES6?
    * ES6中箭頭函數當中的 this 是定義時的對象，而不是使用時的對象
* Explain how prototypal inheritance works.
  * 當試圖存取一個物件的屬性時，其不僅會尋找該物件，也會尋找該物件的原型、原型的原型……直到找到相符合的屬性，或是到達原型鏈的尾端。
* What's the difference between a variable that is: `null`, `undefined` or undeclared?
  * undeclared variables is a variable that has been declared without ‘var’ keyword.
  * undefined is a variable that has been declared but no value exists and is a type of itself ‘undefined’.
  * null is a value of a variable and is a type of object.
  * How would you go about checking for any of these states?
    * 有賦值的undeclared變數需當成全域變數看，沒賦值會報錯
    * undefined和null都是變數的值，不過undefined的type就是undefined，null則是object
* What is a closure, and how/why would you use one?
  * 閉包是函式記得並存取語彙範疇的能力，可說是指向特定範疇的參考，因此當函式是在其宣告的語彙範疇之外執行時也能正常運作。
* What language constructions do you use for iterating over object properties and array items?
  * for      :直接對array[index]更改
  * for...in :可以把屬性都跑過一遍(連繼承來的都是)
  * forEach  :只能對array用,後面接callback func(value, index ,arr)
* Can you describe the main difference between the `Array.forEach()` loop and `Array.map()` methods and why you would pick one versus the other?
  * Array.map()比較侷限用在更改array值的時候，且一定會回傳一個矩陣；Array.forEach()相對自由，不用回傳，只要針對矩陣操作就行。
* What's a typical use case for anonymous functions?
  * Use as an argument to other functions, IIFE`(function(message) {alert(message);}('foo'));`
* What's the difference between host objects and native objects?
  * host objects: 為了完成特定環境任務而產生的物件，像在browser是window而server(node.js)是Nodelist
    *  (assuming browser environment): window, document, location, history, XMLHttpRequest, setTimeout, getElementsByTagName, querySelectorAll, ..
  * native objects: 是原本內建的，不分環境的
    *  Object (constructor), Date, Math, parseInt, eval, string methods like indexOf and replace, array methods, ...
* Explain the difference between: `function Person(){}`, `var person = function(){}`, and `var person = new Person()`?
  * `function Person(){}`:Function Declaration
  * `var person = function(){}`:Function Expression
  * `var person = new Person()`:Function Constructor
* Explain the differences on the usage of `foo` between `function foo() {}` and `var foo = function() {}`
  * 前者會提升整個宣告，後者只會提升變數。
* Can you explain what `Function.call` and `Function.apply` do? What's the notable difference between the two?
  * 兩者都是用來指定this的值，差別只在傳完this值後的參數一個是分開傳一個是用陣列傳。
* Explain `Function.prototype.bind`.
  * 把this值做綁定，卻不立刻執行function
* What's the difference between feature detection, feature inference, and using the UA string?
* Explain "hoisting".
* Describe event bubbling.
* Describe event capturing.
* What's the difference between an "attribute" and a "property"?
* What are the pros and cons of extending built-in JavaScript objects?
* What is the difference between `==` and `===`?
* Explain the same-origin policy with regards to JavaScript.
* Why is it called a Ternary operator, what does the word "Ternary" indicate?
* What is strict mode? What are some of the advantages/disadvantages of using it?
* What are some of the advantages/disadvantages of writing JavaScript code in a language that compiles to JavaScript?
* What tools and techniques do you use debugging JavaScript code?
* Explain the difference between mutable and immutable objects.
  * What is an example of an immutable object in JavaScript?
  * What are the pros and cons of immutability?
  * How can you achieve immutability in your own code?
* Explain the difference between synchronous and asynchronous functions.
* What is event loop?
  * What is the difference between call stack and task queue?
* What are the differences between variables created using `let`, `var` or `const`?
* What are the differences between ES6 class and ES5 function constructors?
* Can you offer a use case for the new arrow `=>` function syntax? How does this new syntax differ from other functions?
* What advantage is there for using the arrow syntax for a method in a constructor?
* What is the definition of a higher-order function?
* Can you give an example for destructuring an object or an array?
* Can you give an example of generating a string with ES6 Template Literals?
* Can you give an example of a curry function and why this syntax offers an advantage?
* What are the benefits of using `spread syntax` and how is it different from `rest syntax`?
* How can you share code between files?
* Why you might want to create static class members?

## Coding questions
* Make this work:
```javascript
duplicate([1,2,3,4,5]); // [1,2,3,4,5,1,2,3,4,5]
```
* Create a for loop that iterates up to `100` while outputting **"fizz"** at multiples of `3`, **"buzz"** at multiples of `5` and **"fizzbuzz"** at multiples of `3` and `5`
