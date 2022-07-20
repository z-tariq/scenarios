---
title: if statements

---
<!--

-->

This is a statement that checks if a single condition is fulfilled and executes a block of code if it’s fulfilled. When the statement’s result is `true` we execute the set code block and it’s `false` we don’t perform any execution.

For instance, assume that we can check if 2 multiplied by 2 is equal to 4. We can create a simple application to check this using the code below:

{{copy filename='code.go'}}
```go
package main

import (
	"fmt"
)

func main() {
	a := 4
	if a == 2*2 {
		fmt.Println(a)
	}
}
```
{{ /copy }}

The code above checks if the variable a is equivalent to the square of 2. If the condition is true, it prints out the value of a.

Run the code:

{{ execute }}
```
go run code.go
```
{{ /execute }}

Next, we will discuss the "if...else" statement.