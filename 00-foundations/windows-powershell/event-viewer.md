# Observateur d'événements Windows

## Situation pratiquée

J'ai utilisé l'Observateur d'événements Windows pour rechercher des informations après un comportement système inhabituel.

## Ce que j'ai observé

J'ai notamment rencontré un événement **Kernel-Power**.

## Ce que j'ai appris

Un événement Kernel-Power peut signaler que Windows a redémarré ou s'est arrêté sans procédure normale.

Il ne permet pas, à lui seul, d'identifier la cause exacte.

Il faut donc le replacer dans le contexte avec :

- l'heure de l'événement ;
- les événements précédents ;
- les processus actifs ;
- les erreurs applicatives ou système ;
- les actions effectuées sur le PC.

## Compétence travaillée

Lire un journal système sans transformer immédiatement un événement en conclusion.
