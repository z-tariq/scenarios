---
title: Understand pointer receiver method

---
<!--

Understand pointer receiver method

-->

The pointer receiver method allows for the modification of values that the receiver is pointing to. 

In other words, pointer receiver methods can update the value to which the receiver points.

This method is created by adding an asterisk  `*` before the struct name that is between the parenthesis.

This is a value receiver method:

```go
func (s Scores) Average() int {
	return((s.English + s.Maths + s.Chemistry + s.Geography)/4)
}
```

This is a pointer receiver method:

```go
func (s *Scores) Average() int {
	return((s.English + s.Maths + s.Chemistry + s.Geography)/4)
}
```

Let's create an application that allows us to modify the score of the student and calculate a new average based on it.

Add the code below to create a pointer receiving method:

{{copy filename='code.go'}}
```go
package main

import (
	"fmt"
)

type Scores struct {
	English, Maths, Chemistry, Geography int
}

//value receiver method
func (s Scores) Average() int {
	return ((s.English + s.Maths + s.Chemistry + s.Geography) / 4)
}

//pointer receiver method
func (s *Scores) newChemistryScore(newScore int) {
	s.Chemistry = newScore
}

func main() {
	s := Scores{69, 82, 65, 68}
	fmt.Println(s.Average())

	//Change the student's chemistry score
	s.newChemistryScore(82)
	fmt.Println(s.Average())
}
```
{{ /copy }}

The above code has two methods, `Average()` and `newChemistryScore()`. The first method calculates the average score and the second method alters the chemistry score.

The `newChemistryScore()` method has no return value because it is created to modify a variable. This is achieved by omitting the return type statement while creating the method.

Run the application using the following command:

{{ execute }}
```
go run code.go
```
{{ /execute }}

Next, we’ll discuss how to the key takeaways.