---
title: Blank package import

---


<!--

-->

If you import a package and it is not used in the application the compiler will give you an error. There are times in Go when we may import a package but not use it as expected in the application. In cases, where you may wish to run the application without removing the import, you use blank imports. 

Below is an example with a blank import:

{{copy filename='code.go'}}
```go
package main

import (
	"fmt"
	_ "strings"
)

func main() {
	fmt.Println("Hello")
}
```
{{ /copy }}

The blank import `strings` is denoted by a `_` before its name.

Run the application using the command below:

{{ execute }}
```
go run code.go
```
{{ /execute }}

Next, we'll look at the key takeaways.