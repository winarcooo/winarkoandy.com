+++
author = "andy winarko"
title = "Re-created new keyword in JS"
description = ""
tags = [
    "javascript",
    "basic",
]
date = "2019-04-24"
categories = [
    "programming",
    "javascript",
]
+++
---
```js
function Person(saying) {
  this.saying = saying
}

Person.prototype.talk = function() {
  console.log('I say:', this.saying);
}

// replicate what `new` does
function spawn(constructor) {
  // 1. create a new object
  var obj = {}
  // 2. set the prototype
  Object.setPrototypeOf(obj, constructor.prototype)

  var argsArray = Array.prototype.slice.apply(arguments)
  // 3. execute constructor with `this`
  // 4. return the created object, unless the constructor return the object
  return constructor.apply(obj, argsArray.slice(1)) || obj
  
}

var crockforg = spawn(Person, 'semicolans1!!')
crockforg.talk()
```
---