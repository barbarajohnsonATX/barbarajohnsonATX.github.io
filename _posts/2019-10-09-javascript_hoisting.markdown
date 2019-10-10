---
layout: post
title:      "Javascript Hoisting"
date:       2019-10-10 03:37:07 +0000
permalink:  javascript_hoisting
---


Hoisting in JavaScript is default behavior of moving declarations to the top of their scope before code execution. This means that a variable can be declared after it has been used.

**Function Declarations
**

These are hoisted completely to the top.  

```
hoisted();  // Output: "This function has been hoisted."

function hoisted() {
  console.log('This function has been hoisted.');
};
```


**Function Expressions**

These are not hoisted.
```
expression(); //Output: "TypeError: expression is not a function

var expression = function() {
  console.log('Is this hoisted?');
};
```
