---
title: Introduction

---
<!--

Introduction

-->

Pointers are variables that are used to store the memory location address of other variables. But why do we need pointers? 

In Go, you’ll sometimes need a copy of the data to work with while still keeping the original unchanged. This is achieved in two ways:

- Passing data by value
- Passing data by reference

**Passing by value**

For instance, when you want to check why a student failed to hit the target score required to pass in a semester, you can add a few hypothetical scores to get a clearer picture. However, you’d still want to keep their original score intact. In this case, we send the hypothetical scores to the function and not the actual variable. That is called passing the value to the function.

**Passing by reference**

Another practical use case is when you have an application that calculates an account’s balance after a withdrawal or a deposit is made in one of its functions. In this case, you want your function to access the actual balance directly. To do that, point the function to where the balance is stored in the memory instead of passing it as a value. The function will then alter the balance after computing the new balance.

Next, we’ll look at how to create a pointer.