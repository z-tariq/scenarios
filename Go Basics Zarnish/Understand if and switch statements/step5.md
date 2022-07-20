---
title: switch...case statement

---


<!--

-->

The "switch...case" gives us a neater alternative to testing more than two conditions. We use the switch statement to select the block of code that is to be executed. Each ‘case’ statement represents a different condition that is being tested.

Let us create an application that tells you what to do based on the current date. Let’s classify the duties based on the dates as shown below:

- 1st → 5th:  Pay the rent
- 6th → 10th: Pay for electricity
- 11th → 20th: Pay the gym subscription
- 21st → 25th: Pay for Netflix
- 25th → end month: Shopping

We’ll use the “time” library to help us check the date and time.

Add the code below to complete the code:

{{copy filename='code.go'}}
```go
package main

import (
	"fmt"
	"time"
)

func main() {
	switch dateToday := time.Now(); {
	case dateToday.Day() < 6:
		fmt.Println("Pay the rent")

	case dateToday.Day() > 5 && dateToday.Day() < 11:
		fmt.Println("Pay for electricity.")

	case dateToday.Day() > 10 && dateToday.Day() < 21:
		fmt.Println("Pay Gym subscription")

	case dateToday.Day() > 20 && dateToday.Day() < 26:
		fmt.Println("Pay for Netflix")

	case dateToday.Day() > 25:
		fmt.Println("Do shopping")

	default:
		fmt.Println("No date has been captured")
	}
}
```
{{ /copy }}

This code starts by capturing the current date (`time.Now()`) and then checking if the day (`dateToday.Day()`) satisfies the conditions. It prints out the duty where the case is true.

Run the code using this command:

{{ execute }}
```
go run code.go
```
{{ /execute }}

Next, we will discuss the key takeaways.