---
title: if...else statements

---
<!--

-->

This statement checks if a single condition is fulfilled and executes one of two code blocks depending on the output. This gives more flexibility than the if statement because you can execute a block of code even when the output is false.

For instance, check if 5 multiplied by 4 is equal to 25. If it is a false statement, then check the value of 5 multiplied by 4. The application below executes this logic:

{{copy filename='code.go'}}
```go
package main

import (
	"fmt"
)

func main() {
	a := 25
	if a == 5*4 {
		fmt.Println(a)
	} else {
		fmt.Println(5 * 4)
	}
}
```
{{ /copy }}

The code above should print out the value of 5*4 after confirming it is not equal to 25.

Run the application using the command below:

{{ execute }}
```
go run code.go
```
{{ /execute }}

Next, we will see the "if...else...if" statement.