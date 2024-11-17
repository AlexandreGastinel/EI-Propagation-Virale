# EI-Propagation-Virale

L'objectif de ce projet est de proposer une stratégie optimale pour le lancement d'une campagne publicitaire. 
Notre code apporte une solution en répondant aux deux questions suivantes:
1. Quels utilisateurs du réseau social sponsoriser pour maximiser l'impact d'une campagne publicitaire ?
2. Quel budget allouer à chaque utilisateur sponsorisé pour optimiser le retour sur investissement.



  FONCTIONNEMENT DU CODE


Transformation du dataset en graphe pondéré orienté :

Nœuds : Représentent les comptes d'utilisateurs.
Arêtes : Représentent les relations d'abonnement.
Poids des arêtes : Probabilité que l'utilisateur cible interagisse avec le contenu (vues, likes, commentaires, partages).


Calcul de l'influence avec PageRank :

L'algorithme PageRank attribue une note de centralité à chaque nœud (utilisateur) en fonction de sa position dans le graphe.
La centralité est divisée par le coût de sponsoring, fournissant une métrique optimisée centralité/coût.


Réduction des redondances avec Louvain :

L'algorithme de Louvain permet de diviser le graphe en communautés d'utilisateurs ayant des interactions fortes.
L'objectif est d'éviter la sélection d'utilisateurs appartenant à la même communauté pour limiter les redondances dans les audiences atteintes.


Simulation de la campagne :

Un modèle probabiliste évalue le succès potentiel de la campagne sur le réseau en simulant sa propagation.
