---
author: "andy winarko"
date: 2019-01-19
title: Go print typeof object
---

> The Go reflection package has methods for inspecting the type of variables. The following snippet will print out the reflection type of a string, integer and float.

```go
package main

import (
    "fmt"
    "reflect"
)

func main() {

    tst := "string"
    tst2 := 10
    tst3 := 1.2

    fmt.Println(reflect.TypeOf(tst))
    fmt.Println(reflect.TypeOf(tst2))
    fmt.Println(reflect.TypeOf(tst3))

}
```
more documentation https://golang.org/pkg/reflect/#TypeOf