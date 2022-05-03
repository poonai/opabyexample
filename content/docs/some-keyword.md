
---
Title: "Some"
type: docs
weight: 6
---

# OPA By Example: Some Keyword

{{< columns >}}

The `some`  keyword allows queries to explicitly declare local variables.

Consider `some` as a looping structure like for loop in any programming language. 

```
Iterative approach:
for i in len(projects): 
    if input["repo"] == projects[i]:
        return true
return false

```


```
Declarative approach (in Rego):
is_open_source{
    some i
    input.repo == projects[i]	
}

```

<br>
<br>

`is_open_source` rule is evaluated to true since `input.project` is present in 
`opensource` array

<--->

https://play.openpolicyagent.org/p/89TGWKWF9U

```
package play

opensource = ["inspektor",
 "opabyexample",
  "awesome-os"]

is_open_source { 
   some i
   opensource[i] == input.project
}
```

```
input.json
{
    "project": "inspektor"
}
```
<br>
<br>

```
output:
{
    "is_open_source": true,
    "opensource_projects": [
        "inspektor",
        "opabyexample",
        "awesome-os"
    ]
}
```
{{< /columns >}}