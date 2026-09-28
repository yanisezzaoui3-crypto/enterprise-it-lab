# 01 — IT Lab

Cette section documente la construction progressive d'un laboratoire informatique destiné à apprendre par la pratique.

Le but n'est pas de reproduire immédiatement une infrastructure complexe, mais de construire un environnement réaliste étape par étape et de comprendre chaque composant avant de passer au suivant.

## Navigation

- [Architecture cible du laboratoire](architecture.md)
- [Virtualisation : notions et préparation](virtualization.md)

## Objectifs du laboratoire

Le laboratoire servira à pratiquer :

- la virtualisation ;
- Windows et Linux ;
- les bases réseau ;
- l'administration système ;
- les services d'infrastructure ;
- PowerShell et Python ;
- le diagnostic ;
- la journalisation et la supervision ;
- la cybersécurité défensive.

## Architecture cible progressive

L'environnement évoluera progressivement vers une petite infrastructure d'entreprise virtuelle.

```text
PC hôte
│
└── Hyperviseur
    │
    ├── Windows Server
    │   ├── Active Directory
    │   ├── DNS
    │   └── DHCP
    │
    ├── Windows Client
    │
    └── Linux Server
        └── services et administration
```

Cette architecture est une cible d'apprentissage. Les machines et services seront ajoutés seulement lorsqu'ils seront compris et utiles à l'étape en cours.

## Progression prévue

### Phase 1 — Préparer l'environnement

- [ ] vérifier les ressources disponibles sur le PC ;
- [ ] choisir l'outil de virtualisation ;
- [ ] comprendre ce qu'est une machine virtuelle ;
- [ ] comprendre NAT, réseau interne et bridge ;
- [ ] créer une première machine virtuelle.

### Phase 2 — Systèmes

- [ ] installer une machine Linux ;
- [ ] installer une machine Windows ;
- [ ] apprendre utilisateurs, groupes, fichiers et permissions ;
- [ ] pratiquer les commandes système de base ;
- [ ] documenter les erreurs rencontrées.

### Phase 3 — Réseau

- [ ] configurer des adresses IP ;
- [ ] comprendre masque, passerelle et DNS ;
- [ ] tester la communication entre machines ;
- [ ] utiliser `ping`, `ipconfig` / `ip`, `nslookup` et `tracert` / `traceroute` ;
- [ ] diagnostiquer volontairement des pannes simples.

### Phase 4 — Services d'entreprise

- [ ] installer Windows Server ;
- [ ] découvrir Active Directory ;
- [ ] créer un domaine de laboratoire ;
- [ ] intégrer un poste client au domaine ;
- [ ] pratiquer DNS et DHCP ;
- [ ] gérer utilisateurs et groupes.

### Phase 5 — Administration et automatisation

- [ ] administrer avec PowerShell ;
- [ ] automatiser des tâches simples ;
- [ ] utiliser Python lorsque cela apporte un gain réel ;
- [ ] documenter les scripts et leur fonctionnement.

### Phase 6 — Cybersécurité défensive

- [ ] comprendre les journaux système ;
- [ ] centraliser ou analyser des logs ;
- [ ] pratiquer le durcissement de base ;
- [ ] créer des scénarios de diagnostic ;
- [ ] observer et expliquer des événements suspects dans un environnement contrôlé.

## Méthode de documentation

Chaque exercice du laboratoire doit idéalement contenir :

1. **Situation** — ce que je cherche à faire.
2. **Concept** — la notion informatique travaillée.
3. **Manipulation** — commandes, configuration ou outils utilisés.
4. **Résultat** — ce qui s'est produit.
5. **Erreur / diagnostic** — problème rencontré et méthode utilisée.
6. **Ce que j'ai compris** — explication avec mes propres mots.
7. **Preuve** — capture, commande, configuration ou fichier lorsque c'est pertinent.

## Principe

Ce laboratoire est un environnement d'apprentissage.

Une case cochée signifie qu'une manipulation a réellement été effectuée et documentée. Une technologie listée mais non cochée représente uniquement une étape prévue.
