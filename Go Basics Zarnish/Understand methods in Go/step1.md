---
title: Introduction

---
<!--

Introduction

-->

A method in Go is a function with a receiver argument. In fact, a receiver argument is the only difference between a method and a function.

**Function:**

```
func func_name(arguments) return_values
```

**Method:**

```
func (receiver receiver_type) func_name(arguments) return_values
```

A receiver can be any data type (e.g. a struct). The method will have access to the properties of the receiver and can call the receiver’s other methods.

There are two types of methods:

- **Values receivers:** they only do calculations using the values received.
- **Pointers receivers:** they do calculations on values received but have the option of altering the received values using a pointer.

A value receiver creates a copy of values and stores them in a different location. This is inefficient when working with large structs because it'll slow down the program.

A pointer receiver passes the address of the data to and doesn't need more memory space to be allocated. This is efficient when working with large structs because values aren't copied with each method call.

Next, we discuss the method structure.