---
title: Extract values from a map

---
<!--

-->

In some cases, you’ll want to work with one single value from a map for other logic implementations. For instance, you may want to code an application that extracts the score of a single student after their name has been entered. In such a case, we locate the value within the map using its key.

If you wanted to get Jane’s score only, you can do it by adding the code below.

{{copy filename='code.go'}}
```go
package main

import (
	"fmt"
)

func main() {

	studentsScore := map[string]int{
		"John":  82,
		"Jane":  85,
		"Kevin": 90,
		"Mary":  80,
	}
{{ highlight }}
	// Extracting a single student score using the key
	fmt.Println(studentsScore["Jane"])
{{ /highlight }}
}
```
{{ /copy }}

Run the application using the following command.

{{ execute }}
```
go run code.go
```
{{ /execute }}

The line `fmt.Println(studentsScore["Jane"])` instructs the application to extract the value mapped by key `Jane` and that's what we should see on the output.

Next, we’ll discuss how to create a struct.