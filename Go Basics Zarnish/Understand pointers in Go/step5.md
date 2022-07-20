---
title: Dereference a variable

---
<!--

Dereference a variable

-->

In the previous step, we saw how we can create a pointer that shows the memory location of a variable. In this step, we’ll see how we can read the value that is stored at the address given by a pointer. This concept is called **dereferencing a variable**.

Enter the code below:

{{copy filename='code.go'}}
```go
package main

import "fmt"

func main() {

	var accountBalance float64 = 10515.50
	var myBalance *float64 = &accountBalance

	fmt.Println("My balance is: ", accountBalance)
	fmt.Println("My balance pointer is: ", myBalance)

{{ highlight }}
	//Check the type of myBalance  
	fmt.Printf("myBalance data type is: %T\n", myBalance)
	//Deference variable
	var myValue float64 = *myBalance
	//Check the type of myValue  after dereferencing
	fmt.Printf("myValue data type is: %T\n", myValue)
	fmt.Println("Value at the pointed address is: ", myValue)
{{ /highlight }}

}
```
{{ /copy }}

From the code above, the variable `myValue` reads the balance data from the address given by `myBalance` pointer.

Run the code using the command below:

{{ execute }}
```
go run code.go
```
{{ /execute }}

Next, we’ll look at how to change the variable using the pointer variable.