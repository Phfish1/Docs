Recomended [Article](https://www.techtarget.com/whatis/definition/operator)

An operation is simply, Characters. Representing a LOGICAL or MATHEMATICAL function.
Influences a perceived value for your specific desires.

>Takes one or more values, and yields another one.

for example: && means the the logical function AND. While + is a mathematical operator for addition

___

### Operands

Oper**ands** and NOT the important Oper**ator**. is simply a term for the objects we perform operations on. as depicted bellow:

![[operators-VS-operands.webp]]
In this example `18`, `12`, | `true`, and `allowed` are operands

``` js
if (18 > 12) {}

if (allowed == true) {}
```

___

# Operators:

___

- **[[Operators#Aritmetic - Operators|Arithmetic]]**
- **[[Operators#Relation / Comparison - Operators|Relation]]** / Comparison
- **[[Operators#Logical - Operators|Logical]]**

>Above ↑ Important!

- Bitwise
- Assignment
- Increment / Decrement
- ...

___

### Aritmetic - Operators

Aritmetic describes dealing with and manipulating properties and numbers.
-> MATH <-

| Operator | Operation |
|:---------:| ---------|
| +   | Addition |
| -   | Subtraction |
| *   | Multiplication |
| /   | Division |
| %   | Modulus |

% Modulus 

### Relation / Comparison - Operators

Relation operators compare values to get a TRUE or FALSE boolean in return.

| Operator | Operation |
| :-------: | ---------|
| == | Equal To |
| != | NOT Equal to |
| > | Greater than |
| < | Less than |
| >= | Greater than or Equal to |
| >= | Less than or Equal to |

Note: in JavaScript we should use `===` and `!==` at all times instead of `==` and `!=`

The function canVote returns TRUE. ( Note: Relation operators are widly used with `if` )

``` js
let age = 18

function canVote() {
	return age >= 18
}
```

### Logical - Operators

Logical in computer science means Booleans. A boolean is 1 or 0. Just like a LOGICAl circuit.

Theese operators take booleans as INPUT. And the logical condition decides what boolean it should OUTPUT

Simply: AND and OR bind together statements *(actually representing booleans)* to determine if binded together statement should be true or false. `if ( 18 > 1 && 1 < 18 )` = TRUE
While NOT makes a TRUE a FALSE and vise versa. NOT True = False

| Operator | Operation |
| :-------: | --------- |
| && | Logical AND |
| \|\| | Logical OR |
| ! | Logical NOT |

This code will execute. Replace any true with false and it will not
``` js
if( true && true ) {
	
}
```

`( 18 > 1 )` Represents either a TRUE or FALSE, this case TRUE. Its representing a Boolean

``` js
if ( 18 > 1 && true ) {
	
}
```

This code will execute if *left side* **OR** *right side* is TRUE.
``` js
if ( true || false ) {

}
```

___
# Extra
___

### Ligature

Note that sometimes we will use ligatures to make our code look nicer. eg:

Fira Mono is the font not using ligature. Fira code is.

![[Ligature.webp]]

### Assignment



