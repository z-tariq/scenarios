---
title: Define the application's entry package

---


<!--

-->

In this scenario, we will discuss how to create and handle packages. This is important because Go applications are structured in packages. 

A package is composed of source files in the same directory that are compiled together. Functions, types, variables, and constants defined in one source file are visible to all other source files within the same package.

We’ll start by defining a package that will serve as an entry point to our application. Add the following code to add a package named ‘main’:

{{copy filename='code.go'}}
```go
package main
```
{{ /copy }}

Next, we’ll look at how to handle imports.