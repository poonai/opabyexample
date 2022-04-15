---
Title: "Set"
type: docs
weight: 4
---

# OPA By Example: Set

{{< columns >}}


Dot(.) is shorthand for Brackets []. 

Rego makes ```x.y``` into ```×["y"]```

- In practice, dot(.) is used <strong>only</strong> with objects, not arrays or sets.

- Brackets [] inspects sets.


<--->

```js
examples
e  := {13,23,33} 
st := {"cat", "dog", "rabbit"}

```

```js
st["cake"] 	// "cake"

```

```js
key := "India"
st[key] 		// “India”

```


{{< /columns >}}