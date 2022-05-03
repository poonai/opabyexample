---
Title: "Input"
type: docs
weight: 3
---

# OPA By Example: Input

{{< columns >}}

The provied input json is binded to the global variable called `input`. The respective property are accessed using `.` (dot) operator.

<br>

The `message` property is assigned to variable `m`. 

<--->

```
package play

default hello = false

hello {
    m := input.message
    m == "world"
}

```

```
input.json

{
    "message": "world"
}
```

```
output 

{
    "hello": true
}
```

{{< /columns >}}