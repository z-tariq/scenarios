---
title: A second pointer example

---
<!--

A second pointer example

-->

This is another example of a program using pointers:

{{copy filename='code.go'}}
```go
package main

import "fmt"

func main() {
	x := 10

	fmt.Println("x before executing the updateX function: ", x)
	updateX(&x)
	fmt.Println("x after executing the updateX function: ", x)
}

func updateX(x *int) {
	*x = 20 // x now is no longer 10 but 20
	fmt.Println("x while executing the updateX function: ", *x)
	y := 30
	x = &y 
	/* This has no impact on the caller 
	The variable x is scoped only to the method body,
	since we are not dereferencing it (*x)
	*/
	fmt.Println("x while executing the updateX function: ", *x)
}
```
{{ /copy }}

Here the variable `x` is an int initialized with a value of 10. 

Within the function `updateX`, the value at address `*x` is then updated to 20. The variable `y` is an int initialized with a value of 30. The variable `x` is then updated with the value at the variable `y` location.

Run the code to see that:

{{ execute }}
```
go run code.go
```
{{ /execute }}

Next, we’ll look at more examples and we will understand what is "dereferencing".