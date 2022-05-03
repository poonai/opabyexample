
---
Title: "Rules"
type: docs
weight: 7
---

# OPA By Example: Rules

{{< columns >}}

In OPA, rules are the policy result. You can simply assign a value to rule or you can assign a value based on 
some condition. 
<br>
<br>

 the value `inspektor` assigned to the rule `project` directly.

<br>

`is_athuor` rule is evaulated based on the input. if the `author` is set to `poonai` then the value is set to `true`, otherwise `false`
<--->

https://play.openpolicyagent.org/p/H2FDgC8RkH
```
package play

project = "inspektor"

default is_author = false



is_author {
   input.author == "poonai"
}
```

```
input.json
{
    "author": "poonai"
}
```

```
{
    "is_author": true,
    "project": "inspektor"
}
```

{{< /columns >}}