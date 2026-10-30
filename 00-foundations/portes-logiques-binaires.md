# Portes logiques et binaire — AND, OR, XOR, NOT

**Date d'apprentissage :** 30 octobre 2026  
**Statut :** notion étudiée ; premiers exercices de compréhension réussis. Maîtrise complète à consolider.

## Situation

Après avoir découvert les bits (0 et 1) et les valeurs binaires, j'ai appris le rôle de quatre portes logiques.

## Ce que j'ai compris

- **AND (ET)** : la sortie vaut 1 seulement si les deux entrées valent 1.
- **OR (OU)** : la sortie vaut 1 si au moins une entrée vaut 1.
- **XOR (OU exclusif)** : la sortie vaut 1 si les deux entrées sont différentes.
- **NOT (NON)** : inverse une seule entrée (0 devient 1 ; 1 devient 0).

### Table de vérité (deux entrées)

| A | B | AND | OR | XOR |
|---|---|---|---|---|
| 0 | 0 | 0 | 0 | 0 |
| 0 | 1 | 0 | 1 | 1 |
| 1 | 0 | 0 | 1 | 1 |
| 1 | 1 | 1 | 1 | 0 |

### Table de vérité (NOT)

| A | NOT A |
|---|---|
| 0 | 1 |
| 1 | 0 |

## Test réalisé

**Question :** quelle est la sortie de XOR si A = 1 et B = 1 ?  
**Ma réponse :** 0.  
**Résultat :** correct, puisque XOR exige des entrées différentes pour donner 1.

## Utilité dans mon parcours IT

Ces opérations sont à la base des circuits logiques. En réseau, l'opération **AND** bit à bit permet également de calculer une adresse réseau à partir d'une adresse IPv4 et de son masque. Ce lien avec les masques reste à pratiquer dans le labo Packet Tracer.

## Prochaine consolidation

Reproduire les résultats de AND, OR, XOR et NOT sans aide, puis relier AND à un exemple d'adresse IPv4 et de masque.
