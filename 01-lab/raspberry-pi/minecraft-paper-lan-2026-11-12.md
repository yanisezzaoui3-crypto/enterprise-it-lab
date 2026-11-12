# Raspberry Pi 5 — serveur Minecraft Paper et tests LAN (12 novembre 2026)

## Objectif
Héberger un serveur Minecraft Java Edition sur un Raspberry Pi 5 sous Linux, puis permettre à des PC Windows du réseau local de s'y connecter.

## Preuves observées
- Console Paper : démarrage terminé avec `Done (16.823s)! For help, type "help"`. Les mondes overworld, nether et end ont été préparés. Avertissement de version Paper ancienne.
- `ip addr` sur le Raspberry : interface `eth0` active (`UP`), IPv4 `10.195.82.132/22`. `wlan0` affichée DOWN.
- PowerShell Windows : `ping 10.195.82.132` = 4 réponses / 4 envoyées, 0 % de perte, latence moyenne 4 ms.
- Capture d'écran : Minecraft lancé sur le PC Windows, avec un monde affiché.

## Ce qui est validé
- Démarrage du serveur Paper sous Linux ARM64.
- Identification de l'adresse IP du serveur.
- Connectivité IP Windows → Raspberry Pi sur le réseau local.
- Lancement du client Minecraft sur Windows.

## À confirmer
- Résultat de `Test-NetConnection 10.195.82.132 -Port 25565`.
- Connexion effective du client Minecraft au serveur Paper hébergé sur le Raspberry Pi.
- Connexion simultanée de deux clients, stabilité et performances.
- Mise à jour de Paper, sauvegardes, configuration et durcissement du serveur.

## Captures fournies dans la conversation
1. Photo du Raspberry Pi 5 câblé.
2. Photo du terminal `ip addr` avec `eth0` et son adresse IP.
3. Photo du client Minecraft en cours d'exécution.

Les trois images sont disponibles dans la conversation d'origine mais **ne sont pas encore téléversées dans le dépôt GitHub**. Ne pas présenter la capture du jeu comme une preuve de connexion au serveur tant que l'adresse du serveur et la connexion multijoueur n'ont pas été vérifiées.

## Compétences mises en pratique
Linux, réseau IPv4/CIDR, Ethernet, ICMP/ping, diagnostic réseau Windows PowerShell, déploiement de service Java et documentation technique.
