---
Title: "With"
type: docs
weight: 10
---

# OPA By Example: With

{{< columns >}}

In rego, the `with` statement is used to overwrite input or data with specific data. 

When writing unit tests, the `with` statement is frequently used.

It acts as a modifier on expressions.

<br><br>

The following expression evealuates to `true`. 

<br><br>

While writing tests -->

<--->

```
allow with input as {
    "user": "poonai", 
    "method": "POST"
    } with data.roles as {
        "dev": ["poonai"] 
        }
         
```
```
> true
```
<br>

```
package test.basic

test_is_admin_allowed {
  allowed with input as {
    "user": {
      "role" : "ADMIN"
    },
    "api": {
      "url" : "/users/{user_id}/profile",
      "method" : "GET"
    }
  }
}


```









