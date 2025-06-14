


## **Jeudi 12 juin - Après-midi : Projet à 11**

* 14h - 15h : [Avec Zahara, Mélusine, Blandine] : 
* * Intégration de la dépendance de la capacité en fonction de la latitude et de la longitude. 
* * Réflexion à propos du fait qu'on ait de trop grandes variations entre l'été et l'hiver.
* * Justification de la profondeur typique de variation quotidienne de température, en considérant que (cf : exo 1 TD11) : $T(t) = T_0 + \theta_0cos(wt - \frac{x}{\delta})e^{-\frac{x}{\delta}}$
* 15h - 16h30 : Changement dans la prise en compte de l'effet de serre : L'atmosphère n'est plus à l'équilibre thermique. On a donc le système différentiel suivant : 
$$ \begin{equation*}
\begin{cases}
dT_{Terre} = [(1-\alpha)P_{sol} +\sigma(T_{atmo}^4-T_{Terre}^4)]\frac{dt}{C_{atmo}\rho_{Terre}Profondeur} \\
dT_{atmo} = \sigma(T_{Terre}^4-T_{atmo}^4)\frac{dt}{C_{atmo}\rho_{atmo}e_{atm}}
\end{cases}
\end{equation*}$$
Résolution numérique avec Euler.
Résultats cohérents mais un chouïa trop élevés l'été.

* 16h30 - 17h30 : On considère que l'atmosphère n'est plus un corps noir, elle absorbe une fraction $\mathbf{\epsilon}$ de ce qu'émet la Terre et le reste est renvoyé dans le vide intersidéral. Correction d'un facteur 2 oublié : l'atmosphère rayonne vers l'intérieur et l'extérieur de la Terre. Le système précédent devient : 
$$ \begin{equation*}
\begin{cases}
dT_{Terre} = [(1-\alpha)P_{sol} +\sigma(T_{atmo}^4-T_{Terre}^4)]\frac{dt}{C_{atmo}\rho_{Terre}Profondeur} \\
dT_{atmo} = \sigma(\mathbf{\epsilon}T_{Terre}^4-2T_{atmo}^4)\frac{dt}{C_{atmo}\rho_{atmo}e_{atm}}
\end{cases}
\end{equation*}$$
* 17h30 - 17h40 : Réunion débrief avec toute l'équipe

## **Vendredi 13 juin - Après-midi : Projet à 11**
* 13h55 - 14h50 : Modification du modèle : On ne considère plus que l'atmosphère est un corps noir parfait, elle ne réémet qu'une fraction $\epsilon$ de ce qu'émettrai un corps noir (c'est ce que j'ai compris de [ça](https://en.wikipedia.org/wiki/Idealized_greenhouse_model). Le système différentiel devient alors :  
$$ \begin{equation*}
\begin{cases}
dT_{Terre} = [(1-\alpha)P_{sol} +\sigma (\epsilon T_{atmo}^4-T_{Terre}^4)]\frac{dt}{C_{atmo}\rho_{Terre}Profondeur} \\
dT_{atmo} = \sigma(\mathbf{\epsilon}T_{Terre}^4-2\epsilon T_{atmo}^4)\frac{dt}{C_{atmo}\rho_{atmo}e_{atm}}
\end{cases}
\end{equation*}$$
* 14h 50 - 15h45 :
* * Tentative de documentation de l'émissivité de l'atmosphère en fonction des différentes quantités des différents gaz à effet de serre avec [cet article](https://arxiv.org/pdf/2303.00808). [Ce cours (Diapo 27)](https://web.lmd.jussieu.fr/~jldufres/Exposes/Duf_ERRE_psud_1.pdf) a l'air de montrer que $\frac{1-\epsilon}{\epsilon}$ = $\frac{240}{390}$, c.à.d $\epsilon$ = 0.71
* 15h50 - 16h20 : Elaboration du document de validation scientifique sur les différentes constantes utilisées dans mon code.
* 16h20 - 17h 25 (Avec Blandine et Mélusine)  : 
* * Ajout de la fonction appelant l'API de la NASA dans notre code pour la gestion de l'albedo. On a alors plus une découpage approximatif de la Terre en différentes zones de couleur.
* * Essai d'ajout d'un flux de chaleur latente : Le jour, on évapore de l'eau, la nuit, elle se condense. Echec d'implémentation.

* A faire : Essayer d'implémenter le code du groupe convectif dans notre main, essayer de quantifier l'impact des courants marins (type Gulfstream) sur la température des continents.
* * 17h25 - 17h40 : Réunion débrief avec toute l'équipe 
