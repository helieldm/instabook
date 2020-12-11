# Instabook : partage de photos avec des groupes d'ami. 

## Contexte
L'objectif de cette application est de pouvoir créer des groupes d'amis, poster des photos accessibles par le groupe. 
Pour chaque photo, on peut "tagger" les membres du groupe qui y apparaissent. Chaque photo peut-être commentée par un membre du groupe, et chaque membre du groupe peut répondre à un commentaire. 

## Étape de réalisation 

L'objectif est de concevoir les fichiers de migrations, les factories nécessaires aux tests, les modèles Eloquent et les relations entre les modèles. 

Ce projet pourra être étendu par la suite. 


### Les jeux de tests
Afin de faciliter le développement, les jeux de tests sont numérotés pour être passé par étapes. 

Ainsi la première étape concernent simplement la structure de la base données, sans prendre en compte les contraintes de clés étrangères, ni d'unicité. Il y a besoin des fichiers de migration, ainsi que des factory qui sont fournies pour cette étape. 
Vous aurez aussi besoin d'avoir créé les modèles et vérifié que chacun à bien le trait hasFactory (`use hasFactory;`).

Ensuite, il est nécessaire de coder les relations dans les modèles, pour pouvoir tester les contraintes d'unicité et de clés étrangères, dans leur forme simplifiées, c’est-à-dire sans relations complexes. 

Enfin, il faudra intégrer certaines règles de gestions, telles que l'appartenance à groupe d'une photo pour être mentionné comme apparaissant sur la photo. 
  - Un commentaire ne peut être que fait que par un utilisateur qui appartient au même groupe que la photo
  - La photo n'est créée que si son propriétaire appartient bien au même groupe que la photo
  - Un utilisateur ne peut être ajouté à une photo que si il est dans le même groupe que la photo