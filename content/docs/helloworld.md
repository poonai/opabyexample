---
Title: "Hello World"
type: docs
weight: 1
---

# OPA By Example: Hello World via CLI

{{< columns >}}

<br>
<br>
<br>

<br>

- Input message (from input.json file) is assigned to a variable ```m```.
- Compares ```m``` with a string. <br>
<strong>Note</strong>: Each rego line is like a IF statement, if condition is satisfied, rule is validated.

- The ```:=``` syntax is shorthand for declaring and initializing a variable.

<br>

- The input value provided by us, here we passed “message” value.

<br><br><br><br><br><br><br><br><br><br><br><br>
<strong>in line 5: </strong> ```true``` condition satisfied

<br><br><br><br><br><br><br><br><br><br>
<strong>OR </strong> 
use this command for a better and direct output.

<--->

```js
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
<br>
<br>
<br>

```js
input.json
1. {
2.     "message": "world"  		
3. }
```

```js
Command: 
$ opa eval -i input.json -d play.rego "data.play.hello"
```

```js
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


```js
$ opa eval --input input.json --data play.rego --format pretty “data.play.hello”
> true
```


{{< /columns >}}
