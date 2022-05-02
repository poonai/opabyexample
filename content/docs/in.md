---
Title: "In"
type: docs
weight: 13
---

# OPA By Example: In

{{< columns >}}

**Import Statement:** - import future.keywords.in

The membership operator `in` lets you check if an element is part of a collection (array, set, or object). 

<br><br><br><br><br><br>

It always evaluates to either `true` or `false`, not `undefined`.

<--->

```
values := [] {
    val1 := 404 in [404, 200, 403]	#array
    val2 := “dgraph” in {“inspektor”, 
                        “opa”, 
                        “signoz”}
    val3 := “poonai” in {
        “mentor”: “poonai”, 
        “mentee”: “zriyansh” 
        }
}
```

```
output.json
{
  "values": [
    true,
    false,
    true
  ]
}
```






