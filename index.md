# La faune pisciole des Hauts-de-Seine
# Sommaire
1. [La présentation et le traitement du jeu de données](#Jeudedonnees)
2. [L'état d'évolution des peuplements de poissons dans les Haut-de-Seine depuis 2009 jusqu'à 2020](#Etatevolutiondespeuplementsdepoissons)
3. [Les stations hydrobiologiques et la répartition d'habitat des poissons](#Repartitionhabitatdespoissons)
4. [L'état des espèces de poissons protégés dans les cours d'eau des Hauts-de-Seine](#Especesdepoissonsproteges)
5. [Conclusion](#Conclusion)

## 1. La présentation et le traitement les jeux de données <a id="Jeudedonnees"></a>

Les données de la diversité des poissons dans la Seine et la localisation des stations hydrobiologiques sur le territoire des Hauts-de-Seine ont été trouvées sur le site [Opendata Hauts-de-Seine](https://opendata.hauts-de-seine.fr/explore/dataset/diversite-des-poissons-dans-la-seine/information/?disjunctive.nom_station_commune&disjunctive.espece) qui s'inscrivent dans le cadre du Schéma directeur d'aménagement et de gestion des eaux (SDAG) du bassin de la Seine. 

### A. Jeu de données n°1: La diversité des poissons dans la Seine

<iframe src="https://opendata.hauts-de-seine.fr/explore/embed/dataset/diversite-des-poissons-dans-la-seine/table/?disjunctive.nom_station_commune&disjunctive.espece&sort=annee&dataChart=eyJxdWVyaWVzIjpbeyJjaGFydHMiOlt7InR5cGUiOiJjb2x1bW4iLCJmdW5jIjoiU1VNIiwieUF4aXMiOiJuYl9pbmRpdmlkdXMiLCJjb2xvciI6InJhbmdlLURhcmsyIiwic2NpZW50aWZpY0Rpc3BsYXkiOnRydWV9XSwieEF4aXMiOiJhbm5lZSIsIm1heHBvaW50cyI6IiIsInRpbWVzY2FsZSI6InllYXIiLCJzb3J0IjoiIiwic2VyaWVzQnJlYWtkb3duIjoibm9tX3N0YXRpb25fY29tbXVuZSIsInN0YWNrZWQiOiJub3JtYWwiLCJjb25maWciOnsiZGF0YXNldCI6ImRpdmVyc2l0ZS1kZXMtcG9pc3NvbnMtZGFucy1sYS1zZWluZSIsIm9wdGlvbnMiOnsiZGlzanVuY3RpdmUubm9tX3N0YXRpb25fY29tbXVuZSI6dHJ1ZSwiZGlzanVuY3RpdmUuZXNwZWNlIjp0cnVlLCJzb3J0IjoiYW5uZWUifX19XSwidGltZXNjYWxlIjoieWVhciIsImRpc3BsYXlMZWdlbmQiOnRydWUsImFsaWduTW9udGgiOnRydWV9&static=false&datasetcard=false" width="800" height="600" frameborder="0"></iframe>
Il s'agit d'un recencement des nombres d'espèces de poissons, nombre d'individus, les stations d'analyse, le nom des communes sur le territoire du département et les années d'observation des poissons.

### B. Jeu de données n°2: Stations hydrobiologiques

<iframe src="https://opendata.hauts-de-seine.fr/explore/embed/dataset/stations-hydrobiologiques/table/?disjunctive.commune&sort=id&static=false&datasetcard=false" width="800" height="300" frameborder="0"></iframe>
On peut trouver dans ce jeu les stations hydrobiologiques qui ont le drôle d'analyser l'impact des aménagements anthropiques sur la productivité piscicole.

En premier lieu, pour assurer la qualité des données, j'ai analysé les deux jeu de données avec l'outil WTFCsv afin d'avoir une vision plus détaillée sur leur contenu. J'ai constaté que les deux fichiers sont propres, il n'y a pas de cellule vide, de cellule fusionnée, des données manquantes ou des données orphelines. 

## 2. L'état d'évolution des peuplements de poissons dans les Haut-de-Seine depuis 2009 jusqu'à 2020 <a id="Etatevolutiondespeuplementsdepoissons"></a>

Tout d'abord, pour analyser l'évolution des espèces de poissons qui présentent dans les cours d'eau des Hauts-de-Seine, j'ai choisi trois données concernant l'année, les nombres individus et les espèces. Ensuite, J'ai utilisé l'outil Openrefine pour afficher les valeurs de ces données pour inspecter, extraire tous les informations de chaque espèce de poissons au fil de temps et créer un nouveau tableau qui contient le nom des poissons, les années et le nombre total de chaque espèce.

|                    | 2009 | 2010 | 2011 | 2012 | 2013 | 2014 | 2015 | 2016 | 2017 | 2018 | 2019 | 2020 |
|--------------------|:----:|:----:|:----:|:----:|:----:|:----:|:----:|:----:|:----:|:----:|:----:|:----:|
| Ablette            |  17  |   7  |  56  |  352 |  233 |  183 |  397 |  174 |   3  |  12  |  139 |  76  |
| Barbeau fluviatile |   1  |   0  |   6  |  12  |  12  |  49  |  24  |   2  |   7  |   3  |  15  |   1  |
| Black bass         |   0  |   0  |   0  |   0  |   0  |   0  |   0  |   0  |   0  |   0  |   0  |   2  |
| Bouvièvre          |   0  |   0  |   6  |   3  |   4  |   2  |   0  |   3  |   1  |   3  |   2  |  37  |
| Brème bordelière   |   0  |   0  |   0  |   0  |   0  |   0  |   0  |   0  |   0  |   0  |   0  |   1  |
| Brème sp.          |  11  |   0  |   2  |   4  |  19  |   6  |   3  |   3  |   0  |   8  |   0  |   2  |
| Brochet            |   0  |   0  |   0  |   0  |   0  |   2  |   0  |   2  |   0  |   0  |   0  |   0  |
| Chabot             |  170 |  93  |  330 |  173 |  235 |  270 |  213 |  18  |  28  |  27  |  13  |  42  |
| Chevesne           |  31  |  141 |  207 |  300 |  155 |  214 |  176 |  160 |  55  |  58  |  169 |  280 |
| Gardon             |  27  |  248 |  656 |  136 |  32  |  996 |  89  |  15  |  96  |  64  |  795 |  520 |
| Goujon             |  12  |  16  |  32  |  28  |  29  |  123 |  38  |  11  |   1  |  16  |  46  |  172 |
| Grémille           |   0  |   0  |  30  |   0  |   0  |   0  |   0  |   0  |   0  |   0  |   3  |   0  |
| Hotu               |   0  |   1  |  35  |   1  |   5  |  123 |  80  |   0  |  13  |   0  |  30  |  39  |
| Ide mélanote       |   0  |   0  |   0  |   0  |   0  |   1  |   0  |   0  |   0  |   0  |   0  |   0  |
| Loche franche      |   0  |   0  |   0  |   0  |   0  |   0  |   2  |   0  |   0  |   0  |   0  |   0  |
| Perche commune     |  76  |  41  |  88  |  30  |  75  |  11  |  73  |  13  |  167 |  10  |  42  |  30  |
| Perche soleil      |  18  |   5  |   1  |   0  |   0  |   0  |   0  |   0  |   1  |   3  |   5  |   0  |
| Rotengle           |  51  |  32  |  19  |  32  |  21  |   8  |  12  |   1  |   5  |   1  |  11  |  46  |
| Sandre             |   2  |   1  |   0  |   0  |   1  |   2  |   0  |   0  |   1  |   3  |   0  |   0  |
| Silure             |   4  |   3  |   1  |   0  |   0  |   0  |   0  |   0  |   0  |   0  |   0  |   1  |
| Silure glane       |   0  |   0  |   0  |   0  |   1  |   0  |   1  |   0  |   2  |   0  |   1  |   0  |
| Tanche             |   0  |   3  |   0  |   0  |   0  |   0  |   0  |   1  |   0  |   0  |   0  |   0  |
| Vairon             |   0  |   0  |   0  |   0  |   0  |   1  |   0  |   0  |   0  |   0  |   0  |   0  |
| Vandoise           |   1  |   0  |  16  |   1  |   3  |   5  |  14  |   0  |  14  |  38  |   5  |  108 |

> Tableau généré avec [Tables Generator](https://www.tablesgenerator.com)

Après avoir les données nécessaires, j'ai fait une première datavisualisation avec le graphique Bar Chart Race sur Flourish. Un graphique dynamique qui me permet de visualiser le changement de la quantité des espèces de poissons au fil de temps et d'ajouter les images de certaines poissons.
<div class="flourish-embed flourish-bar-chart-race" data-src="visualisation/12718348"><script src="https://public.flourish.studio/resources/embed.js"></script></div>
Grâce à cet visualisation, on pourrait constater que les espèces de poissons dans les Hauts-de-Seine sont assez pauvres. On compte ici 24 d'espèces de poissons qui appartiennent à la famille cyprinidés et une espèce de poisson envahissante (Le Perche Soleil). 
Le chabot, la chevesne, le gardon, le goujon, la perche commune, le hotu sont présentés dans la Seine depuis le 19è siècle et ont formé une communauté assez dense dans le bassin de la Seine. Par contre, on pourrait voir ici la raréfaction de certains d'espèces de poissons comme la brème, le brochet, l'ide mélanote, la loche franche, la tanche, la silure et le vairon. Surtout, il n'y a pas la présence des espèces des poissons migrateurs.


## 3. Les stations hydrobiologiques et la répartition d'habitat des poissons <a id="Repartitionhabitatdespoissons"></a>

Afin de savoir la répartition d'habitat des espèces de poisson, j'ai utilisé le deuxième jeu de données qui fournit les coordonnées géographiques des stations de suivi pour faire un map sur datawrapper et créer un autre graphique hiérarchique avec le premier jeu de données sur Flourish pour avoir une visualisation sur la proportion entre eux.
<br>
<div class="flourish-embed flourish-hierarchy" data-src="visualisation/12719498"><script src="https://public.flourish.studio/resources/embed.js"></script></div>
Type de graphique: Hierarchy
<br/><br/>

<iframe title="Les stations hydrobiologiques des Hauts-de-Seine" aria-label="Carte" id="datawrapper-chart-eQhGu" src="https://datawrapper.dwcdn.net/eQhGu/2/" scrolling="no" frameborder="0" style="width: 0; min-width: 100% !important; border: none;" height="746" data-external="1"></iframe><script type="text/javascript">!function(){"use strict";window.addEventListener("message",(function(e){if(void 0!==e.data["datawrapper-height"]){var t=document.querySelectorAll("iframe");for(var a in e.data["datawrapper-height"])for(var r=0;r<t.length;r++){if(t[r].contentWindow===e.source)t[r].style.height=e.data["datawrapper-height"][a]+"px"}}}))}();</script>
  
A travers les deux graphiques, j'ai appris que les poissons se retrouvent la plus dense dans les stations 2, 7, 6 et 1. Parce que l'aménagement des berges impactent sur l'état écologique de la Seine et les milieux d'abri, de nutrition et de reproduction des poissons. On peut voir sur la carte les trois zones de fraie sur les stations 2, 6 bis et 7. Pourtant, les nombres de poissons observés dans les stations 2 et 7 sont plus nombreux que celle de 6bis car cette station a été récemment ajouté en 2017. Quant aux stations 1 et 2, on peut se trouver les berges naturels qui ne présent pas ou peu les signes d'intervention de l'homme. Elles facilitent le développement des poissons. Les informations concernant les emplacements des zones de fraie et les berges se sont trouvés dans la rubrique [Environnement](https://www.hauts-de-seine.fr/mon-departement/les-hauts-de-seine/missions-et-actions/environnement/le-shema-damenagement-de-la-seine-et-ses-berges) du département Hauts-de-Seine.

## 4. L'état des espèces de poissons protégés dans les cours d'eau des Hauts-de-Seine <a id="Especesdepoissonsproteges"></a>
L'Arrêté du 8 décembre 1988 concernant les protections réglementaires françaises relatives aux epèces a fixé une liste des espèces de poissons protégées sur l'ensemble du territoire nationale qui contient le brochet, la vandoise, l'ide mélanote et la bouvière. 
<br/>
J'ai décidé de réaliser un graphique sur Flourish pour visualiser l'évolution de ces espèces depuis 2009 jusqu'à 2020.
<div class="flourish-embed flourish-scatter" data-src="visualisation/12719098"><script src="https://public.flourish.studio/resources/embed.js"></script></div>
<br/>
Type de graphique: Scatter
Cet visualisation monstre que 
## 5. Conclusion <a id="Conclusion"></a>
