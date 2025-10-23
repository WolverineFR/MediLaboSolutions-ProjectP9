# Éco-conception et Green Code – Projet Medilabo

Dans une démarche d’éco-conception, le projet Medilabo vise à réduire son impact environnemental tout en conservant une qualité de service optimale.

## Objectif du Green Code

Le Green Code permet de concevoir des logiciels moins gourmands en énergie et en ressources.
Cela passe par des choix d’architecture, de code et d’infrastructure plus efficaces et responsables.
L’objectif est de limiter la consommation énergétique et les coûts liés aux ressources tout en gardant la performance.

## Points importants identifiés dans le projet

- Multiplication des microservices
- Niveau de logging trop élevé
- Appels Feign répétés entre microservices
- Images Docker lourdes basées sur OpenJDK
- Boucle de calcul coûteuse dans RiskCalculatorService

## Solutions et améliorations envisagées

- Mutualisation des dépendances entre microservices pour réduire la duplication et la taille des builds.
- Réduction du niveau de logs et archivage automatique des anciens fichiers pour limiter la consommation disque.
- Utilisation d’images Docker slim pour alléger les containers.
- Mise en place d’un cache pour les données patient et les notes, afin de limiter les appels répétés.
- Optimisation du calcul du risque avec un algorithme plus efficace.
- Surveillance de la consommation mémoire des containers Docker.
- Limitation du rechargement complet des pages côté front-end pour réduire les ressources consommées.

## Bénéfices attendus :

- Réduction de l’empreinte carbone du projet
- Meilleure performance et réactivité des services
- Maintenance simplifiée et code plus propre
