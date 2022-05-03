
---
Title: "Negation"
type: docs
weight: 5
---

# OPA By Example: Negation

{{< columns >}}
Negation keyword `not` does the following

- ```not``` turns ```undefined``` into ```true```.
- ```not``` turns ```false``` into ```true```.
- ```not``` turns everything else into ```undefined```.

<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>

`deny` rule is evaluated to `true` because `not` keyword turned the `false` into `true`


<--->
https://play.openpolicyagent.org/p/cpyuU3Yi8S
```
package play

allowed_admins = {"poonai",
 "priyansh"}

deny {
   not allowed_admins[input.user]
}
```

```
input.json 
{
    "user": "hacker"
}
```

```
output:
{
    "allowed_admins": [
        "poonai",
        "priyansh"
    ],
    "deny": true
}
```

{{< /columns >}}