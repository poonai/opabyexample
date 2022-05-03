---
Title: "Every"
type: docs
weight: 9
---

# OPA By Example: Every

{{< columns >}}

**Import Statement:** <br> `import future.keywords.every`
- Introduces the every keyword to the policy file.

- Importing every means also importing in without an extra import statement.

The every keyword is used to state explicitly that the body of the element is true for all elements in the domain. 

It will go over the domain, bind its variables, and verify that the body is consistent with those constraints. 

If any of the bindings fails to result in a successful body evaluation, the total statement is undefined.

**Note:** Negating every is forbidden.

<--->


```
Example:
scope {
    every x in {1, 2, 3} {
    x != 4 
    } 
}
```
```
Evaluates to:
{ 
    “scope”: true 
    }
```