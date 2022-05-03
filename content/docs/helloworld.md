---
Title: "Hello World"
type: docs
weight: 1
---

# OPA By Example: Hello World via CLI

{{< columns >}}
Here's our first rego policy, which evaluates the `hello` rule. The complete policy code can be seen here.
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>


The given policy takes JSON input.
<br>
<br>
<br>
<br>
<br>
<br>

To evaluate the policy, use `opa eval` command. The input file and policy file are mentioned using `-i` and `-d` flags respectively. 

<br>

We are getting result as `true` since we are querying the rule `hello`
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
Results can be pretty printed using `--format pretty`
<--->

```
play.rego
1. package play
2. default hello = false
3. 
4. hello {
5.     m := input.message		
6.     m == "world"			
7. }							

```
<br>

```
input.json
1. {
2.     "message": "world"  		
3. }
```

```
Command: 
$ opa eval -i input.json -d play.rego "data.play.hello"
```

```
output.json
1. {
2.   "result": [
3.     {
4.       "expressions": [
5.         {
5.           "value": true, 	
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


```
$ opa eval --input input.json --data play.rego --format pretty “data.play.hello”
> true
```


{{< /columns >}}
