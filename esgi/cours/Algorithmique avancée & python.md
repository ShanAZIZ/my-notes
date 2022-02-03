---
tags: [Cours, ESGI]
title: Algorithmique avancée & python
created: '2021-12-31T02:14:52.663Z'
modified: '2022-01-04T18:27:03.447Z'
---

# Algorithmique avancée & python

## TRI PAR INSERTION

DAT -> Données à trier  
DDT -> Données déjà triés  
N -> nb de données 

```
N * ( 
  Pour chaque d dans DAT :
    Trouver la position de d dans DDT
    Insérer p à la position p dans DDT
)

N * ( O(log(N) * O(N)) 

N * O(n) -> O(N2) 
```


## TRI PAR SELECTION  

DAT -> Données à trier  
DDT -> Données déjà triés 
N -> nb de données 

```
N * ( 
  Tant que DAT non vide :  
    Trouver le minimum d de DAT O(n) 
      Retirer d de DAT O(n)
      O(1) ajouter d à la fin des DDT 
) 

N * ( O(N) + O(N) + O(I)) 
N * O(N) -> O(N2)  
```

## TRI A BULLES 

```
N *Jusqu'à stabilité :  
  N *Pour  i allant de 0 à N-1 : 
    O(I)Si data [i] > data [i+1] :  
      O(I)Echange(data[i], data [i+1] 

N* N*(O(I) + O(I))
N2 * O(I) 
O(N2) 
```

__Problèmes du tri à bulles :__ 

- Les petites valeurs descendent lentement 

  - Solution : tri cocktail -> passe dans un sens puis dans l'autre 

- À chaque étape on ne bouge que d'une case  

  - Solution : tri pair - impair ->  une passe sur les couples qui commencent par un indice pair puis impair  

- Chaque étape dépend de la précédente  

  - Solution : tri peigne -> faire varier l'intervalle des couples et le faire diminuer à chaque fois 

 
