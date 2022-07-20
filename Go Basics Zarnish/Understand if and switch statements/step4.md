---
title: if...else if...if statements

---


<!--

-->

This is a statement formed by combining "if...else" statements. It tests more than two conditions and executes a defined code block where the boolean result is true.

Check if the value of 5 multiplied by 3 is equal to 18, or more than 18, or less than 18. There are three conditions in this case and each is different from the other.

Enter the code below to create an application that checks the conditions stated above:

{{copy filename='code.go'}}
```go
package main

import (
	"fmt"
)

func main() {
	k := 5 * 3
	if 18 > k {
		fmt.Println("k is less than 18")
	} else if 18 == k {
		fmt.Println("k is equal 18")
	} else {
		fmt.Println("k is more than 18")
	}
}
```
{{ /copy }}

The code above should prints out the condition that the 5 multiplied by 3 satisfies.

Run it:

{{ execute }}
```
go run code.go
```
{{ /execute }}

Next, we will discuss the "switch...case" statement.