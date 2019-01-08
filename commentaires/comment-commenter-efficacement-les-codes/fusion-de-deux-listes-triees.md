# Fusion de deux listes triées

{% tabs %}
{% tab title="Code brut" %}
```python
def fusion(liste1,liste2):
    """ Procède à la fusion de deux listes supposées triées.
    >>> fusion([1,4,6],[2,3,5])
    [1, 2, 3, 4, 5, 6]
    """ 
    L = []                          #
    i1,i2 = 0,0                     #
    n1,n2 = len(liste1),len(liste2) #
    while i1 < n1 and i2 < n2:      #
        if liste1[i1] < liste2[i2]: #
            L.append(liste1[i1])    #
            i1 = i1 + 1             #
        else:                       #
            L.append(liste2[i2])    #
            i2 = i2 + 1             #
    if i1 == n1:                    #
        L.extend(liste2[i2:])       #
    else:                           #
        L.extend(liste1[i1:])       #
    return L                        #
```
{% endtab %}

{% tab title="Commentaire bas niveau" %}
```python
def fusion(liste1,liste2):
    """ Procède à la fusion de deux listes supposées triées.
    >>> fusion([1,4,6],[2,3,5])
    [1, 2, 3, 4, 5, 6]
    """ 
    L = []                          # Création liste vide
    i1,i2 = 0,0                     # Initialisation des compteurs
    n1,n2 = len(liste1),len(liste2) # Racourcis
    while i1 < n1 and i2 < n2:      # Tant que l'on n'a pas épuisé l'une des listes
        if liste1[i1] < liste2[i2]: # On regarde si l'élément de la liste1 est
            L.append(liste1[i1])    # plus petit que celui de la liste2, on le rajoute
            i1 = i1 + 1             # à L et on passe au suivant
        else:                       # Sinon, on fait le contraire en rajoutant
            L.append(liste2[i2])    # l'élément de la liste2
            i2 = i2 + 1             # et en passant au suivant.
    if i1 == n1:                    # Si la liste1 est finie,
        L.extend(liste2[i2:])       # on rajoute les éléments restant de liste2
    else:                           # et si c'est le contraire,
        L.extend(liste1[i1:])       # on rajoute les éléments restant de liste1 
    return L                        # Renvoi de la liste L
```
{% endtab %}

{% tab title="Commentaire avec du recul" %}
```python
def fusion(liste1,liste2):
    """ Procède à la fusion de deux listes supposées triées.
    >>> fusion([1,4,6],[2,3,5])
    [1, 2, 3, 4, 5, 6]
    """ 
    L = []                          # Futur récipiendaire de la liste triée
    i1,i2 = 0,0                     # Points de départ
    n1,n2 = len(liste1),len(liste2) #
    while i1 < n1 and i2 < n2:      # On prend l'élément le plus petit entre
        if liste1[i1] < liste2[i2]: # les deux listes à l'emplacement courant
            L.append(liste1[i1])    # dans chaque liste. On le rajoute dans L
            i1 = i1 + 1             # (qui est donc correctement ordonnée)
        else:                       # et on déplace le curseur d'un cran dans 
            L.append(liste2[i2])    # la liste où il a "disparu"
            i2 = i2 + 1             # 
    if i1 == n1:                    # Si une des listes est épuisée, on rajoute
        L.extend(liste2[i2:])       # les éléments de l'autre (forcément plus
    else:                           # grands) à la liste L
        L.extend(liste1[i1:])       # 
    return L                        # Renvoi de L (forcément triée)
```
{% endtab %}
{% endtabs %}

