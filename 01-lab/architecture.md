# Architecture cible du laboratoire

Cette page décrit l'architecture **prévue** du laboratoire. Elle sert de référence avant les installations et sera mise à jour au fur et à mesure des manipulations réellement effectuées.

## Vue d'ensemble

```text
                         ┌──────────────────────┐
                         │       PC hôte        │
                         │ Windows + hyperviseur│
                         └──────────┬───────────┘
                                    │
                         Réseau virtuel du lab
                                    │
          ┌─────────────────────────┼─────────────────────────┐
          │                         │                         │
┌─────────▼─────────┐     ┌─────────▼─────────┐     ┌─────────▼─────────┐
│  Windows Server   │     │  Windows Client   │     │   Linux Server    │
│                   │     │                   │     │                   │
│ - Active Directory│     │ - poste utilisateur│    │ - administration  │
│ - DNS             │     │ - joint au domaine│     │ - services Linux │
│ - DHCP            │     │ - tests réseau    │     │ - logs / scripts │
└───────────────────┘     └───────────────────┘     └───────────────────┘
```

> Cette architecture représente une cible d'apprentissage. Les services ne sont pas considérés comme installés tant qu'ils n'ont pas été réellement configurés et documentés.

## Rôle des composants

### PC hôte

Le PC physique fournit les ressources du laboratoire :

- processeur ;
- mémoire vive ;
- stockage ;
- accès réseau ;
- logiciel de virtualisation.

Il hébergera les machines virtuelles.

### Hyperviseur

L'hyperviseur permettra de créer et exécuter plusieurs machines virtuelles sur le même ordinateur.

Notions à comprendre :

- machine virtuelle ;
- CPU virtuel ;
- RAM virtuelle ;
- disque virtuel ;
- carte réseau virtuelle ;
- snapshot ;
- réseau NAT ;
- réseau interne ;
- bridge.

### Windows Server

Cette machine sera utilisée pour découvrir des services courants d'une infrastructure Microsoft.

Services prévus :

- **Active Directory Domain Services** pour gérer identités, ordinateurs et domaine ;
- **DNS** pour la résolution de noms ;
- **DHCP** pour l'attribution automatique de paramètres réseau.

### Windows Client

Cette machine simulera le poste d'un utilisateur dans l'entreprise.

Elle servira notamment à :

- tester la connectivité ;
- rejoindre le domaine ;
- ouvrir une session avec différents comptes ;
- tester les droits et politiques ;
- pratiquer le diagnostic côté utilisateur.

### Linux Server

Cette machine permettra d'apprendre l'administration Linux et d'ajouter progressivement des services.

Elle servira notamment à :

- pratiquer le terminal ;
- gérer utilisateurs, groupes et permissions ;
- comprendre les services et processus ;
- analyser des logs ;
- tester des scripts et outils d'administration.

## Réseau du laboratoire

Le réseau sera construit progressivement.

Avant de fixer des adresses IP définitives, les notions suivantes devront être comprises et testées :

- adresse IP ;
- masque de sous-réseau ;
- passerelle ;
- DNS ;
- DHCP ;
- NAT ;
- communication entre machines virtuelles.

Un plan d'adressage sera ajouté lorsqu'il sera réellement utilisé.

## Logique d'apprentissage

Le laboratoire suivra cette logique :

```text
comprendre le composant
        ↓
l'installer ou le configurer
        ↓
tester son fonctionnement
        ↓
provoquer ou rencontrer une erreur
        ↓
diagnostiquer
        ↓
documenter la preuve et ce qui a été compris
```

## État

- [x] architecture cible définie ;
- [ ] hyperviseur choisi ;
- [ ] première machine virtuelle créée ;
- [ ] réseau virtuel configuré ;
- [ ] Windows Server installé ;
- [ ] Windows Client installé ;
- [ ] Linux Server installé ;
- [ ] services d'infrastructure configurés.
