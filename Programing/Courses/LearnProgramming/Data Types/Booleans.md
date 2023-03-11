Booleans are either **true** or **false**.
In reality these represent: 1 for true, and 0 for false

Booleans are LOGICAl, logical meaning True or False. 0 or 1 just like in real LOGICAL circuits.

``` js
let isMale = true;
let isFemale = false;
```

Note that we use operators ( Relational operators ) to compare values and get a boolean, either true or false. this is then used in conditional statements when we want to run our code IF SOMETHING IS TRUE. like the [[IF - then (Else)|if]] statements.

# Boolean logic

for more see: [[Operators|Operators]]

We can define and express boolean logic in diffrent ways eg:

``` js
if (hungry == true) {}

if (hungry != false) {}
```

hungry = true. And the if conditions will run in both cases.

`!=` means **NOT**. ("The oposite")

Booleans are commonly expresed using operators. like: `>` `<` `==` etc...
but when you combine these with the **NOT** operation it becomes a bit confusing.

Example:

___

can vote when 17 `FALSE`
can vote when 18 `TRUE` <---
can vote when 19 `TRUE`

VS

can NOT vote when 17 `TRUE`
can NOT vote when 18 `FALSE` <---
can NOT vote when 19 `FALSE`

___

In coding this is expresed as

``` js
age >= 18
```

VS

``` js
age < 18
```

`>=` becomes `<` without the = sign because it excludes the year when age = 18

>`<` is the oposite of `>=` 
