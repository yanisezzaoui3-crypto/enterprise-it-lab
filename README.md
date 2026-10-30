# Enterprise IT Lab

Portfolio d'apprentissage orienté **support informatique, systèmes, réseau, automatisation et cybersécurité défensive**.

## Objectif

Construire progressivement des compétences techniques vérifiables et documenter chaque étape sur GitHub.

Le dépôt suit une progression simple :

1. consolider les bases déjà pratiquées ;
2. construire un laboratoire informatique ;
3. apprendre l'administration Windows/Linux et le réseau ;
4. automatiser avec PowerShell et Python ;
5. progresser vers la cybersécurité défensive.

## État actuel

### 00 — Foundations
Consolidation des expériences déjà réalisées avant le démarrage du laboratoire :

- Python débutant ;
- Git et GitHub ;
- Windows et PowerShell ;
- diagnostic système ;
- outils IA utilisés dans un environnement de développement.
- [portes logiques AND, OR, XOR et NOT : MAÎTRISÉ](00-foundations/portes-logiques-binaires.md) — tables de vérité A, B, S apprises le 30 octobre 2026.

### 01 — IT Lab
La construction du laboratoire est maintenant planifiée et documentée :

- [Feuille de route du laboratoire](01-lab/README.md)
- [Architecture cible](01-lab/architecture.md)

### 02 — Réseau

- [Premier réseau Cisco Packet Tracer : deux PC et un switch](02-reseau/01-deux-pc/README.md)
- Test PC0 vers PC1 réussi : 4 réponses sur 4, aucune perte. Configurations et captures documentées.
- [Deuxième réseau : trois PC et un switch](02-reseau/02-trois-pc/README.md) — configurations IPv4 vérifiées et pings de PC2 vers PC0 et PC1 réussis le 27 octobre 2026 (4 réponses sur 4 à chaque test).
- [Troisième réseau : deux sous-réseaux reliés par un routeur](02-reseau/03-routeur-deux-reseaux/README.md) — table de routage interprétée avec accompagnement ; pings PC0↔PC3, PC1→PC3 et PC2→PC3 réussis (4 réponses sur 4), puis trajet PC3→PC1 observé en mode Simulation le 27 octobre 2026.

### Prochaine étape
Réaliser une panne volontaire d'adressage et la corriger. Consolider l'explication du masque et reproduire la configuration avec moins d'aide. Les fichiers `.pkt` restent pour l'instant sur le PC local.

## Principe du dépôt

Chaque sujet doit montrer :

- la situation ou le problème ;
- ce qui a été testé ;
- les commandes ou outils utilisés ;
- le résultat ;
- ce qui a été compris ;
- les erreurs rencontrées et leur correction.

> Ce dépôt représente une progression d'apprentissage. Une technologie présente ici n'est pas automatiquement une technologie maîtrisée.
