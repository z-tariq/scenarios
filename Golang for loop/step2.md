---
title: Create a simple for loop

---
<!--

-->

The basic for loop will iterate until the counter reaches the point where the boolean is false.

Assume we want to output all the numbers between 5 and 11. We would define the starting point as 6 and limit the loop to go up to 10.

Let’s create a simple application to execute the logic above.

{{copy filename='code.go'}}
```go
package main

import (
	"fmt"
)

func main() {
	for i := 6; i < 11; i++ {
		fmt.Println(i)
	}
}
```
{{ /copy }}

The application iterates 5 times and increases the out by 1 each time.

Our application is now complete. Run it using the command below:

{{ execute }}
```
go run code.go
```
{{ /execute }}

The code above can be also written this way:

{{copy filename='code.go'}}
```go
package main

import (
	"fmt"
)

func main() {
	for i := 6; i <= 10; i++ {
		fmt.Println(i)
	}
}
```
{{ /copy }}

Next, we will discuss how to break from a loop.