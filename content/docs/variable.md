---
Title: "Variables"
type: docs
weight: 8
---

# OPA By Example: Variables

{{< columns >}}

The variables in Rego differ from those in a typical programming language. 

Rego finds a value for a variable that makes all expressions evaluated as `true`, and if not found, the variable becomes `undefined`.

- String <br>
- Number <br>
- Boolean <br>
- Null <br>
- Array - A list of values. <br>
- Object - A dictionary mapping strings to values. <br>
- Set - An unordered collection of distinct values.<br>



Variables are immutable. Do not assign them twice. Variables cannot be changed once assigned. 










<--->

```
s = "a string"				
n == 17.35 					
b := true 					
U := null 					
a := [1,1,2,3] 				
e := {1,2,3} 				
d := {["user": "om", "path": ["/", "dogs"]} 
```


```
// Example: 
// Assignment (:=) assigns a variable to a value
x := 1
x := 2 	// COMPILER ERROR


```