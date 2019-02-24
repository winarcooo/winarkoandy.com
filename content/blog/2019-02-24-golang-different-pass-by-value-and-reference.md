+++
author = "andy winarko"
title = "Golang Pass-by-value vs Pass-by-reference"
description = ""
tags = [
    "go",
    "golang",
    "snippet",
]
date = "2019-02-24"
categories = [
    "golang",
]
+++
---

Sedikit menjelaskan aja, perbedaan mendasar pass-by-value & by-rerefence dalam golang.

### Passing by value

```go
package main

import "fmt"

type Person struct {
	firstname string
	lastname  string
}

func changeName(p Person) {
	p.firstname = "Bob"
}

func main() {
	person := Person{
		firstname: "Alice",
		lastname:  "Dow",
	}

	changeName(person)  // function ini hanya mengambil copy dari variable person

	fmt.Println(person)
}
```

Output dari code diatas,

```
{Alice Dow}
```

bisa dilihat, function `changeName` yang ada di `main` gak mengubah sama sekali firstname dari person. Ini karena `changeName` mengubah copy dari variable person, bukan varible person itu sendiri.

---

### Passing By Pointer

```go
package main

import "fmt"

type Person struct {
	firstname string
	lastname  string
}

func changeName(p *Person) {
	p.firstname = "Bob"
}

func main() {
	person := Person{
		firstname: "Alice",
		lastname:  "Dow",
	}

	changeName(&person)  // function ini menunjuk ke variable yg sama

	fmt.Println(person)
}
```
Output dari code diatas,

```
{Bob Dow}
```

disini, variable person di function `main` berubah karena function `changeName`, ini karena menunjuk ke variable yang sama.

---