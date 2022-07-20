---
title: Understand the value receiver method

---
<!--

Understand the value receiver method

-->

Just like a function, a simple method starts with the word `func`. It is then followed by parenthesis that contains the struct that will handle the value it will be receiving. This is followed by the name of the method. The last value is the type of value that the method will return.

Example:

```go
func (s Scores) Average() int {
}
```

Let's create a value receiver method that computes a student’s average score. To do this we need to create a struct that holds all the student scores and a method containing mean calculation formula.

The student’s score values are passed from the main function to the method using the struct defined when creating a method.

Add the code below to create a struct containing all the subjects that the student is taking:

{{copy filename='code.go'}}
```go
package main

import (
	"fmt"
)

type Scores struct {
	English, Maths, Chemistry, Geography int
}

func (s Scores) Average() int {
	return ((s.English + s.Maths + s.Chemistry + s.Geography) / 4)
}

func main() {
	s := Scores{69, 82, 65, 68}
	fmt.Println(s.Average())
}
```
{{ /copy }}

The code above has the score of four subjects a student is taking represented as variables of type int. `Average()` is a value receiver method that takes all the scores, computes the average, and returns it as an int type.

Run the application using the command below:

{{ execute }}
```
go run code.go
```
{{ /execute }}

Next, we’ll discuss how to create a pointer receiver method.