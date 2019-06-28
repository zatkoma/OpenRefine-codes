## Poslední část URL bez prvního slova


```GREL
value.split("/")[-1].split("?")[0].split(".html")[0].split("-").join(" ").split(/^(.*?) /)[-1]
```
