
---
Title: "Rules"
type: docs
weight: 7
---

# OPA By Example: Rules

{{< columns >}}

In the right side example, <br> ```max``` is the head and statements inside are the ```body```. <br>
In Rego we say the rule head is ```true``` if the rule body is true for some set of variable assignments. <br> <br>
<strong>Note:</strong> If one condition evaluates to ```true``` but second evaluates to ```false``` or ```undefined```, the entire rule max evaluates to ```undefined``` and not ```false```.

- Rego lets you encapsulate and re-use logic with rules. 
- Rules are just if-then logic statements. 
- Rules can either be “complete” or “partial.
- Every rule consists of a head and a body. 

<br><br>

## Functional Rules:
Functional rules let you extend the set of built-in functions. <br>
<strong>Example - 1.</strong> <br>

<br><br><br><br><br><br><br>
<strong>Example - 2.</strong> <br>


<--->


```
policy.rego
package play
	max {
	a := input.x
   	b := input.y
   	a < b			# true 	AND
	b -1 == a		# true
}
```

```
input.json
{
    "x": "1"
    "y": "2"
}
```

```
output.json
{
    "max": true
}

```

<br><br>

```
dist_sys (“inspektor.com”)

dist_sys(r) { 
    r == “inspektor.com” 
    }

// BOTH THE ABOVE LINES ARE EQUIVALENT, 
// rule body is optional. 
```


```
safe_repo(p) = true {...}
safe_repo(p) = 	    {...}

// Again, both the above lines are the same 
// because, by default, the return value is true.


```



{{< /columns >}}