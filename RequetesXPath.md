1. Sélectionner les titres de tous les films.

> /films/film/titre  
> //film/titre  
> //titre

2. Sélectionner le résumé (texte uniquement) du film dont le titre est "Minority Report".

> //film[titre="Minority Report"]/resume/text

3. Sélectionner le nom du dernier réalisateur dans l'ordre du document.

> //realisateur[last()]/nom

4. Sélectionner le titre du deuxième film dans l'ordre du document.

> //film[position() = 2]/titre  
> //film[2]/titre

5. Sélectionner la position dans l'ordre du document des films dont le texte du résumé contient le mot « mafia ».

Pas possible hors XSLT.

6. Sélectionner les titres des films pour lesquels une image est disponible.

> //film[boolean(resume/image) = true()]/titre  
> //film[boolean(resume/image)]/titre
> //film[resume/image]/titre

7. Sélectionner les dates des films de Scorcese.

> //film[@id_realisateur = //realisateur[nom="Scorsese"]/@id_realisateur]/@annee

8. Retourner le nombre de films sortis en 2003.

> count(//film[@annee = 2003])