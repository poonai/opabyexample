---
Title: "Else"
type: docs
weight: 12
---

# OPA By Example: Else

{{< columns >}}

Remember **if**, **else if**, **elif**, **else** and all other forms of conditional statements? 

Rego just has one, `else`

Here, `else` is used in similar fashion as in every typical programming language, when you wish to check multiple rules or rule bodies for a given condition. 

Connect multiple rule bodies with an `else` statement and check the conditions on the next body when the conditions on the first rule body are not satisfied.

**Note:**
- To avoid ambiguity, make sure to use the form else = when using an else statement.

- There is no limit imposed on the number of else clauses on a rule.

<--->
```
rule.rego
default is_swapped = false
is_swapped = {
	a == 5
	b == 10 
} else {
	a := 5
	b := 10
}
```

```
input.json
{ 
    “a”: “10”,  “b” :”5” 
}
```

```
output.json 
> true
```










