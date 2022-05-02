
---
Title: "Run Rego"
type: docs
weight: 3
---

# OPA By Example: Run Rego

{{< columns >}}


The simplest way to interact with OPA is via the command-line using the ```opa eval``` sub-command

The output generated, when we run the query, is JSON formatted.

Explanation.
> Here, ```“value”: false```, indicates that the condition we were testing for is not true.

<br>
<br>

<strong>line 6: </strong><br>
```false``` as 1 is not greater than 2, condition not satisfied.
<--->

```
command
$ opa eval '1 > 2'

```


```
Output.json
1. {				
2.   "result": [
3.    {
4.      "expressions": [
5.        {
6.          "value": false,   	
7.          "text": "1 \u003e 2",
8.          "location": {
9.            "row": 1,
10.            "col": 1
11.          }
12.       }
13.      ]
14.    }
15.  ]
16.}

```

{{< /columns >}}
