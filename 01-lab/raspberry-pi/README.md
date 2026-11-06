# Raspberry Pi — installation Linux sur carte microSD (Fatlab)

**Date :** 6 novembre 2026  
**Statut :** préparation en cours ; écriture et démarrage non encore confirmés.  
**Contexte :** atelier Fatlab, installation de Linux sur Raspberry Pi avec lecteur de carte SD USB, après une première tentative avec une clé USB.

## Matériel et outil observés
- Raspberry Pi (modèle exact non encore identifié).
- Carte microSD dans un lecteur USB reconnu sous Windows comme `Generic- USB3.0 CRW -SD USB Device`, capacité affichée **37,3 Go**, lecteur **E:\\**.
- **Raspberry Pi Imager v2.0.12** sous Windows.

> Attention : l'écriture d'une image OS efface le contenu du support sélectionné. Vérifier que E: est bien la carte microSD avant de lancer l'écriture.

## Étapes constatées (captures du 6 novembre)
1. Ouverture de Raspberry Pi Imager.
2. Sélection de **Raspberry Pi OS (64-bit)**, version basée sur **Debian Trixie** avec bureau Raspberry Pi, affichée comme « recommandée » par Imager. Le téléchargement annoncé est d'environ 1,4 Go. **Choix constaté**, mais la compatibilité dépend du modèle de Raspberry Pi.
3. Dans « Stockage », sélection du lecteur de carte SD USB `Generic- USB3.0 CRW -SD USB Device` (37,3 Go, E:).
4. Dans « Personnalisation > Nom d'hôte », saisie de **WADA3A** (à confirmer si Imager accepte les majuscules ou normalise le nom).
5. Dans « Localisation », premier essai affichant **Zagreb (Croatia)**, fuseau **Europe/Zurich** et clavier `hr` : combinaison incohérente pour un clavier suisse ; **ne pas conserver `hr`**.
6. Capture suivante : paramètres de localisation encore vides.
7. **Capture de localisation :** **Bern (Switzerland)**, fuseau **Europe/Zurich**, disposition clavier **ch**. C'est le bon choix de pays et de disposition pour un clavier suisse ; la variante exacte (suisse français ou suisse allemand) reste à vérifier sur le clavier physique.
8. **Capture — personnalisation Wi-Fi :** mode **RÉSEAU SÉCURISÉ**, nom de réseau (SSID) **`WADA3A BINKS`**. Champs mot de passe et confirmation remplis à l'écran (masqués). **Aucun mot de passe n'est enregistré dans le dépôt**. Connexion effective du Raspberry Pi à ce Wi-Fi pas encore vérifiée.
9. **Capture — Accès à distance / authentification SSH :** écran « Configurer l'accès SSH » atteint. Interrupteur **Activer SSH désactivé** sur la première capture ; options proposées : mot de passe ou clé publique. Sur la **nouvelle capture**, l'option **« Utiliser un mot de passe pour l'authentification » est sélectionnée** (bouton radio bleu). **L'activation effective de SSH et le fonctionnement d'une connexion restent à vérifier.** Explication apportée : adresse IP = appareil, port = service sur l'appareil, TCP = transport fiable des données, SSH = terminal distant sécurisé. Ces notions sont **en découverte, non évaluées ni maîtrisées**.

## Vérifications encore à faire
- Identifier le modèle précis du Raspberry Pi pour confirmer le choix 64 bits.
- Vérifier les paramètres utilisateur et l'éventuel accès SSH en évitant de publier mots de passe et secrets ; confirmer ultérieurement la connexion effective au Wi-Fi `WADA3A BINKS`.
- Lancer l'écriture sur la microSD, attendre la vérification de l'image par Imager.
- Insérer la microSD dans le Raspberry Pi, brancher l'alimentation et constater le premier démarrage.
- Contrôler Linux et le clavier sur l'appareil, par exemple avec `uname -a`, `cat /etc/os-release` et un test de frappe.
- Ajouter les preuves des étapes réellement réussies, sans déclarer l'installation terminée avant le premier démarrage.

## Compétences travaillées
- Reconnaître OS, support de stockage et architecture 64 bits.
- Préparer un support de démarrage Linux avec Raspberry Pi Imager.
- Configurer localisation, fuseau horaire et clavier.
- Suivre un diagnostic de manière reproductible, avec captures et vérification indépendante.

**Note de suivi :** compléter ce journal au fur et à mesure des nouvelles captures envoyées depuis le Fatlab.

## Mini-quiz réseau et SSH (6 novembre 2026)
- **IP et port** : à la question « que représente 22 dans 192.168.1.20:22 ? », réponse **B (port SSH)** : correcte.
- **TCP** : à la question « que fait TCP lorsque des données se perdent ? », réponse **B (retransmettre les données perdues)** : correcte.
- **Lien IP + port** : à la question « pourquoi faut-il l'adresse IP et le port pour SSH ? », réponse **A (IP = appareil ; port = service)** : correcte. Notion comprise dans ce quiz, à revoir en situation réelle.
- **À consolider** : TCP utilise des accusés de réception et des mécanismes de retransmission ; la notion reste **en apprentissage**, pas encore déclarée maîtrisée.
