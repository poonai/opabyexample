---
Title: "Set"
type: docs
weight: 4
---

# OPA By Example: Set

{{< columns >}}
Sets are unordered collections of unique values. 


Line 1: `e` is a scalar set.

Line 2: `st` is a set of strings.

Line 3: checks if `cake` is present in the set or not.

In rego, Sets can be defined in terms of scalars, variables, references, and composite values.

Dot(.) is shorthand for Brackets []. 

Rego makes ```x.y``` into ```×["y"]```

- In practice, dot(.) is used <strong>only</strong> with objects, not arrays or sets.

- Brackets [] inspects sets.


<--->

```
1. e  := {13,23,33} 
2. st := {"cat", "dog", "rabbit"}

```

```
3. st["cake"] 	// "cake"

```

```
4. key := "India"
5. st[key] 		// “India”

```


{{< /columns >}}