---
title: Extract values from a struct

---
<!--

-->

Sometimes you’ll need just one value from a struct. This can be important when you want to use selected values that are stored within the struct.

Let us create an application that extracts the student name and the first subject from a struct. We do this using the code below:

{{copy filename='code.go'}}
```go
package main

import (
	"fmt"
)

type Student struct {
	grade int
	name string
	subjects [] string
	}

func main() {

	aStudent:= Student {
			grade: 3,
			name: "John",
			subjects: []string {
				"English",
				"Maths",
				"Chemistry",
				"Biology",
				},
			}

//Extracting student name
fmt.Println(aStudent.name)
{{ highlight }}
//Extracting the student’s first subject
fmt.Println(aStudent.subjects [0])
{{ /highlight }}
}
```
{{ /copy }}

Our application is now complete. Add the command to compile the application.

{{ execute }}
```
go run code.go
```
{{ /execute }}

Next, we'll look at the key takeaways.