---
attachments: [floyd_warshall_pseudocode.png, floyd_warshall.png]
tags: [Cours, ESGI]
title: Intelligence Artificielle
created: '2021-12-31T02:00:54.949Z'
modified: '2022-01-04T18:27:30.540Z'
---

# Intelligence Artificielle 

## 08/09/202 
Cours sur les graphs orientés 

## 09/09/2021 

### Algorithme de Floyd-Warshall 

![floyd_warshall](../.././attachments//floyd_warshall.png)

Appliquer l'algorithme de Floyd-Warshall sur le graph ( à copier ) 

|   | 1 | 2  | 3  | 4  | 5  |
|---|---|----|----|----|----|
| 1 | 6 | 3  | 1  | 7  | 10 |
| 2 | 3 | 6  | -2 | 4  | 7  |
| 3 | 5 | 8  | 6  | 12 | 15 |
| 4 | ∞ | ∞  | ∞  | ∞  | -3 |
| 5 | 7 | 10 | 2  | 10 | 3  |


![floyd_warshall_pseudocode](../.././attachments/floyd_warshall_pseudocode.png)

### Algorithme de Dijkstra
