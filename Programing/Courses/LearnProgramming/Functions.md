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

4 takes on the varible(Parameter) number
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

### Storing functions inside variables

You can store the result of a function within a variable.

``` js
function multiply(x, y) {
	return x * y
}

let result1 = multiply(5, 3)
```

Now the value `15` is stored within the `result1` variable. HUGE

> Note that the `x` and `y` variables are not describing names, but thats fine in our case since it just represents random numbers. Also because of **Variable Scope**