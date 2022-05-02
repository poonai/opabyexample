---
Title: ":= OR == OR ="
type: docs
weight: 14
---

# OPA By Example: := OR == OR =

{{< columns >}}


## Assignment (:=)
The assignment operator (:=) is used to assign values to variables. 

Scope = local. 



## Comparison (==)
Comparison checks if two values are equal within a rule or not. 


<br><br><br>

## Unification (=)
Unification combines assignment and comparison. 

Also, 

Note: It is generally advised not to use unification operator if other 2 are sufficient for defining rules.

(An excerpt from official OPA docs:)
### Best Practices for Equality.

| *        | Compiler Errors            |   Use Case        |
| -------- | -------------------------- |  ---------------  |
| :=       |  Var already assigned      |   Assign variable |
| ==       |  Var not assigned          |   Compare values  |
| =        |  Values cannot be computed |   Express query   |

**Note:** Each of the 3 operators can be used everywhere.

<--->
```
assign {
    val != 100
    val := 10     # error because val appears earlier in the query.
    val := 20     # error because val is assigned twice.
}
```

```
comp {
    val := “opa”
    val == “opa”   # true because val refers to the local variable
}
```

```
{ "comp": true }
```

```
a := 2
a  = 2 
// Both the above state true 
// and valid in rego, 
// both creates a variable 
// and assigns 2 to it. 
```

```
404 == 404
404 = 404
// Both the above state true 
// and valid in rego, 
// checks for comparison. 
```







