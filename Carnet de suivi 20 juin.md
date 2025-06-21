
  

[comment]: <> (Si la compilation de ce fichier ne fonctionne pas, vous pouvez le retrouver en ligne directement sur cette page Github : https://github.com/Babou-69/Carnet-de-suivi/blob/main/Carnet%20de%20suivi%2013%20juin.md)

  
  
  

## **Jeudi 19 juin - Après-midi : Projet à 11**

  

* 14h - 15h30 : [*Line, Léo, Nolane, Lilas, Mélusine*] :

*  * **Compréhension** du code sur la convection
* * **Débuggage** du code sur la convection (durée de simulation trop courte et dépendance avec la vitesse du vent)
* 15h30 - 17h30 :
* * Changement de la fonction principale du code pour qu'elle convienne aux conventions prises pour la bibliothèque (donc ne dépendre plus que d'un paramètre temporel t et plus de deux paramètres, h et j)
* * Implémentations des fonctions **P_inc_solar** et **capacite** dans la bibliothèque de l'équipe
* 17h30 - 17h40 : Réunion d'équipe, débrief, répartition des tâches pour la prochaine séance


  
## **Vendredi 20 juin - Après-midi : Projet à 11**
* 8h - 9h30 [*Mélusine, Blandine*] : 
* * Modification de notre fonction de calcul de l'albédo en fonction de la longitude et de la latitude : Précédemment, nous appelions l'API de la NASA pour une longitude et une latitude donnée. Pour ne plus dépendre de l'API de la NASA (et éviter ainsi des calculs lourds), on discrétise la Terre en petites zones, on fait une bonne fois pour toute 3 appels API à la NASA pour avoir une valeur moyenne de l'albedo sur cette zone et on stocke tout dans un fichier .csv, qu'on appellera plus tard.
*  * Exécution de la fonction précédente, beaucoup d'appels API (273,pour un découpage sommaire en 91 zones), c'est long. ***A faire*** : améliorer la précision (découpage plus fin) et faire tourner le programme de nuit sur un réseau WIFI stable.
* 9h30 - 10h30 [*Mélusine, Blandine*] : Ecriture de la fonction qui prend en entrée une latitude et une longitude et renvoie l'albedo, en s'appuyant sur le fichier csv précédemment crée. Implémentation dans la bibliothèque de l'équipe.
*  10h30 - 11h30 :  
* * Correction du produit scalaire entre les rayons lumineux et la normale à la surface, qui était faux (erreur de projection)
* *  Création d'un fichier minimaliste renvoyant la courbe de température en fonction de la latitude et longitude, faisant appel à notre bibliothèque. Erreur albédo NASA: name 'datetime' is not defined, alors même que nous importons bien "datetime", tant dans notre code que dans notre bibliothèque.
* 11h30 - 12h10 : 
* * Essai de compréhension de l'erreur précédente. Correction : cette erreur était liée au fait qu'on avait deux fichiers de nom identiques dans des dossiers différents.
* 12h10 - 12h20 : Réunion débrief de la matinée

* 14h - 16h : Présentations projets à 3.
* 16h - 17h [*En groupe*] :
* * Modifications et réarrangement du Github
* 17h - 17h10 [*seul*] : Pause
* 17h10 - 17h40 [*seul*] :
* * Création d'un fichier .md [Explication _code_avec_appel_biblio_.md](https://github.com/z-the-turtle/Projet_CREPES/blob/main/Dossier%20final/GUI%20et%20code/Explication%20_code_avec_appel_biblio_.md) qui explique le [code](https://github.com/z-the-turtle/Projet_CREPES/blob/main/Dossier%20final/GUI%20et%20code/Code_avec_appel_biblio.py) principal, sans GUI.
* 17h40 - 17h50  [*Avec l'équipe*]: 
* * Réunion listant ce qu'il  reste à faire.
