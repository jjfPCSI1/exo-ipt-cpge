# Factorielle

## Calcul d'une factorielle

Déterminer la complexité de la fonction suivante

```python
def factorielle(n):
    p = 1
    for i in range(1,n+1):
        p = p*i
    return p
```
