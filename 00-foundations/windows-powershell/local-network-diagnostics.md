# Diagnostic réseau local sous Windows

## Manipulations déjà pratiquées

Dans différents dépannages, j'ai déjà travaillé avec :

- adresses IP locales ;
- ports ;
- services locaux ;
- connexions entre un programme et `127.0.0.1` ;
- vérification qu'un service écoute correctement sur le PC.

## Exemple

Un service local peut écouter sur une adresse comme :

```text
127.0.0.1:PORT
```

`127.0.0.1` représente la machine locale.

## Ce que j'ai appris

Il faut distinguer :

- une connexion locale ;
- une connexion vers le réseau local ;
- une connexion vers Internet ;
- un service qui écoute sur un port.

Voir un port ouvert ne signifie pas automatiquement qu'un programme est accessible depuis Internet.

## Objectif suivant

Approfondir avec :

- `ipconfig` ;
- `ping` ;
- `tracert` ;
- `nslookup` ;
- `netstat` ;
- DNS ;
- DHCP ;
- TCP/UDP.
