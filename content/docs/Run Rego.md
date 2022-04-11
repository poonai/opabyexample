
---
Title: "Run Rego"
type: docs
weight: 3
---

# OPA By Example: Run Rego

{{< columns >}}
we get output as JSON formatted data.

false, as 1 is not greater than 2, condition not satisfied


Explanation :-
> Here, “value”: false, indicates that the condition we were testing for is not true.


<--->

```rego
command
$ opa eval '1 > 2'

```


```rego
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
