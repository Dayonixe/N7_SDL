# Practical Work - Specification and Description Language

<a href="https://www.pragmadev.com/">
  <img src="https://img.shields.io/badge/language-SDL-3dc1c6?style=flat-square" alt="laguage-SDL" />
</a>

---

Pour ce TP, nous avons utilisé <a href="https://www.pragmadev.com/">PragmaStudio</a> pour l'utilisation du langage.

Pour compiler le projet, dans l'arborescence, faire clic-droit sur le système et *Build*.

Pour lancer une simulation, dans l'arborescence, faire clic-droit sur le système et *Debug*.

---

Dans un premier temps notre objectif était simplement de gérer un protocole qui reçoit des données (ici une chaîne de caractères) de l’utilisateur, les insères dans les messages de donnée (ici une chaîne de caractères avec des données précédentes) et les délivres à l’arrivée.

<img src=/Documents/partie1.png alt="Partie 1" />
Transmission de paquet


Dans la seconde partie nous devions insérer un élément perturbateur. Entre le protocole et l'utilisateur, on ajoute une couche qui peut dédoubler des paquets de manière aléatoire. Elle doit pouvoir dédoubler les messages de données comme les acquittements.

<img src=/Documents/partie2.png alt="Partie 2" />
Duplication de paquet


Par la suite nous complétons l'élément perturbateur qui a maintenant la possibilité de perdre des paquets.

<img src=/Documents/partie3.png alt="Partie 3" />
Perte de paquet


Après avoir ajouter la possibilité d'avoir des paquets dédoublés et d'autres paquets perdus, il faut fiabiliser notre protocole pour traiter ces cas d'erreurs.
Pour cela nous utilisons le principe du *bit alterné*, dit aussi *fenêtre glissante de taille 1*.

<img src=/Documents/partie4-1.png alt="Partie 4-1" />
Principe du bit alterné
<img src=/Documents/partie4-2.png alt="Partie 4-2" />
Gestion des pertes avec le timer
<img src=/Documents/partie4-3.png alt="Partie 4-3" />
Lancement et reset du timer

> **Warning**<br>
> Pour l'utilisation du timer dans la simulation, il faut aller l'activer via le menu *Options → Timer → Real time timers*
