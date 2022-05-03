---
Title: "Else"
type: docs
weight: 12
---

# OPA By Example: Else

{{< columns >}}

Remember **if**, **else if**, **elif**, **else** and all other forms of conditional statements? 

Rego just has one, `else`

`else` is used in similar fashion as in every typical programming language, when you wish to check multiple bodies of the rule.


**Note:**
- To avoid ambiguity, make sure to use the form else = when using an else statement.

- There is no limit imposed on the number of else clauses on a rule.

<--->
https://play.openpolicyagent.org/p/HLnVL4jjtl
```
package play 

default allow = false

allow {
   input.role = "admin"
} else {
   input.role = "special-user"
}

```

```
input.json
{
    "role": "special-user"
}
```

```
output:
{
    "allow": true
}
```










