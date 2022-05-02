---
Title: "Default"
type: docs
weight: 11
---

# OPA By Example: Default

{{< columns >}}

**Syntax:** 
`default <rule name> = <value>`

If the rule body is not satisfied, it is `undefined`, in which case the `default` value is assigned if the `default` value is specified.

<br>

When the allow document is queried, the return value will be either `true` or `false`

<br><br><br><br><br><br><br>

The allow document would be `undefined` for the same input if it didn't have a default definition.

<--->

```
default allow := false
request_method {
    input.user == "zriyansh"
    input.method == "POST"
}

allow {
    input.user == "poonai"
}
```

```
{
   "user": "poonai",
   "method": "POST"
}
```

```
false 
// as poonai doesn’t have the 
// rights to use method POST.
```



