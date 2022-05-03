---
Title: "Every"
type: docs
weight: 9
---

# OPA By Example: Every

{{< columns >}}


The every keyword is used to state explicitly that the body of the element is true for all elements in the domain. 

It will go over the domain, bind its variables, and verify with it's body constraints. 

If any of the bindings fails to result in a successful body evaluation, the total statement is undefined.

<br>

we are validating none of the user is `contractor`
<--->
https://play.openpolicyagent.org/p/LNJ9Tdosd2

```
package play
import future.keywords.every









allow {
    every user in {"admin", "dev", "support"} {
      user != "contractor" 
    } 
}
```
```
output:
{
    "allow": true
}
```