---
Title: "Input"
type: docs
weight: 2
---

# OPA By Example: Input

{{< columns >}}


```input``` - global variable representing JSON policy query.<br>
```data``` - global variable containing external data.

- here, ```servers``` is a JSON data object with some array values associated with it.

<br><br><br>

- validating input JSON data using global variable ```input```.
<--->

```
examples
1. s0 := input.servers[0]
2. s1 := input.servers[1]	

```


<br><br><br><br>

```
1. input.servers[0].id == "app"
```

{{< /columns >}}