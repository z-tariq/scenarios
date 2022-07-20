---
title: Pointers, values and addresses

---
<!--

Pointers, values and addresses

-->

To create a pointer, we use an asterisk `*` and an ampersand `&`. When an ampersand `&` is placed in front of a variable, it indicates that the value represents the address of the variable. When an asterisk `*` also known as a **dereferencing operator** follows a variable name, it indicates that it is a pointer variable. For instance:

```go
var myBalance *float64 = &accountBalance
```

The above code creates a `myBalance` pointer that points to a float64 variable that is initialized with the address of `accountBalance`.

`myBalance` is not a `float64` variable but it's a `*float64`. This is why the following code is not correct:

```go
var accountBalance float64 = 100.21
var myBalance *float64 = accountBalance
```

Go will return a similar error to the following one: `cannot use accountBalance (type float64) as type *float64 in assignment`.

The above code should be:

```go
var accountBalance float64 = 100.21
var myBalance *float64 = &accountBalance
```

Let's implement the code above in a program:

{{copy filename='code.go'}}
```go
package main

import "fmt"

func main() {
	var accountBalance float64 = 100.21
	var myBalance *float64 = &accountBalance
}
```
{{ /copy }}

In order to print the value of `myBalance`, this is what we should use:

{{copy filename='code.go'}}
```go
package main

import "fmt"

func main() {
	var accountBalance float64 = 100.21
	var myBalance *float64 = &accountBalance
{{ highlight }}
	fmt.Print(*myBalance)
{{ /highlight }}
}
```
{{ /copy }}

Execute the above code to check the result:

{{ execute }}
```
go run code.go
```
{{ /execute }}

However, if your goal is just printing the address of the variable `myBalance`, you will need to use:

{{copy filename='code.go'}}
```go
package main

import "fmt"

func main() {
	var accountBalance float64 = 100.21
	var myBalance *float64 = &accountBalance
{{ highlight }}
	fmt.Print(myBalance)
{{ /highlight }}
}
```
{{ /copy }}

Execute the above code to check the result:

{{ execute }}
```
go run code.go
```
{{ /execute }}