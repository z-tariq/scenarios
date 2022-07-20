---
title: Address and address value

---
<!--

Address and address value

-->

Let us now see how a pointer variable can be applied in an application. Assume we have an application that handles bank transactions. We'll use a pointer variable to show the location of the account balance.

Enter the code below to implement the example above.

{{copy filename='code.go'}}
```go
package main

import "fmt"

func main() {

	var accountBalance float64 = 10515.50
	var myBalance *float64 = &accountBalance

	fmt.Println("My balance is: ", accountBalance)
	fmt.Println("My balance pointer is: ", myBalance)
}
```
{{ /copy }}