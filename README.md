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
