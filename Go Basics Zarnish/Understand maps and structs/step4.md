---
title: Create a struct

---
<!--

-->

This is a collection type that is used to handle different types of data together. Other collection types in Go require consistency in the type of data that they handle.

Assume you want to store students’ information that is composed of their name, grade, and the subjects they are taking. In this case, the grade would be an int, the name would be a string and the subjects would be an array.  This can be represented by this struct code:

```go
type Student struct {
	grade int
	name string
	subjects [] string
	}
```

Let us now create a simple application that adds a student’s data to a struct. Use the code below to do that.

{{copy filename='code.go'}}
```go
package main

import (
	"fmt"
)

type Student struct {
	grade    int
	name     string
	subjects []string
}

func main() {

	aStudent := Student{
		grade: 3,
		name:  "John",
		subjects: []string{
			"English",
			"Maths",
			"Chemistry",
			"Biology",
		},
	}
	//Print all the student details
	fmt.Println(aStudent)
}
```
{{ /copy }}

The application adds a single student's data to the struct `aStudent`.

Run the application using this command:

{{ execute }}
```
go run code.go
```
{{ /execute }}

Next, we’ll discuss how to extract values from a struct.