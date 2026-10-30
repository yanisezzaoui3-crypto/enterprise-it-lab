# Portes logiques binaires — AND, OR, XOR et NOT

**Date :** 30 octobre 2026  
**Statut : MAÎTRISÉ** — quatre portes logiques apprises avec leurs tables de vérité.

## Définition

Une **table de vérité** présente toutes les combinaisons possibles des entrées et la sortie d'une porte logique.

- **A** : première entrée (0 ou 1).
- **B** : deuxième entrée (0 ou 1).
- **S** : sortie obtenue.

Pour NOT, il n'y a qu'une entrée : A.

## 1. AND — ET

La sortie vaut **1 uniquement si A ET B valent 1**.

| A | B | S |
|---|---|---|
| 0 | 0 | 0 |
| 0 | 1 | 0 |
| 1 | 0 | 0 |
| 1 | 1 | 1 |

## 2. OR — OU

La sortie vaut **1 si au moins une entrée vaut 1**.

| A | B | S |
|---|---|---|
| 0 | 0 | 0 |
| 0 | 1 | 1 |
| 1 | 0 | 1 |
| 1 | 1 | 1 |

## 3. XOR — OU exclusif

La sortie vaut **1 si A et B sont différents**.

| A | B | S |
|---|---|---|
| 0 | 0 | 0 |
| 0 | 1 | 1 |
| 1 | 0 | 1 |
| 1 | 1 | 0 |

## 4. NOT — NON

La sortie vaut **l'inverse** de l'entrée A.

| A | S |
|---|---|
| 0 | 1 |
| 1 | 0 |

## Apprentissage et vérification

- J'ai appris les quatre portes **AND, OR, XOR et NOT** avec les tables de vérité **A / B / S**.
- **Je maîtrise cette notion.**
- Exercice effectué : **XOR avec A = 1 et B = 1 : S = 0**, réponse correcte.

## Lien avec mon apprentissage réseau

Les portes logiques constituent une base de l'informatique. **AND** s'applique également bit par bit pour obtenir l'adresse réseau à partir d'une adresse IPv4 et d'un masque. Cette application réseau est une étape distincte de la maîtrise des portes logiques.

## Étape suivante

Appliquer AND à un exercice concret de masque IPv4 dans Cisco Packet Tracer.
