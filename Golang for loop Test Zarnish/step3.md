---
title: Create an infinite for loop with a break

---
<!--

-->

Unless we break a for loop it will run infinitely. Break in a loop means exiting the loop at a set point to stop it from running infinitely.

Failure to break can lead to an application crashing midway before completing the execution of the code within its scope.

Below is an example of a for loop that breaks at a set point.

{{copy filename='code.go'}}
```go
package main
 
import "fmt"
 
func main() {
	k := 3
	for {
		fmt.Println("Continue")
		if k == 8 {
			break
		}
		k++
	}
}
```
{{ /copy }}

The for loop in the application above is not restricted and thus would print 'Continue' infinitely unless we break from inside the loop. We break when the counter gets to 8.

Run the application using the following command:

{{ execute }}
```
go run code.go
```
{{ /execute }}

To infinitely run some specified instruction without a break, we only need to remove the `break` instruction with the surrounding condition:

{{copy filename='code.go'}}
```go
package main

import "fmt"

func main() {
	k := 3
	for {
		fmt.Println("Continue")
		k++
	}
}
```
{{ /copy }}

Run the application using the following command:

{{ execute }}
```
go run code.go
```
{{ /execute }}

Next, we will discuss the key takeaways.