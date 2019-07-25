# Useful vzorečky pro OpenRefine

## Průměr

| Hledanost|
|---------|
| 100, 50 |
| 10, 25 |
| 32, 34 |

```GREL
forEach(value.split(','),v,v.toNumber()).sum() / length(forEach(value.split(','),v,v.toNumber()))
```
| Hledanost|
|---------|
| 75 |
| 17,5 |
| 33 |

## Sečtení

| Hledanost|
|---------|
| 100, 50 |
| 10, 25 |
| 32, 34 |

```GREL
forEach(value.split(','),v,v.toNumber()).sum()
```

| Hledanost|
|---------|
| 150 |
| 35 |
| 66 |
