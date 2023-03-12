In JavaScript you comment like this:

``` js
// Hi i am a comment
let name = "Philip"
// I will never run :)

// Here to provide context and help in reading and understanding the code
```

Multiline comments:

``` js
/*


HUGE comment



*/

```


### JSdoc Comments

JSdoc comments are mostly for adding documentation alongside your code.
See how to use [JSdoc](https://jsdoc.app/about-getting-started.html) 
Writen like this:

``` js
/** Documenting the getName() function */
```

``` js
/**
*
* Multiple lines
*
*/
```

___

There are other use cases for JSdoc comments like helping the coding experience. Not the reading experience.

I came uppon an example that tells the online code editor to recognise the variable as an array: ( usefull for **autocompletion** )

``` js
let names = ["Philip", "Bernard", "Arne", "Arve"]

/** 
* @params {array} names
*/
```