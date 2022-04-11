---
Title: "Input"
type: docs
weight: 2
---

# OPA By Example: Input

{{< columns >}}



input - global variable representing JSON policy query
data - global variable containing external data

where “servers” is a JSON data object with some array values associated with it.

validating input JSON data using global var input.
<--->

```rego
examples
1. s0 := input.servers[0]
2. s1 := input.servers[1]	

```

```
1. input.servers[0].id == "app"
```

