Print:
``` python
print("Hello world")
```

Console log
``` js
console.log("Hello world");
```

To display variables or text for (often) for debuging purposes.

It is IMPORTANT to note that console log / pring does **NOT REPLACE RETURN** when handeling a function.

WRONG:
``` js
function double(number) {
	console.log(number * 2);
}

double(4);
```

Print or console log simply prints the answer. Best practice is to return the computed logic of a function using the `return` statement. "`return` exits a function"

Good:
``` js
function double(number) {
	return number * 2;
}

// console.log(double(4)); also good
let result = ( double(4) );
console.log(result);
```

