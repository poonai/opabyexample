---
Title: "Default"
type: docs
weight: 11
---

# OPA By Example: Default

{{< columns >}}

`default` keyword is used to assign default value for the rule.

<br>
<br>

`false` is assigned to the rule `allow`

<--->
https://play.openpolicyagent.org/p/LNJ9Tdosd2

```
package play 

default allow = false

```

```
output:
{
    "allow": false
}
```



