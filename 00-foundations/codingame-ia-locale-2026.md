# CodinGame Fall 2026 — IA locale et développement assisté

**Mise à jour : 3 novembre 2026**  
**Statut : projet en cours, résultats non audités dans ce dépôt**

## Situation et objectif

Participation au challenge CodinGame Fall 2026 avec un projet local `CODINGAME-FALL-2026` ouvert dans Visual Studio Code sous Windows 11. Objectif : reprendre le développement et les tests d'un bot Python après la limite d'utilisation des assistants cloud, sans perdre les versions précédentes.

**Important : les fichiers locaux des bots et les résultats de tests ne sont pas présents dans ce dépôt GitHub.** Cette page est un journal de progression, pas une archive du code du challenge.

## Réalisations constatées lors de la séance

- Utilisation du terminal PowerShell intégré à VS Code dans le dossier local du projet.
- Vérification de l'installation d'Ollama : `ollama list` montre `qwen3:4b` et `ecom-qwen3:4b-16k`, chacun d'environ 2,5 Go.
- Diagnostic d'un refus de connexion à l'API locale d'Ollama, puis vérification que le service répond.
- Lancement du modèle local `qwen3:4b` via `ollama run qwen3:4b` : invite interactive observée.
- Démarrage d'OpenCode depuis le terminal. Après sélection, l'interface affiche `qwen3:4b Ollama`.
- Première tentative de bilan du projet en mode Plan. L'agent a demandé de préciser la tâche au lieu de produire une analyse des fichiers : **l'accès effectif au code et sa compréhension ne sont pas encore vérifiés**.

## État du bot rapporté lors des échanges

- Plusieurs versions du bot Python existent ou sont évoquées, notamment V1 et V3.
- Selon un compte-rendu antérieur, V3 aurait gagné **8 parties sur 8** contre le boss, contre **6 sur 8** pour V1. **Ces chiffres sont rapportés, pas reproduits ni validés depuis ce dépôt.**
- Un audit de V3 a signalé un risque stratégique : des commandes `SPAWN` successives peuvent neutraliser plusieurs triangles possédés, réduisant le revenu de score. Correction et tests encore à réaliser ou à vérifier.
- Les fichiers originaux, règles et résultats doivent être inspectés avant de modifier quoi que ce soit.

## Compétences pratiquées

- Lancer des commandes dans PowerShell et lire des messages d'erreur.
- Distinguer une IA locale Ollama d'un modèle distant proposé par OpenCode.
- Diagnostiquer une connexion locale et vérifier le modèle actif.
- Rédiger une consigne de travail en lecture seule et demander des preuves avant modification.

**Niveau déclaré : pratique guidée.** Cette activité ne prouve pas à elle seule une maîtrise autonome du développement Python ou des agents IA.

## Prochaine étape unique

Faire lire le dossier `CODINGAME-FALL-2026` par un agent configuré en lecture seule, vérifier qu'il cite des fichiers réellement présents, puis récupérer les tests du bot V3. Ne modifier ou publier aucun bot tant que cet état n'est pas confirmé.


## Vérification de la sauvegarde GitHub — 5 novembre 2026

- Contrôle du compte GitHub connecté : aucun dépôt séparé nommé `CODINGAME-FALL-2026` n'apparaît parmi les dépôts accessibles.
- Ce dépôt `enterprise-it-lab` contient **le journal de progression**, mais **pas le code des bots, ni l'intégralité des règles, ni les tests locaux**. Ne pas confondre journal et sauvegarde du projet.
- Projet original déclaré sur l'ancien PC : `C:\Users\yanis\OneDrive\Bureau\CODINGAME-FALL-2026`. La présence effective du dossier dans le cloud OneDrive n'est pas encore vérifiée.
- Fichiers à rechercher dans la copie originale : `docs/REGLES.md`, `docs/RESSOURCES.md`, `docs/REFERENCES.md`, `docs/ETAT_PROJET.md`, `AGENTS.md`, `CLAUDE.md`, `bots/bot_v1.py`, `bots/bot_v2.py`, `bots/bot_v3.py` (ce dernier est signalé dans les échanges, pas vérifié dans GitHub).
- Bilan des essais **rapportés, pas reproduits** : V1 = 6/8 contre boss Bronze ; V2 = 5/8 ; V3 = 8/8. Point critique V3 : `SPAWN` successifs peuvent faire perdre la propriété/production des triangles.
- Sur le nouveau PC prêté au laboratoire : retrouver d'abord le **dossier original synchronisé** via OneDrive ou une copie depuis l'ancien PC. Ne pas créer un nouveau bot à partir de zéro tant que cette récupération n'a pas été essayée.
- Après récupération : ouvrir le dossier dans VS Code, demander à Claude Code et à Codex un **audit en lecture seule** (inventaire fichiers, provenance des règles, vérification tests et compatibilité Gold), avant tout changement.
- **Attention** : `enterprise-it-lab` est public. Ne pas publier ici le code de compétition en cours ; prévoir un dépôt **privé** séparé pour la sauvegarde complète du projet.
