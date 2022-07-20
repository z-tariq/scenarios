---
title: Change the value at a pointer's address

---
<!--

Change the value at a pointer's address

-->

Assume that we have made a withdrawal from the account and want to update the account balance. This would essentially require us to change the value at the address given by the pointer. This is called **passing data by reference**.

Add the code below to show how this works:

{{copy filename='code.go'}}
```go
package main

import "fmt"

func main() {

	var accountBalance float64 = 10515.50
	var myBalance *float64 = &accountBalance

	fmt.Println("My balance is: ", accountBalance)
	fmt.Println("My balance pointer is: ", myBalance)

	//Check the type of myBalance
	fmt.Printf("myBalance data type is: %T\n", myBalance)
	//Deference variable
	var myValue float64 = *myBalance
	//Check the type of myValue  after dereferencing
	fmt.Printf("myValue data type is: %T\n", myValue)
	fmt.Println("Value at the pointed address is: ", myValue)

{{ highlight }}
	//Change referenced variable
	var withdrawnAmount float64 = 5000
	*myBalance = *myBalance - withdrawnAmount
	fmt.Println("Value at pointed address is ", *myBalance)
{{ /highlight }}

}
```
{{ /copy }}

The code calculates the balance left after withdrawing `5000` from the account. The balance is updated from the pointer `*myBalance` by subtracting the `withdrawnAmount` from the value at the address given by the pointer (`*myBalance = *myBalance - withdrawnAmount`).

Use the command below to run the application:

{{ execute }}
```
go run code.go
```
{{ /execute }}

Next, we’ll look at the key takeaways.