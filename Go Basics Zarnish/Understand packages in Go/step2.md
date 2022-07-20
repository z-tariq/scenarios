---
title: How to import packages

---

<!--

-->

There are many Go packages that are available and can easily be added to an application. You can get documentation for all the libraries built into Go on [pkg.go.dev](http://pkg.go.dev) or by using the godoc command that we will see in one of the next scenarios.

You import a package by using the ‘import’ command. Enter this command to import the `fmt` library that is used when working with strings.

{{copy filename='code.go'}}
```go
package main
{{ highlight }}
import (
	"fmt"
)
{{ /highlight }}
```
{{ /copy }}

Next, we’ll look at how to handle blank package import.