# JavaScript Study Guide

## Values and Types
JavaScript has typed values, not typed variables. Built in types include:
- string  : 'hello world'
- number : 42
- boolean : true
- null and undefined : null / undefined
- object : { b: 'c' }
- symbol (ES6)

### Objects
Key Value pairs, set properties that hold own value
```javacript
var obj = {
    a: 'cat',
    b: '42',
    c: true,
};

obj.a;       // 'cat'
obj["b"];   //42
```

### Arrays
Array is object that any values
```javascript
var array = [
    "cat",
    42,
    true
];

array[0];           //'cat'
typeof array;  //object
```

## Functions
```javascript
function foo() {
    return 42;
}

foo.bar = "hello world";
typeof foo;             // function
typeof foo();          //number
typeof foo.bar       //string
```

## Value Comparisons
```javascript
var a = "42";
var b = Number( a );
var c = 43;
a == b;      //true
a === b;    //false
a < c;         //true
```

### Truthy and Falsy
All falsey four values are below:
```""``` (empty string)
```0```, ```-0```, ```NaN```(invalid number)
```null```, ```undefined```
```false```

### Equality
Four operators: ==, ===, !=, !==

## Function Scopes
Variables defined in functions with var are function specific, those without var are considered global
Along with typical scope ussage, ES6 allows for use of let, variable belongs to individual block
```javascript
function foo() {
    var a = 1;
    if (a >= 1) {
        let b = 2;
        while (b < 5) {
            let c = b * 2;
            b++;
            console.log( a + c );
        }
    }
}

foo();
// 5 7 9
```

## Conditionals
### if / elseif / else
```javascript
if (a == 2) {
    // do something
}
else if (a == 10) {
    // do another thing
}
else {
    // fallback to here
}
```

### Switch Statements
if 2 or 10, execute cool stuff
```javascript
switch (a) {
    case 2:
    case 10:
        // some cool stuff
        break;
    case 42:
        // other stuff
        break;
    default:
        // fallback
}

### Ternary Operator
```javascript
var a = 42;

var b = (a > 41) ? "hello" : "world";
```

## Strict Mode
strict mode allows for tighting of behavior, thus safer and more efficient in compilatoin
global variables will not be defined based inside of strict sections
```javascript
function foo() {
    "use strict";
    // this code is strict mode
    function bar() {
        // this code is strict mode
    }
}
// this code is not strict
```

## Functions As Values
foo is anonymous due to no name
```javascript
var foo = function() {
    // ...
}
var x = function bar() {
    // ...
}
```

### Immediately Invoked Function Expressions (IIFEs)
```javascript
var x = (function name(){
    console.log( "hello");
    return 24;
})();
x; //"hello" and 24
```
the (); actually executes the function expression, much like foo();

### Closure

### Moduels

## ```this``` Identifier

## Prototypes