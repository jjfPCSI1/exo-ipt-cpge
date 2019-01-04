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
On fait une assignation après lecture d'un élément dans une liste (2 op.).
Puis $n$ fois un test (1 op.) avec, parfois, une assignation (1 op.), soit $n$ à $2n$ opérations dans la boucle. Au total
$$
n + 2 <= C(n) \leq  2n + 2 = O(n)
$$
{% endhint %}

{% endtab %}

{% tabs %}
{% tab title="First Tab" %}
Voyons voir
{% endtab %}

{% tab title="Caché dans un onglet" %}
Une manière de mettre la solution ?
{% endtab %}

{% tab title="Second Tab" %}

{% endtab %}
{% endtabs %}


