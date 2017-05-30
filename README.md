# Web Manifest Validator

This page is meant to be used to test the validity of a Web Manifest. The parser follows the rules from the W3C specification.

https://manifest-validator.appspot.com/


# Arrow functions

An arrow function expression has a shorter syntax than a function expression and does not bind its own this, arguments, super, or new.target. These function expressions are best suited for non-method functions, and they cannot be used as constructors.

## Basic Syntax

````JS
(param1, param2, …, paramN) => { statements }
(param1, param2, …, paramN) => expression
// equivalent to: (param1, param2, …, paramN) => { return expression; }

// Parentheses are optional when there's only one parameter:
(singleParam) => { statements }
singleParam => { statements }

// A function with no parameters requires parentheses:
() => { statements }
() => expression // equivalent to: () => { return expression; }
````

# Classes & Constructors
Always use class. Avoid manipulating prototype directly.
class syntax is more concise and easier to reason about.
````JS
class Queue {
  constructor(contents = []) {
    this.queue = [...contents];
  }
  pop() {
    const value = this.queue[0];
    this.queue.splice(0, 1);
    return value;
  }
}
````

## Advanced Syntax
````JS
// Parenthesize the body to return an object literal expression:
params => ({foo: bar})

// Rest parameters and default parameters are supported
(param1, param2, ...rest) => { statements }
(param1 = defaultValue1, param2, …, paramN = defaultValueN) => { statements }

// Destructuring within the parameter list is also supported
var f = ([a, b] = [1, 2], {x: c} = {x: a + b}) => a + b + c;
f();  // 6
````


# Advance JavaScript


````JS
// Boring
if (isThisAwesome) {
  alert('yes'); // it's not
}

// Awesome
isThisAwesome && alert('yes');

// Also cool for guarding your code
var aCoolFunction = undefined;
aCoolFunction && aCoolFunction(); // won't run nor crash


//debugger
var x = 1;
debugger; // Code execution stops here, happy debugging
x++;


var x = Math.random(2);
if (x > 0.5) {
  debugger; // Conditional breakpoint
}
x--;

//globals_for_debugging
var deeplyNestedFunction = function() {
  var private_object = {
    year: '2013'
  };
  
  // Globalize it for debugging:
  pub = private_object;
};

// Now from the console (Chrome dev tools, firefox tools, etc)
pub.year;


//join
['first', 'name'].join(' '); // = 'first name';

['milk', 'coffee', 'sugar'].join(', '); // = 'milk, coffee, sugar'

//jshipster_method
// Boring
if (success) {
  obj.start();
} else {
  obj.stop();
}

// Hipster-fun
var method = (success ? 'start' : 'stop');
obj[method]();

//jshipster_or_or
// default to 'No name' when myName is empty (or null, or undefined)
var name = myName || 'No name';


// make sure we have an options object
var doStuff = function(options) {
  options = options || {};
  // ...
};


/jshipster_templates
var firstName = 'Tal';
var screenName = 'ketacode'

// Ugly
'Hi, my name is ' + firstName + ' and my twitter screen name is @' + screenName;

// Super
var template = 'Hi, my name is {first-name} and my twitter screen name is @{screen-name}';
var txt = template.replace('{first-name}', firstName)
                  .replace('{screen-name}', screenName);


//jshipster_timing
var a = [1,2,3,4,5,6,7,8,9,10];

console.time('testing_forward');
for (var i = 0; i < a.length; i++);
console.timeEnd('testing_forward');
// output: testing_forward: 0.041ms

console.time('testing_backwards');
for (var i = a.length - 1; i >= 0; i--);
console.timeEnd('testing_backwards');
// output: testing_backwards: 0.030ms 

//jshipster
var z = 15;
doSomeMath(z, 10);
xxx // Great placeholder. I'm the only one using xxx and it's so easy to find in code instead of TODOs
doSomeMoreMath(z, 15);
````

#### TODO : Map, Reduce, and Filter
