
---
Title: "Some"
type: docs
weight: 6
---

# OPA By Example: Some Keyword

{{< columns >}}

Consider an array:-  <br>
```projects = [“inspektor”, “dgraph”, “opabyexample”]```


<br><br><br><br>

<strong>Note:</strong> OPA figures out that it has to iterate over the entire projects[] array by itself.

<strong>Points to remember:</strong>
- Rego has no side-effects. 
- In Rego you use loops for checking a condition, possibly recording the location. 
- Generating new JSON out of existing JSON.



<--->


```js
Iterative approach (in programming languages):
for i in len(projects): 
    if input["repo"] == projects[i]:
        return true
return false

```

```js
Declarative approach (in Rego):
is_open_source{
    some i
    input.repo == projects[i]	
}

```

{{< /columns >}}