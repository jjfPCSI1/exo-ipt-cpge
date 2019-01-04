# Maximum

## Recherche d'un maximum dans une liste

Déterminer la complexité de la fonction suivante

```python
def maximum(liste):
    M = liste[0]
    for element in liste:
        if element > M:
            M = element
    return element
```



