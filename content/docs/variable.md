---
Title: "Variables"
type: docs
weight: 4
---

# OPA By Example: Variables

{{< columns >}}

The variables in Rego differ from those in a typical programming language. variable can be input or output. If the value provided by the to policy then it is considered as input, otherwise it considered as output. 

<br>
<br>

Value to a variable is assigned using `:=` .
<br>
 array is assigned to the variable `site`

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

The policy only resulted `sites` variable not `current_user` variable becauase `current_user` is considered as input variable


<--->

<br>
<br>
<br>
<br>
<br>
<br>
https://play.openpolicyagent.org/p/E0VhMNnjqq

```
package play

sites := [
    {"name": "prod"},
    {"name": "dev"}
]

```


```
input: 
{
    "current_user": "poonai"
}
```

```
output: 
{
    "sites": [
        {
            "name": "prod"
        },
        {
            "name": "dev"
        }
    ]
}
```