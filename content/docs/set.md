---
Title: "Set"
type: docs
weight: 4
---

# OPA By Example: Set

{{< columns >}}
<br>
Sets are unordered collections of unique values. Values can be in terms of scalars, variables, references, and composite values.
<br>
<br>
<br>
<br>

We have an set called `allowed_databases` which are defined using `{}`
<br>
<br>
<br>
<br>
The values inside the sets are looked up using `[]`

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

The `allow` rule is evaluated to `false` since database world doesn't exist in the set `allowed_databases`
<--->

https://play.openpolicyagent.org/p/V9ez0x0OGE
```
package play

default allow = false

allowed_databases = {"stagging",
 "referralcampaign"}



allow {
   allowed_databases[input.database]
}

```

```
input:
{
    "database": "world"
}

```

```
output: 
{
    "allow": false,
    "allowed_databases": [
        "referralcampaign",
        "stagging"
    ]
}

```
{{< /columns >}}