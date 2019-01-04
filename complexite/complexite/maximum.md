# Maximum

## Recherche d'un maximum dans une liste

{% tabs %}
{% tab title="Énoncé" %}
Déterminer la complexité de la fonction suivante

```python
def maximum(liste):
    M = liste[0]
    for element in liste:
        if element > M:
            M = element
    return element
```
{% endtab %}

{% tab title="Indication" %}
{% hint style="info" %}
Pensez voir à ce qu'il en coûte de regarder les éléments.
{% endhint %}
{% endtab %}

{% tab title="Corrigé" %}
{% hint style="success" %}

On fait une assignation après lecture d'un élément dans une liste \(2 op.\). 
Puis $$n$$ fois un test \(1 op.\) avec, parfois, une assignation \(1 op.\), soit 
$$n$$ à $$2n$$ opérations dans la boucle. Au total 

$$
n + 2 \leq C(n) \leq  2n + 2 
$$

Le coût est encadré par deux fonction qui sont en $$O(n)$$, c'est donc 
lui-même un $$O(n)$$, soit une complexité linéaire en temps.

{% endhint %}
{% endtab %}
{% endtabs %}

