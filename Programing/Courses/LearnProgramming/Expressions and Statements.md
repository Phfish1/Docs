Recomended: [Video](https://www.youtube.com/watch?v=WVyCrI1cHi8), [VideoArticle](https://hexlet.io/courses/intro_to_programming/lessons/expressions/theory_unit), [Article](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Expressions_and_Operators#Expressions) 

# Expression

> An Expression is any valid code that results in a value

Its a combination of one or more: values, functions or operators that computes a value

___

Example of expressions together with their produced values

`"Philip"` is Philip
`18` is 18
`1 + 2` is 3
`age == 18` is true or false
`18 > 12` is true

or it can be a function
`canVote(age)` in out case say it return true. "Depends on the function"

Example represents how the computer processes the expression: 
( Note: works left to right unless Math Order of Operation )

```
12 + square(7 + 5) + square(square(2));

12 + square(12) + square(square(2));
12 + 144 + square(square(2));
12 + 144 + square(4);
12 + 144 + 16;
156 + 16;
172;
```

For better understanding watch video linked on top of page

___

### Calculation order

You can change the order of operation using `()`

``` js
return 10 * 10 - 5 // 45
```

``` js
return 10 * (10 -5) // 25
```

expersions with `()` parentheses around them, are executed first

# Statements

A statment is a code / instruction for the program.

A program is essentially a sequence of statements.
eg: `if, while, for, let, const, print, console.log, etc...`

# Comparison

Code consists of statments together with expressions

A statement:

``` js
let name
```

An expression:

``` js
"Philip"
```

Code:

``` js
let name = "Philip"
```

___

Now you can start to understand why a Statement does not take a statement as a value, it would look like this:

Statement 1:

``` js
let name
```

Statement 2:

``` js
if() {}
```

Code:

``` js
let name = if() {}
```

Does not make sense or work.

___

Lets try the same example but only using expressions:

Expression 1:

``` js
5 + 5
```

Expression 2:

``` js
canVote()
```

Code:

``` js
5 + 5 = canVote()
```






