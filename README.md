# Instabook : partage de photos avec des groupes d'ami. 

## Contexte
L'objectif de cette application est de pouvoir créer des groupes d'amis, poster des photos accessibles par le groupe. 
Pour chaque photo, on peut "tagger" les membres du groupe qui y apparaissent. Chaque photo peut-être commentée par un membre du groupe, et chaque membre du groupe peut répondre à un commentaire. 

## Étape de réalisation 

L'objectif est de concevoir les fichiers de migrations, les factories nécessaires aux tests, les modèles Eloquent et les relations entre les modèles. 

Ce projet pourra être étendu par la suite. 


### Les jeux de tests
Afin de faciliter le développement, les jeux de tests sont numérotés pour être passé par étapes. 

Ainsi la première étape concernent simplement la structure de la base données, sans prendre en compte les contraintes de clés étrangères, ni d'unicité. Il n'y a pas besoin de factory pour cette étape, seulement des fichiers de migration. 

Ensuite, il est nécessaire de coder les modèles et les factories, pour pouvoir tester les ajouts/suppression des modèles en BDD, puis les contraintes d'unicité et de clés étrangères, dans leur forme simplifiées, c'est à dire sans relations complexes. 

Ensuite il faudra coder les relations entre les modèles. 

Enfin, il faudra intégrer certaines règles de gestions, telles que l'appartenance à groupe d'une photo pour être mentionné comme apparaissant sur la photo. 