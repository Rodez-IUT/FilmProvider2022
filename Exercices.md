## Exercice 1 - Document XML Bien Formé

La société FilmProvider est spécialisée dans la publication d’informations sur les films cinématographiques.
Pour communiquer facilement avec ses partenaires (vidéo club, ciné-club...), FilmProvider décide de publier ses
informations au format XML.
FilmProvider ne possède pas d'outil spécialisé et le service chargé de la conception fait une maquette dans un éditeur
de texte. Comment vérifier que cette maquette est un document XML bien formé ?
Le document, qui transgresse en fait 7 fois les règles du « bien formé », est contenu dans le fichier
FilmProvider_bad.xml, fourni en ressource. Vous êtes chargé de le corriger, et vous ne disposez que d'un éditeur
de texte et d'un navigateur Web compatible XML (Chrome ou Firefox). À vous de trouver les 7 erreurs !

1. Ouvrir le fichier FilmProvider_bad.xml dans le navigateur,
   noter le message d'erreur, corriger le fichier XML dans l'éditeur et le sauvegarder sous FilmProvider_ok.xml
   à la racine de votre projet.  
   Continuer à corriger en rechargeant la page dans le navigateur jusqu'à ce que le document XML soit affiché correctement.

> fix #1 document bien formé

## Exercice 2 - Requêtes XPATH

Ouvrir le fichier "FilmProvider.xml" disponible dans les ressources et écrire les requêtes Xpath correspondant aux phrases suivantes :

1. Sélectionner les titres de tous les films.
2. Sélectionner le résumé (texte uniquement) du film dont le titre est "Minority Report".
3. Sélectionner le nom du dernier réalisateur dans l'ordre du document.
4. Sélectionner le titre du deuxième film dans l'ordre du document.
5. Sélectionner la position dans l'ordre du document des films dont le texte du résumé contient le mot « mafia ».
6. Sélectionner les titres des films pour lesquels une image est disponible.
7. Sélectionner les dates des films de Scorcese.
8. Retourner le nombre de films sortis en 2003.

> fix #2 requêtes XPATH

## Exercice 3 - Schema XML

La société FilmProvider est spécialisée dans la publication d’informations sur les films cinématographiques.
Pour communiquer facilement avec ses partenaires (vidéoclub, cinéclub...), FilmProvider décide de publier ses informations au format XML.  
Une fiche de film est composée d'un titre, d’un identifiant, et d'un résumé.  
La fiche mentionne aussi l’année de sortie du film et le réalisateur.   
Le résumé est composé de texte et d’une image optionnelle.  
Le réalisateur est caractérisé par son nom et son prénom.  
Les fiches de film et des réalisateurs sont stockés dans un même fichier.   
On ne veut pas dupliquer les informations relatives à un même réalisateur.

1. Ecrire un XML Schema « FilmProvier.xsd » décrivant la structure des documents devant être générés par la société « FilmProvider ».
   Le fichier XML "FilmProvider.xml" fourni en ressource doit être conforme au XML Schema à écrire.
2. Créer un nouveau document XML en indiquant qu’il doit être conforme au XML Schema écrit précédemment. Remplir le document
   en vous aidant des fonctionnalités fournies par votre éditeur XML.

> fix #3 Schema XML

## Exercice 4 - Schema XML amélioré


1. Reprendre le schéma FilmProvider.xsd pour qu'il intègre les contraintes suivantes :

- les éléments définis dans le schéma doivent être lié à l'espace de nom « http://formationxml/filmprovider »
- les attributs id_realisateur des éléments realisateur et film doivent être déclarés respectivement comme key et keyref
- les id_realisateur et id_film doivent être conformes à des patterns adaptés (real_<num>, film_<num>)
- l’année de sortie d’un film doit être comprise entre 1920 et 2006.

2. Créer un nouveau document XML en indiquant qu’il doit être conforme au XML Schema écrit précédemment.
   Remplir le document en vous aidant des fonctionnalités fournies par votre éditeur XML.

> fix #4 Schema XML amélioré