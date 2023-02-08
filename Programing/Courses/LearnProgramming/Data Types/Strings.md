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

### String Methods

Methods performs operations on the object its being used on. SEE [[Properties and Methods]]

Method is often defined with `()` at the end. Instead of nothing like properties
``` js
let name = "philip";

let BIGname = name.toUpperCase();


consoe.log(BIGname); // "PHILIP"
console.log(name); // "philip" 
```

This method makes a copy of the string, makes it UPPER case and in this instance stores it in `BIGname`

