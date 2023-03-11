# Variables 1.

Used to store data for further manipulation

``` Js
let age 18;
```

`age` is the VARIABLE_NAME
`18` is the VALUE

### Modifying variables

let/int whatever is only used first to declare the variable.
You cannot define `let age` more than once. But you can of course modify the value.

``` js
let age = 17;

age = 18;
```

UNLESS [[Functions#Variable Scope|Variable scopes]]. You can define the same variable name in diffrent variable scopes.

### Hardcoding

Make sure to not hardcode. Setting a fixed value. Much rather gather data which then is modified eg:

``` js
let year = 2023;
let nexdDecade = year + 10;
```

Now when next year comes around you will only have to change the variable `year`

___
___

# Naming conventions

**ALWAYS** Use Describing variable names. If not your gonna spend more time reading code than actually coding.
This also aplies to all namin. Do not underestimate the POWER of DESCRIBING NAMES!

BAD

``` js
let x = "Skudvig";
```

GOOD

``` js
let afterName = "Skudvig";
```

Naming conventions means a set of rules you use when defining variables, functions etc.
This is important because it makes your code easier to read and understand. HUGE!

### JavaScript naming conventions

JavaScript use **lowerCamelCase** for naming variables and functions:

>You cannot define a variable with spaces. So when writing spacious variables, you write first word lower case and all the word after UPPER case

``` js
let isThisLowerCamelCase = true; // CORRECT 
```

``` js
let This_Is_Not_Lower_Camel_Case = true // WRONG
```

Note that other languages use other naming conventions

### Python naming conventions

Python use a standard called **[PEP 8](https://realpython.com/python-pep8/)** 
Python writes functions and variables like so:

``` python
name = "Philip"
after_name = "Skudvig"
philip_cats_favorite_food = "Donuts"
```


