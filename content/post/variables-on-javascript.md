---
title: "Variables on Javascript"
date: 2023-02-06T22:44:00+07:00
draft: false
tags: ["javascript", "fundamental"]
---

## Variables

Variables is a name that programmer use to store value. In Javascript, we know 3 types of variable that can be used to store value :

1. var
2. let
3. const

When we store value using **_var_** and **_let_** keyword, the value can be reassigned with another value.

```javascript
//using keyword var to store x value
var x = 6;
console.log(x); // 6

//reassigned value x
x = 10;
console.log(x); // 10 => value change from 6 to 10

//using keyword let to store a value
let a = 4;
console.log(a); // 4

//reassigned value a
a = 3;
console.log(a); // 3 => value change from 4 to 3
```

Value assigned with using const keyword cannot be changed.

```javascript
//using keyword const to store x value
const x = 6;
console.log(x); // 6

//reassigned value x
x = 10;
console.log(x); // 6 => value not change to 10 cause using const keyword
```

## Redeclaring Variables

Redeclaring variable define with **_let_** keyword will result in error.

```javascript
let x = 10;
let x = 2; // cannot redeclared block-scope variable 'x'
```

But it is possible to Redeclaring variable define with **_var_** keyword.

```javascript
var x = 10;
var x = 2; // Possible
```

The **_let_** and **_const_** keyword was introduced to javascript since 2015. So if we want our code to run in older browser, we must use **_var_** keyword.

Using **_let_** and **_const_** within a **Block Scope**, will make the variable cannot be accessed outside of block.

```javascript
let x = 10;
console.log(x); // 10

//Declaring x inside Block
{
  let x = 5;
  console.log(x); // 5
}

// Variable x inside block cannot be accessed
console.log(x); // 10
```

But still possible to access it when using **_var_** keyword.

```javascript
var x = 10;
console.log(x); // 10

//Declaring x inside Block
{
  var x = 5;
  console.log(x); // 5
}

// Variable x inside block is accessed
console.log(x); // 5
```
