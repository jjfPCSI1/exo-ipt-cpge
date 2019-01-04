# Calcul de somme

Calculer la complexité du calcul de somme suivant

```Python
def somme1(n):
    s = 0
    for i in range(5):
        for k in range(n):
            s = s + i*k
    return s

```
