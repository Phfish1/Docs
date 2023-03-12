An **Array** is a list of values / variables. 
Its a way of structuring data.
Represented like this:

``` js
let shoppingList = ["banana", "apple", "chocolate", "MAGIC-BEANS"]
```

It can hold any value, even another arrays:

``` js
let eggList = [1,2,3,4]
let shoppingList = ["apple", eggList, true]

console.log(shoppingList) // ["apple", [1,2,3,4], true]
```

an empty array might also be usefull:

``` js
let secretList = []
```

### But why?

Instead of writing each variable together with its value, we can place them all inside 1 array

``` js
let age01 = 28
let age02 = 18
let age03 = 80
let age04 = 42
```

Array:

``` js
let ages = [28, 18, 80, 40]
```

This makes it scalable and reliable. How? see [[Arrays#`1.2` Arrays vs No array|Arrays vs No Array]] 

___

# `1` Accesing Arrays

An array is comprised of **array items**, represented by the **array indexes** storing the items

```js
let exampleArray = [5, 2, 6]
```

This array holds 3 items `5, 2, 6` each with its own **index**. 
The index of an array starts at **0** !

These are the values together with their indexes:

- `5` has an index of [`0`]
- `2` has an index of [`1`]
- `6` has an index of [`2`]

![[Array-index-example01.webp]]
### `1.1` Accesing indexes

To access the array index and its value we use `[]` together with the array and finally the index itself `myArray[0]` ( `0` representing the index )

``` js
let myArray = [7, 11, 6, 55]

myArray[0] // its value equals to: 7
myArray[1] // 11
myArray[2] // 6
myArray[3] // 55
```

>NOTE: If you gonna access item number 4 you do 4 - 1 and find the index of `3`

If you would try to access an index that does not exist. Like `4` or `89` you would get an error, or in JavaScript it will return `undefined`

### `1.2` Accesing First and Last

You always know what the first index is. it is `0`

You can acces the **Last** index by finding the [[Arrays#`1.4` Length of array|length]] of the list - 1. ( to account for indexes that start at 0 )

``` js
let numbers = [10, 20, 30, 40, 50]

let firstItem = numbers[0]
let lastItem = numbers[numbers.length - 1] // !!!

console.log(firstItem) // 10
console.log(lastItem) // 50

```

`lastItem` is an array item, and the index is an expression representing the length of the list `5` - 1 which is `4`. So its expressing `numbers[4]`. Redundant and Reliable

>In some languages like python you can simply write `numbers[-1]` to get the last item

___

# `2` Changing arrays

You can change an array by changing each individual item by accessing its index

``` js
let workers = [01, 02, 03, 04]
workers[01] = 00

console.log(workers) // [00, 02, 03, 04]
```

Or you can add new enteries, although there are better ->METHODS<- 
Here i use `.length` (NOT RECOMENDED) use [[Arrays#`1.3.1` .push() method|.push()]] 

``` js
let favNumbers = [10, 20, 30, 40]
favNumbers[4] = 50
favNumbers[favNumber.length] = 99

console.log(favNumbers) // [10, 20, 30, 40, 50, 99]
```

### `2.1` .push() method

**.push()** is a [[Properties and Methods|method]] used for adding items at the **END** of an array.
use this instead of `.length`

``` js
let familyMembers = ["Philip", "Mom"]
familyMembers.push("Dad")

console.log(familyMembers) // ["Philip", "Mom", "Dad"]
```

___

Every method returns something. `.push()` returns the length of the array.

``` js
let numbers = [10, 20, 30, 40]

console.log( numbers.push() ) // 4

function addNumber(numbers) {
	return numbers.push(10) // 4
}
```

We can not return `numbers.push()` inside a function that would only give us the array length
Do this instead:

``` js
function addNumbers(numbers) {
	numbers.push(10)
	return numbers
}
```





___
___

# Naming

Arrays should be named in plural. Because they are ment to hold more than 1 item:

``` js
let items = []
let ages = []
let suitUppgrades = []
let names = []
let groceries = []
```

when a more discribing name is present you MIGHT use that: ( Most ends in "list" )

``` js
let shoopingList = []
```

___
___

# `1` Examples

### `1.1` Logging a simple array

An array can be expressed just like a number, boolean or string etc..

``` js
console.log([10, 20, 30]) // [10, 20, 30]
```

### `1.2` Arrays vs No array

This is using an array. getting the length of `ages` needed to find the average.
We loop throught the `ages` array using a `for` loop. Appending each entry to the `sum` variable
Then we calculate the average and return the result

``` js
let ages = [28, 18, 80, 40]
let lengthOfAges = ages.length

function getAverageAge() {
    let sum = 0
    for (let i=0; i < lengthOfAges; i++) {
        sum += ages[i]
    }

  average = sum / lengthOfAges
  return average
}

result = getAverageAge()
console.log(result) // 41.5
```

Here is the same code but without arrays. Note that is not scalable by any means
It might look smaler, but note the long `+` chain and the unreliable `4` used when calculating the average

``` js
let age1 = 28
let age2 = 18
let age3 = 80
let age4 = 40

function getAverageAge(age1, age2, age3, age4) {
    sum = age1 + age2 + age3 + age4
    average = sum / 4
    return average
}

result = getAverageAge(age1, age2, age3, age4)
console.log(result)
```

### `1.3` Arrays with functions

You can pass arrays through functions, "AMAZING". but be aware of how **return** arrays

``` js
let playerData = [999, "philip", true]
```

CORRECT:

``` js
function resetScore(score) {
	score[0] = 0
	return score // [o, "philip", true]
}
```

WRONG: ( only returns the index `score[0]` which you set to 0 )

``` js
function resetScore(score) {
	return score[0] = 0 // 0
}
```

``` js
playerData = resetScore(playerData) // Function call
```

### `1.4` Length of array

Find the length of an array using the `.length` **[[Properties and Methods|property]]**

``` js
let numbers = [10,20,30,40,50]
let answers = [true, false, false]
let groceries = []

numbers.length // 5
answers.length // 3
groceries.length // 0
```

