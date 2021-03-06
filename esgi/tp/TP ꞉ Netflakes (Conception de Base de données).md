# TP : Netflakes (Conception de Base de données)


NetFlakes est le nouveau leader de la VOD. Ils vous ont mandaté pour concevoir le modèle de données de la nouvelle version de son application mobile.

Dès la page Home, cette application mettra en avant les derniers épisodes des 5 séries les plus populaires du moment et une sélection de films remontés en fonction de la préférence de l'utilisateur par catégorie. Si l'utilisateur n'a pas précisé ses préférences, __les films les plus populaires du moment seront affichés__(compter les vues ?).

Sur la page d'un épisode ou d'un film, la principale fonctionnalité est le stream en temps réel de la vidéo concernée. Cette interface présentera également une sélection d'informations relatives a la série ou au film : description, date de production, date de sortie officielle, titre de l'épisode ou du film, nom de la série si il y a lieu, numéro ou nom de la saison si il y a lieu, liste des principaux acteurs, de l'équipe de production (réalisateur, producteur, metteur en scène, maison de production). On aura également la possibilité de choisir différentes versions en matières de langues, de sous-titres et de définition (HD / MD / LD). On pourra également consulter sur cette page la liste des commentaires, notes et critiques des utilisateur, il est a noter que les grands critiques dispose de comptes spéciaux et que leur commentaires sont mis en valeur et présentés a part des commentaires des utilisateurs standard. Seront également présent sur ces pages une sélection de captures d'écrans et images (dont une principale servant de vignette) et d'extraits video parmi lesquels on pourra distinguer la Bande Annonce, si il ya lieu.

Sur la page d'une saison on affichera la liste des épisodes, en mettant en valeur les plus récents et les plus regardés.

Sur la page d'une série on affichera la liste des saisons, ainsi que la liste des acteurs phares de la série, avec pour chacun le (ou les) personnages incarné dans la série, et les série de la même maison de production.

Un système de catégorie, et un système de tags permettent de qualifier les séries et films, et permettent de déterminer les préférences des utilisateurs en décomptant pour chaque catégorie et pour chaque tag le nombre de visualisation de chaque utilisateur.

La gestion des abonnements doit être intégralement intégrée a cette nouvelle application, les utilisateurs une fois connectés devront pouvoir souscrire des forfaits par nombre de devices simultanées, pour des durée allant de 1 semaine a un an (x semaines, x mois, ou 1 année) cette abonnement est par défaut automatiquement renouvelable, si ce nombre de connexion simultanées est dépassé, alors un message d'erreur doit indiquer a l'utilisateur le nombre actuelle de session et lui interdire toute utilisation de l'application tant que ce nombre est dépassé.

Enfin un système (optionnel sur choix de l'utilisateur) permettra l'envoi de push notifications a la sortie d'un nouvel épisode d'une série dont l'utilisateur aura déjà visionné au moins un épisode.



![netflakes](../.././attachments//netflix.drawio.png)