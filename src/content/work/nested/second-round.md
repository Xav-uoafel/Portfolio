---
title: Second-Round
publishDate: 2024-03-15 00:00:00
img: /assets/2nd.png
img_alt: Interface utilisateur de l'application Second-Round affichant des jeux d'occasion
description: |
  Application facilitant la mise en relation entre professionnels vendeurs de jeux d'occasion et particuliers.
tags:
  - Développement
  - Base de Données
  - API
  - Design
  - IA
---

SecondRound est une mobile web app conçue pour transformer l'expérience d'achat et de vente de jeux vidéo d'occasion. Ce projet est le fruit d'un défi intense de 10 jours réalisé en collaboration avec deux autres développeurs Full Stack. Ensemble, nous avons couvert chaque aspect du développement, de la conception visuelle à la mise en production, avec l'ambition de simplifier et d'enrichir les interactions entre les détenteurs de magasins de jeux vidéo et les joueurs.

**Fonctionnalités pour les Vendeurs**
- **Auto-génération de fiches produits** : Photographiez les jeux et obtenez automatiquement une fiche produit détaillée, prête pour la vente.
- **Gestion des réservations** : Visualisez et acceptez facilement les réservations en cours directement depuis l'accueil.
- **Stock et modifications** : Un espace dédié pour gérer le stock et mettre à jour les fiches de jeux vidéo.

**Fonctionnalités pour les Joueurs**
- **Recherche simplifiée** : Trouvez des jeux vidéo d'occasion près de chez vous grâce à la recherche et à l'auto-localisation.
- **Itinéraire et timer** : Visualisez l'itinéraire pour récupérer votre jeu et suivez le timer de récupération sur la page d'accueil.

**Technologies Utilisées**
- **Ruby on Rails** : Utilisé pour la gestion backend et la logique métier de l'application.
- **JavaScript** : Utilisé pour rendre l'interface utilisateur dynamique et interactive.
- **Bootstrap** : Utilisé pour la mise en page et le style de l'application.
- **PostgreSQL** : Base de données relationnelle utilisée pour stocker les données des articles et des utilisateurs.
- **Redis** : Stocke en cache les informations prises via l'appareil photo de l'utilisateur.
- **API GiantBomb & OpenAI** : Intégrés pour récupérer les jaquettes des jeux vidéo puis envoyer vers ChatGPT pour une génération de fiche produit.

**Job logique**
La logique principale de l'application est encapsulée dans GetGameInfosJob, un job programmé qui traite les données de jeux vidéo à partir de photos prises par les utilisateurs. Ce job utilise GetGameInfos, un service pour extraire des informations via une API externe et mettre à jour les données du jeu en conséquence. Ensuite, AttachGamePicture est appelé si le titre en anglais du jeu est présent, ce qui ajoute une image du jeu à la fiche. Enfin, le résultat est diffusé en temps réel via ActionCable pour mettre à jour l'utilisateur sur le statut du traitement.

Réflexions
SecondRound a été une aventure palpitante et riche en apprentissages ! Ce projet nous a offert une plongée intense dans les rouages du développement web et mobile, le tout sous la pression d'une échéance serrée. Travailler en équipe a été un véritable plaisir : nous avons uni nos forces, échangé des idées innovantes et relevé chaque défi avec enthousiasme. Ensemble, nous avons non seulement amélioré nos compétences techniques, mais aussi exploré de nouvelles façons d'optimiser l'expérience utilisateur dans le domaine du commerce de jeux vidéo d'occasion. Et le meilleur dans tout ça ? Nous avons réussi à livrer le projet à temps tout en nous amusant !
