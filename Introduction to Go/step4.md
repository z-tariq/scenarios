---
title: Your First Go Program
---
Let's start with some actual coding and write our first program in Go.

{{ copy filename='helloWorld.go'}}
```
package main
import (
   "fmt"
)
func main(){
    fmt.Println("Hello from Brainarator !!")
}
```
{{ /copy }}

We'll look into the components of this file in detail in the upcoming scenarios, for now lets just move on and run our program.

You can run your code with the following command:

{{execute}}
```
go run helloWorld.go
```
{{/execute}}

You can see the following output on your screen.

```
Hello from Brainarator !!
```

That was a brief introduction to Go and a sample program, we'll look into the components of this basic program including packages and imports in the upcoming scenarios.

Happy Learning!

