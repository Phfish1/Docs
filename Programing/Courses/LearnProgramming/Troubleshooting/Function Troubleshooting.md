
# Common Errors

### `1` Implicit return

implicit return occurs when not specifying a returned value. 
- The word implicit means: *sugested* but not directly specified.

In code that means you have not defined a value for the function to return and the computer will automaticly assign it for you

``` js
function getName(name) {
	formatted = name.trim();
}
```

getName returns: `undefined`
When calling the function getName, since no return is specified it becomes:

``` js
function getName(name) {
	formatted = name.trim();
	return undefined;
}
```

most functions need to specify a return!
