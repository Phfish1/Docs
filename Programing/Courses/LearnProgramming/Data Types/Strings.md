Strings are datatypes defines but double quotes `"STRING"`. They hold multiple characters that composes a string / word:

``` js
let name = "Philip";
let country = "Norway";
let name = 18;
```

### String Properties

Properties are characteristics already known / computed. Like the length of the string. In JavaScript we can use the .length property to spit out the already computed length of the string. SEE [[Properties and Methods]]

``` js
let name = "Philip";

function ReturnNameLength(name) {
	return name.length;
}
```

# String Methods

Methods performs operations on the object its being used on. SEE [[Properties and Methods]]

Method is often defined with `()` at the end. Instead of nothing like properties

``` js
let name = "philip";

let BIGname = name.toUpperCase();


consoe.log(BIGname); // "PHILIP"
console.log(name); // "philip" 
```

This method makes a copy of the string, makes it UPPER case and in this instance stores it in `BIGname`

**Methods:**
- .toUpperCase()
- .toLowerCase()
- .trim()


### .trim()

Trim is a method for removing white spaces from your string
`    SPACE    ` - Becomes - `SPACE`

This can be usefull when gathering userinput or when working with data in general.

``` js
let email = " philip@gmail.com  "
email = email.trim() // "phlip@gmail.com"
```

___

# Comparing strings

We can use if (else) statements in clever ways to compare strings:
Examples:
- Comparing using `==`
- Trimming `.trim` or using `toLowerCase()` on input
- Using `.length`

Comparing name lengths:

``` js
let name = "Philip"

if (name.length >= 5) {
	console.log("Average name")
} else {
	console.log("Short name")
}
```

Gathering user input to make choices:

``` js

function niceInput(input) {
	input = input.trim()
	input = input.toLowerCase()
	return input
}

let choice = "  Y  "
choice = niceInput(choice)


if (choice == "y") {
	console.log("YES")
} else {
	console.log("NO")
}
```

___
___

# `1` String Concatenation

>Pronounced: ( Con-CAT-enation )
>Meaning: ( to link together something in a series or chain )

String **concatenation** is the process of combining(concatenating) strings together.

___

You concatenate / append a string to another one using the `+` operation:

``` js
let name = "Philip"
let fullName = name + " Skudvig" // Philip Skudvig 
```

Remember to add spaces. -> ` Skudvig` or else it would be `PhlipSkudvig`
Higly reusable code:

``` js
function greetings(name, age) {
	return "Welcome " + name + " You are " + age + " years old!"
}

console.log(greetings("Philip", 18)) // Welcome Phlip You are 18 years old!
```

### `1.1` Addition VS Concatenation

the operator `+` might do Addition or Concatenation based on the [[Operators#Operands|Operands]].

- 1 or more strings = Concatenation

- All numbers = Addition

>NOTE: In some languages you get an error concatenating a string and an integer

Example:

``` js
let name = "Philip"
let age = 18
let street = 21

console.log("Hello " + name) // Hello Philip | Concatenation
console.log(age + street) // 39 | Addition
console.log(name + age) // Philip18 | Concatenation
```

# `1` String Interpolation

Recomended [VIDEO](https://www.youtube.com/watch?v=0q8spKeh1Kc) 

String Interpolation is checking a string for placeholders(`{}`) then inserting into them a given value

Example in JavaScript:

``` js
let name = "Philip"
let age = 18

let message = `Hello ${name} you are ${age}` // Hello Philip you are 18
```

When using string interpolation in JavaScript we use a special string called a **template string**. Using ` `` ` instead of `""`. Then inserting our values using `${VALUE}`

``` js
let name `Name`
```

### `1.1` Examples in Python

VARIABLES USED:
``` python
name = "Philip"
age = 18
food = "Pizza"
cost_of_food_usd = 100
```

String Interpolation using a `f-string` ( Formatted string literal ). Like a template string

``` python
print(f"Hi {name} you are {age} years old!\n") ## Hi Philip you are 18 years old!
```

Using **[[Expressions and Statements|Expressions]]**

``` python
print(f"Age in 10 years is {age + 10}") # Age in 10 years is 28
```

Or different ways of using `.format()`

``` python
print("Hi {} you are {} years old!\n".format(name, age)) ## Hi Philip you are 18 years old 
```

Asigning names to variables using `.format()`

``` python
print("Menu: {food_item}. Cost is {cost}$ :)\n".format(food_item=food, cost=cost_of_food_nok)) # Menu: Pizza. Cost is 100$ :)
```


___
___
