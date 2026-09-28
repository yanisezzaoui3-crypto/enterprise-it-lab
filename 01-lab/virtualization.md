# Virtualisation

Cette page prépare la première étape pratique du laboratoire : comprendre la virtualisation avant de créer une machine virtuelle.

## Situation réelle

Je veux apprendre Windows Server, Linux, le réseau et la cybersécurité sans acheter plusieurs ordinateurs physiques.

La solution consiste à utiliser mon PC comme machine principale et à créer plusieurs ordinateurs virtuels à l'intérieur.

## Termes à connaître

### Hyperviseur

Un **hyperviseur** est un logiciel qui permet de créer et faire fonctionner des machines virtuelles.

Exemples connus :

- Hyper-V ;
- VirtualBox ;
- VMware Workstation.

> Phrase à retenir : **un hyperviseur fait tourner plusieurs ordinateurs virtuels sur un seul ordinateur physique.**

### Machine virtuelle — VM

**VM** signifie *Virtual Machine*, ou **machine virtuelle**.

Une VM se comporte comme un ordinateur séparé.

Elle peut avoir :

- son propre système d'exploitation ;
- sa propre mémoire vive ;
- son propre disque virtuel ;
- sa propre carte réseau virtuelle ;
- sa propre adresse IP.

> Phrase à retenir : **une VM est un ordinateur logiciel qui fonctionne à l'intérieur d'un ordinateur physique.**

### CPU virtuel — vCPU

Le **CPU** est le processeur de l'ordinateur.

Une **vCPU** est une partie de la puissance du processeur physique donnée à une machine virtuelle.

Exemple :

```text
PC physique : 8 cœurs
VM Linux : 2 vCPU
VM Windows : 2 vCPU
```

> Phrase à retenir : **la vCPU représente la puissance processeur attribuée à une VM.**

### RAM virtuelle

La **RAM** est la mémoire de travail utilisée par les programmes pendant qu'ils fonctionnent.

Une VM reçoit une partie de la RAM du PC physique.

Exemple :

```text
PC : 16 Go de RAM
VM Windows : 4 Go
VM Linux : 2 Go
```

> Phrase à retenir : **la RAM d'une VM vient de la RAM du PC physique.**

### Disque virtuel

Une VM utilise un fichier qui se comporte comme un disque dur.

Ce fichier contient notamment :

- le système d'exploitation ;
- les programmes ;
- les fichiers de la VM.

> Phrase à retenir : **le disque virtuel est le stockage de la machine virtuelle.**

### Carte réseau virtuelle

Une VM peut avoir une carte réseau virtuelle.

Elle permet à la VM de communiquer :

- avec le PC hôte ;
- avec les autres VM ;
- avec Internet, selon la configuration.

> Phrase à retenir : **la carte réseau virtuelle permet à la VM de communiquer sur un réseau.**

## Modes réseau à comprendre

### NAT

**NAT** signifie *Network Address Translation*.

Dans un lab, le NAT permet généralement à une VM d'accéder à Internet en passant par la connexion du PC hôte.

```text
VM
↓
PC hôte
↓
Internet
```

> Phrase à retenir : **NAT permet à une VM de sortir vers Internet en utilisant la connexion du PC hôte.**

### Réseau interne

Un réseau interne permet aux VM de communiquer entre elles sans forcément être directement accessibles depuis le réseau extérieur.

Exemple :

```text
Windows Server ↔ Windows Client ↔ Linux Server
```

> Phrase à retenir : **un réseau interne sert à faire communiquer les machines du laboratoire entre elles.**

### Bridge

Le mode **bridge** place la VM sur le même réseau que le PC physique.

La VM peut alors apparaître comme une machine séparée sur le réseau local.

> Phrase à retenir : **bridge connecte la VM directement au même réseau local que le PC physique.**

## Avant de créer la première VM

Nous devons vérifier :

- [ ] la quantité de RAM disponible ;
- [ ] le processeur ;
- [ ] l'espace disque libre ;
- [ ] si la virtualisation matérielle est activée ;
- [ ] quel hyperviseur utiliser.

## Choix de l'hyperviseur

Le choix sera fait après vérification du PC.

Le but n'est pas d'installer plusieurs outils inutilement, mais de choisir celui qui convient au matériel et au laboratoire prévu.

## Première manipulation prévue

Lorsque le PC sera disponible :

1. vérifier les caractéristiques du PC ;
2. vérifier que la virtualisation est disponible ;
3. choisir l'hyperviseur ;
4. l'installer ;
5. créer une première VM simple ;
6. documenter les commandes, captures et problèmes rencontrés.

## État

- [x] notions principales de virtualisation documentées ;
- [ ] caractéristiques du PC vérifiées ;
- [ ] hyperviseur choisi ;
- [ ] hyperviseur installé ;
- [ ] première VM créée ;
- [ ] premier test réseau effectué.
