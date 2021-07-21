#Requetes SQL


Auteurs

Lister les auteurs

select \* from `author`

Afficher l'auteur ayant l'id 2

select \*from `author` WHERE `id`=2


Articles

Lister tous les articles

select \* from `post`

Afficher l'article ayant l'id 1

select \*from `post` WHERE `id`=1


#Bonus

Auteurs

Lister les auteurs par ordre alphabétique (sur le nom)

SELECT \*
FROM `author`
ORDER BY `name`


Lister les auteurs dont l'e-mail contient @gmail.com

SELECT \*
FROM `author`
WHERE `email` LIKE '%@gmail.com'


Lister les auteurs qui n'ont pas d'image de profil

select \* from `author` where `image` IS NULL


Articles
Lister le titre et la date de publication de tous les articles

select title,published_date from `post`


Afficher le titre d'un article en particulier (en passant l'id de l'article)

select title from `post` where id=1


Lister les 2 derniers articles publiés

SELECT \*
FROM `post`
ORDER BY `published_date` DESC
limit 2


Compter le nombre d'articles (doc) et renommer la colonne en nbArticles

SELECT COUNT( title) , resume ,published_date, views AS nbArticles
FROM `post`
