---
Title: "Hello World via CLI"
type: docs
weight: 1
---

# OPA By Example: Hello World via CLI

{{< columns >}}



Input message (from input.json file) is assigned to a variable 'm'.


compares ‘m’ with string.
Note: Each rego line is like a IF statement, if condition is satisfied, rule is validated.

The <strong>:=</strong> syntax is shorthand for declaring and initializing a variable.


the input value provided by us, here we passed “message” value.

<--->

```rego
play.rego
1. package play
2. default hello = false
3. 
4. hello {
5.     m := input.message		
6.     m == "world"			
7. }							

```

```rego
input.json
1. {
2.     "message": "world"  		
3. }
```

```rego
Command: 
$ opa eval -i input.json -d play.rego "data.play.hello"
```

```rego
output.json
1. {
2.   "result": [
3.     {
4.       "expressions": [
5.         {
5.           "value": true, 		# true, condition satisfied
6.           "text": "data.play.hello",
7.           "location": {
8.             "row": 1,
9.            "col": 1
10.          }
11.         }
12.       ]
13.     }
14.   ]
15. }
```
OR use this for a better and direct output	
```rego
$ opa eval --input input.json --data play.rego --format pretty “data.play.hello”
> true
```

