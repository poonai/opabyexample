---
Title: "In"
type: docs
weight: 13
---

# OPA By Example: In

{{< columns >}}

The membership operator `in` lets you check if an element is part of a collection (array, set, or object). 

It always evaluates to either `true` or `false`, not `undefined`.

<br>
<br>
<br>
<br>
<br>

checking whether `delete` exist in the array `allowed_statements`

<--->
https://play.openpolicyagent.org/p/iGDupYLFkK
```
package play 

import future.keywords.in

allowed_statements = ["query", "update", "insert"]

default allow = false 

allow {
    "delete" in allowed_statements
}
```

```
output.json
{
    "allow": false,
    "allowed_statements": [
        "query",
        "update",
        "insert"
    ]
}
```






