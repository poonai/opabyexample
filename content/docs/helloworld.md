---
Title: "Hello World"
type: docs
weight: 1
---

# OPA By Example: Hello World

{{< columns >}}



Go is an open source programming language designed for building simple, fast, and reliable software.

Please read the official documentation to learn a bit about Go code, tools packages, and modules.

Go by Example is a hands-on introduction to Go using annotated example programs. Check out the first example or browse the full list below.

<--->

```go
package main

import "fmt"

func main() {
    fmt.Println("hello world")
}

```
```
$ go run hello-world.go
hello world

$ go build hello-world.go
hello-world         hello-world.go

$ ./hello-world
hello world

```

