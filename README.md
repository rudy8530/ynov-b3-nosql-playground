# Ludi Project
<p>Ludi project est un projet qui est né avec 2 de mes amis. Il s'agit de créer une application à destination des sportifs uniquement sur Android. </br> 
Vous trouverez dans ce dépôt git différents fichiers: 
    - Ludi_UML, il s'agit d'un fichier présentant une première version de la structure relationnelle en UML
    - MCD App, il s'agit du modèle MCD généré avec le logiciel WorkBench
</p>
<p>Cette application est pour le territoire français</p>

<h2>Spécifications et exigences</h2>
Vous pourrez retrouver toutes les spécifications et les exigences du projet dans le document intitulé "2018 04 17 - Description projet".

<h2>Choix des technologies</h2>
<p>La table User est qui se démarque de toutes les autres. En effet, l'application permettra aux utilisateurs d'ajouter une photo de profil, cette dernière devra donc être stocker dans une base de données.</br>
Pour ce faire, nous avons choisi la solution MongoDB car ce système de gestion de base de données est orienté documents et il est répartissable sur un nombre quelconque d'ordinateurs et il ne nécessite pas de schéma prédéfini des données.</p>

Pour les tables suivantes, les données seront uniquement consulter, il n'y aura aucune écriture dans la base de données par les utilisateurs:
  - activity
  - specificity
  - town
  - gender
  - authtoken

<p>La solution retenue pour toutes ces tables est MySQL, en effet c'est une solution rapide, facile à utiliser, sécurisé, ouvertes et elle est portatible (Linux, Windows etc...).</p>

En revanche pour les tables ci-dessous, nous allons utiliser la solution Cassandra. En effet, l'application va écrire beaucoup d'informations dans ces différentes tables et Cassandra est très utile lorsque l'on écrit beaucoup dans les tables (plus que si on consultait).
Le langage utilisé pour Cassandra est le Java.
Tables concernées:
- Session
- Participant
- Notification
- Messaging
- Friend
