
---
Title: "Negation"
type: docs
weight: 5
---

# OPA By Example: Negation

{{< columns >}}

- ```not``` turns ```undefined``` into ```true```.
- ```not``` turns ```false``` into ```true```.
- ```not``` turns everything else into ```undefined```.

Consider a rego object ```obj``` (-->).


### Check path existence by writing the path.
- check if path exists <br>
```obj.spec.speed```

- check if path does not exist <br>
```not obj.spec.speed```



<--->
<br><br><br>

```js
obj := {car":"Tata", 
"color": ["black", “white”], 
"spec": {"speed": 227}}
```

```js
> not obj.x	// true, there exist no ‘x’
> not false	// true
> not 22	// undefined
> not true  // undefined
```


{{< /columns >}}