Recomended: [Article](https://pynative.com/python-control-flow-statements/) 

Control Flow is the order of which code is executed within a program. Control flow statements are how we manipulate the control flow

flow control statements in python:

![[python-flow-control-statements.webp]]

### Branching

`IF` is a control flow statement that will run ONLY if its condition is met.
This introduces the concept of **Branching**.

Braching is essentially instead of executing code linearly one-by-one we define **control flow statements** that intersect with this linearity allowing us to run code in different orders.

![[branching-and-linear-programming.png]]

Here is some code together with a diagram to help visualize it: ( [TOOL USED](https://bogdan-lyashenko.github.io/js-code-to-svg-flowchart/docs/live-editor/index.html) )

``` js
let loopvar = true

while (loopvar) {
  if (count > 18) {
    count = count + 1
  }
  
  if (count < 5 ) {
    console.log("You baby")
  }
  
}

END
```

![[braching01-flowchart.webp]]
