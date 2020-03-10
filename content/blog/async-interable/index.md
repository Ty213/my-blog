---
title: Async Iterators 
date: "2020-03-09"
description: "Async Iiterators (for await... of)"
---

I needed a way to loop over data in an array and perform a asynchronous function on each item.
for await...of will allow you to await a function inside of the for loop.

`for await (variable of iterable) {
  statement
}
`

variable: is the name given to each item.
iterable: the object to be iterated over. (array, set, object)


For more information:
[for await...of mozilla docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/for-await...of)

