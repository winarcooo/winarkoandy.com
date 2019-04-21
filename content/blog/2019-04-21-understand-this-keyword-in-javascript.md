+++
author = "andy winarko"
title = "Understand `this` keyword in Javascript"
description = ""
tags = [
    "javascript",
    "basic",
]
date = "2019-04-21"
categories = [
    "programming",
    "javascript",
]
+++
---
```js
/**
 * * Understand `this` and `bind` in javascript
 * `this` is reference to context where are you now
 * `bind` is property on a function 
 */
const button = {
    onClick: null
};

const dragon = {
    element: 'dirt',
    // technically breath property(which is a function) is know nothing about other property in this dragon object
    // they dont magically connect each other like class in java, or php.
    // but in this scope, this.element reference to dragon object (element property)
    breath: function() {
        console.log(`i am breathing ${this.element}`);
    }
};

const godzila = {
    element: 'fire',
};

// `bind` is a property on a function

/** 
 * doing this way, will return undefined, 
 * because `this` in dragon.breath doesn't reference `this` to dragon object
 * even it in dragon property but it still just a normal function
*/
button.onClick  = dragon.breath // return "i am breathing undefined"

/**
 * here `bind` come to the rescue,
 * we use bind in a function (dragon.breath is a function)
 * and bind any of `this` reference on dragon.breath function to dragon object
 * in this case element property in dragon object
 * so `this` will return `dirt`
 */
button.onClick = dragon.breath.bind(dragon); // return "i am breathing dirt"
button.onClick()
```
---