---
title: Create a map

---


<!--

-->

This is the syntax for creating a Go map:

```go
map[KeyType]ValueType
```

Let’s create a map for a data set containing student names and their score. The student names are strings and scores are integers:

```go
studentsScore := map[string]int{
	"John": 82,
	"Jane": 85,
	"Kevin": 90,
	"Mary": 80,
	}
```

The map above has the name `studentScore`, and maps student names to their respective score. In other words, the name is the key and the score is the value. 

In the above example, all the keys have to be of type string and the values have to be of type int.

Let us create a simple application that stores mapped student data. Add the code below to create it:

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

	fmt.Println(studentsScore)
}
```
{{ /copy }}

The code above creates a struct `studentsScore` containing details of four students.

Use the following command to run the application:

{{ execute }}
```
go run code.go
```
{{ /execute }}

As you can see the code prints the map with the different keys and their values.

```go
map[John:82 Jane:85 Kevin:90 Mary:80]
```

Next, we will discover how to extract values from a map.