A **Reusable** piece of code that performs some code / logic. Then gives you the result

``` js
function double(number) {
	return number * 2
}
```

the returning value is what the function `double` will store.
`return` returns the computed value of your function. To be stored in variables or eg(printed)
This function doubles the number given when the function was initialized:

``` js
double(4)
```

the integer `4` takes on the varible(Parameter) named `number`
Output will be `8`

### Parameter and Arguments

A Parameter is simply: ==A variable to store your function arguments==
In our double function: `4` is our Argument AND `number` is our Parameter

![[parameters-vs-arguments.png]]

You can have multiple parameters/arguments or no parameters/arguments:

```js
function add(a, b) {
	return a + b
}

add(2, 3)
```

The returned value is `5`


### Variable Scope

The parameters and variables are only accesible within the function: `{}`

``` js
let name = "Philip"

function subtract(x, y) {
	return x - y
}

subtract(5, 7)
```

the parameters `x` and `y` are only within the function subtract.
And the variable `name` is not accesible within the subtract function. This is VARIABLE SCOPE

This can couse some confusion, that can be mitigated by not naming a variable inside a function the same as a variable in the main program.


### Storing functions inside variables

You can store the result of a function within a variable.

``` js
function multiply(x, y) {
	return x * y;
}

let result1 = multiply(5, 3);
```

Now the value `15` is stored within the `result1` variable. HUGE

> Note that the `x` and `y` variables are not describing names, but thats fine in our case since it just represents random numbers. Also because of **Variable Scope**

___
___

# Functions and Conditions

we can simply put conditions in our functions or:
We can run our functions based on conditions ( if, else, elif ). That can be very powerfull!

`if` statement to initialize the function (`party`)

``` js
function party() {
	...
}

if (age >= 18) {
	return party();
}
```

Here we use a function and an `if` statement to call another function (`double`)

``` js
function double() { // Runs third
	...
}

function run() { // Runs seccond
	if (operation == "double") {
		return double();
	}
}

run("double") // Runs first
```

Now imagine we add more conditions and perhaps more parameters. POWER!

``` js
function double(doubleNum) { // First defined // Not runned
	return doubleNum * 2;
}

function triple(tripleNum) { // Second defined // runned third
	return tripleNum * 3;
}

function run(operation, number) { // Third defined // runned second
	if (operation == "double") {
		return double(number);
	} elif (operation == "triple") {
		return triple(number);
	} 
}

run("triple", 20) // returns 60 // first runned
```

In this example we are **Passing the parameter**.

Parameter `number` of function `run()`
becomes ⬎
Parameter `tripleNum` of function `triple()`

### Code execution

Remember how code is interpreted / executed. Top-to-bottom.
first functions are defined. But they are not runned unless called.

>the intire program follows your defined programing logic

In the examples above we always use `return function()` we need to return our value gained from the function. If you would just call the function like this:

```js
function double(doubleNum) {
	return doubleNum * 2;
}

function run(operation, number) {
	if (operation == "double") {
		double(number); // 16
		// needs a return ;(
	}
}

run("double", 8) // undefined
```

The value calculated from the double function would return its value to the `run` function. But not any further!

___
___

# Function Body

When working with functions it might be usefull not to directly modify the value stored in a parameter. Instead create new variables to store a parameters modifyed value.

NOT "BEST-PRACTICE": ( but will work )

``` js
function getName(name) {
	name = name.toUpperCase();
	return name.trim();
}
```

CORRECT:

``` js
function getName() {
	formatted = name;
	formatted = formatted.toUpperCase();
	formatted = formatted.trim();
	
	return formatted;
}
```

Rather write you logic line by line that cram everything into one or a few lines. This makes it more easy to read, and easier to modify.

___
___

# `1` Tips

When writing functions that soule purpose is returning a boolean. Its best to start with:
- `can`
- `has`
- `is`

or something similar since the naming implies that the result will be either true or false:

``` js
function canVote() {
}

function isOlderThanMe() {
}

function hasDied() {
}
```

___

### `1.1` Define Varaibles before functions

WRONG:

``` js
function isWrong() {
	
}

name = "Philip"
```

Correct:

``` js
name = "Philip"

function isRight() {
	
}
```

___

### `1.2` Stressing the importance of reusability

The most important aspect of a function is to take in parameters and solve a problem, **Repeatedly**

Instead of:

``` js
let name = "Philip"
let age = 18

console.log("Welcome " + name + " You are " + age " Years old!" )
```

You can do this:

``` js
let name = "Philip"
let age = 18

function greetings(name, age) {
	return "Welcome " + name + " You are " + age " Years old!"
}

consolo.log(greetings(name, age))
```

Functions create **Reusability**

This also allows for easier to read and modify code. 
You can eg( place an `if` statement inside the function for more flexibility combined with reusability of a function)

___
___

# Errors:

[[Function Troubleshooting#`1` Implicit return|Implicit Return]]