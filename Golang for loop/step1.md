---
title: Introduction

---
<!--

-->

Looping allows for repeated execution of a code block. This can be used when we are searching for an item inside a collection or a string. We can iterate over a map, an array, a slice, or a collection when searching for a specific element.

Go only has the for loop and doesn’t contain a while loop like other languages. This is because the for loop will work the same way when used with a single condition.

This is the structure of a basic for loop:

```go
for i:= 0; i < 6; i++{
}
```

From the above code snippet:

`i := 0` initializes the variable that we shall use.

`i < 6` gives a boolean type result that determines if the block is executed.

`i++` sets the initialized variable to be a counter. This will enable auto-increment on the variable and also stop code execution just before the condition `i < 6` is no longer true (e.g `i==6`).