
- If
- Else
- Else if / Elif

These are what we call conditional statements ( sometimes refered to as expressions or constructs ).

These **conditional statements** perform code based on their **condition** yielding either `true` or `false`

This is some psudocode demonstrating conditional statements together with a diagram

``` code 
if ( condition ) Then
	( code )
	
else if ( condition )
	( alternative code  )
	
else
	( final-alternative code )
	
End
```

![[IF-THEN-ELSE-END.webp]]

The conditions are booleans, and you might use operators to manipulate the result.
Python:

``` python
if var1 >= var2 :
    print("hi")

elif var1 != var2:
    print("We are not the same")")

else:
    print("oki bro")
```

___

# IF

`if` is the conditional statement that will run ONLY if its condition it met.
This allows us to do [[Control Flow Statements |Branching]] in our code. AKA run code non linearly

JavaScript:

``` js
if (age >= 18) {
	return true;
}
```

Or you can check if a number is positive

``` js
function isPositive(number) {

	if (number > 0) {
		return true;
	}
}
```

___

# Else

**Else** is placed after an `if` or `elif`. It runs only in cases where the if / else if statements does not run. ("IF `true` run, ELSE run this instead") 

``` js
if ( true ) {

} else {

}
```

### Oposite of Else:

`Else` takes the **Oposite** of the `if` statement.

The bellow IF says if `age >= 18` then run code. The **Else** truly represents the oposite of the `if` which is `age < 18`

``` js
if (age >= 18) {

} else {

}
```

Instead of writing an `if` expressing `age < 18` it is baked into the ELSE statement
Learn more about Boolean logic [[Booleans#Boolean logic|HERE]]

![[if-elseExample01.webp]]
Diagram indicating an if and else statment. Where `+` means the if condition is true, and `-` means the else is initialized


# Else if ( Elif )

Else if ( or sometimes refered to as `elif` ) is used in when handeling more than 1 or 2 scenarios. 

`Else if` is checked **ONLY** if the first `if` returns false.
It takes arguments just like an if statmenet. You can have as many as you want

``` js
let name = "Philip"
let nameLength = name.length

if (nameLength >= 10) {
	console.log("Long Name")
} else if (nameLength >= 5) {
	console.log("Average Name")
} else {
	console.log("Short Name")
}
```

``` js
CONSOLE OUTPUT:
"Average Name"
```

in this case `else` represents `NameLength < 5`. "Everything not defined in the if or else if"

![[else-if01.webp]]
Make notice of the `+` and `-` on the `if` block

> TIP: Remember that `else if` is checking everything that does not comply with the first `if` statement


___
___

# Common differentials

### `1` if and else without else

Inside a function the same effect of an else can be accomplished with a return like this:

``` js
function canVote(age) {
	if (age >= 18) {
		return true
	}
	return false
}
```

This is because the `return` statement exits the function

### `2` Boolean expression shortcut

Instead of writing an if-else statement we can simply return a boolean as an expression.
This example returns the result of the expression `age >= 18` -> true OR false

``` js
function canVote(age) {
	return age >= 18
}
```

instead of writing this:

``` js
function canVote(age) {
	if (age >= 18) {
		return true
	} else {
		return false
	}
}
```

learn more about expressions [[Expressions and Statements|HERE]] 