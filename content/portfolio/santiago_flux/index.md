+++
title = "Analyse SIG : transports urbains à Santiago du Chili"
draft = false
image = "/portfolio/santiago_flux/santiago.jpg"
showonlyimage = false
Description = "Une analyse SIG des flux de population majoritaires dans la ville de Santiago du Chili, dans le but de dimensionner un projet de ligne de métro."
+++

{{<photo_gallery photo1="/portfolio/santiago_flux/polarites.png" photo2="/portfolio/santiago_flux/flux_pendulaires.png" photo3="/portfolio/santiago_flux/flux_activite.png" photo4="/portfolio/santiago_flux/flux_univ.png" photo5="/portfolio/santiago_flux/flux_hosp.png">}}


#### Cadre du projet

Dans le cadre d'un cours de plannification de transports urbains à l'UTC, il était demandé aux étudiants de choisir une ville et de proposer une amélioration de son réseau de transport. Dans notre groupe de quatre étudiants, nous avons choisi d'étudier la ville de Santiago du Chili, ville dans laquelle l'un de mes camarades avait étudié.

Santiago est la capitale administrative et économique du Chili, et compte près de 4 912 500 habitants (2012). Dans un pays en développement marqué par une culture consumériste et libéraliste, la voiture est le moyen de transport le plus largement répandu. Santiago possède cependant sept lignes de métro, et deux de trains périurbains, ce qui est atypique au Chili. L'agglomération étudiée est composée de 34 communes aux niveaux de vie, densité de population et fonctions urbaines très hétérogènes. 

Le but du projet est de poser un diagnostic sur les systèmes de transport existants, puis d'en proposer une amélioration. A l'issue du diagnostic, nous avons choisi d'ajouter une ligne de métro au réseau existant, nous en avons proposé un tracé et un dimensionnement en utilisat la méthode gravitaire.


#### Diagnostic territorial

Dans un premier temps, il a fallu nous familiariser avec le territoire étudié. Pour un projet de transport, la compréhension du territoire s'effectue à plusieurs niveaux. Il faut appréhender le rôle du territoire dans son pays ou sa région (en l'occurrence, une capitale administrative et éonomique), puis s'intéresser à son organisation interne en terme de répartition des fonctions urbaines, de répartition socio-économique des populations... et les flux de population qe ces répartitions dans l'espace engendrent, et qui constituent la demande en transports. Il faut ensuite comprendre l'étenue de l'offre de transport existante et la confronter à la demande.

- Analyse urbaine

Pour analyser cette métropole, nous avons choisi d'utiliser ArcGis, car les Systèmes d'Information Gographique (SIG) sont des outils très puissants d'analyse du territoire. Nous avons pris contact avec une ancienne professeure chilienne, aujourd'hui géographe et géomaticienne. Elle nous a fourni les dernières données géomatiques de 2019 sur toute la métropole : l'hydrographie, la voirie, l'emprise au sol, le PLU (équivalent chilien), le bâti, le réseau de métro et de bus avec les arrêts et les lignes en construction, les classes socio-économiques, les aléas naturels, ainsi que de nombreuses couches de données ponctuelles comme les établissements scolaires, les centres de santé, les centres commerciaux, les attractions touristiques, les édifices religieux...
Nous avons visualisé et superposé ces différentes couches de sorte à obtenir une compéhenstion globale des différents quartiers de Santiago.

- Diagnistic de l'Offre

Pour effectuer le diagnostic de l'offre, nous avons complété notre connaissance des systèmes de transport existants (voirie, tracé des lignes de bus, métro et trains périurbains) en faisant des recherches sur leurs caractéristiques comme la fréquence de passage, les types de véhicules et leurs capacités, le prix des tickets et les horaires de service. Pour le transport routier, nous avons effectué une étude de la congestion des principaux axes de la métropole en fonction de l'heure de la journée et des jours de la semaine. Nous avons ainsi identifié les axes les plus congestionnés aux heures de pointe, et empruntés pendant les migrations pendulaires.

- Diagnostic de la demande

Le diagnostic de la demande est fait de manière théorique, en calculant différents types de flux de population entre les communes de l'agglomération. Le découpage en communes nous semble pertinent car chaque commune est relativement homogène en termes de densité humaine, de niveau de vie et de fonctions urbaines.
Ainsi, nous déterminons 4 types de flux : les flux universitaires, les flux de santé, les flux pendulaires liés à l'activité professionnelle, et les flux dits "d'activité", qui englobent des activités non professionnelles jugées nécessaires ou très ancrées culturellement (Achats alimentaires en marché et supermarché, achats autres en centre commercial et pratiques religieuses).

{{<bouton article="/portfolio/santiago_flux/Diagnostic_de_la_demande.pdf">}}Téléchargement Méthodologie demande (fr){{</bouton>}}


 

#### Projet d'amélioration : nouvelle ligne de métro

La confrontation de l'offre et de la demande met en lumière un manque de transports en commun efficace pour relier les communes de la périphérie du sud et de l'ouest de la métropole. En effet, ces zones comprennent d'important bassins d'emplois industriels, et sont peuplées de populations au niveau de vie bas (parfois trop bas pour posséder une voiture), mais pas non plus en situation de pauvreté extrême. Maipu, une commune du sud-ouest, attire particulièrement l'attention par son dynamisme naissant et la congestion importante de ses routes en semaine, en particulier les axes reliant la périphérie au centre.

- Elaboration du tracé

En suivant les flux calculés, nous proposons un tracé de ligne de métro permettant de relier les communes de Maipu à La Cisterna. Le réseau de métro de Santiago est un réseau étoilé, mais ces dernières années, des lignes périphériques ont vu le jour. Ce tronçon est un chaînon manquant dans les transports urbains périphériques, et permet d'assurer une ligne circulaire contournant le centre, Nord-Est au Nord-Ouest en passant par le Sud.
Le tracé proposé est étudier de manière à raccorder les lines existantes de manière stratégique tout en desservant des points attractifs, comme des zones de forte densité d'emploi ou des centres commerciaux ou hospitaliers. L'implantation dans le tissus urbain est également étudiée. Les avenues larges sont privilégiées pour faciliter les traveaux et assurer le moins de destruction possible de bâtiments existants.

- Dimensionnement de la nouvelle ligne

Le placement des stations est réalisé avec la méthode gravitaire. On détermine une zone d'affluence autour du tracé, normalement un buffer d'une certaine distance (par exemple 1km), ou une zone déterminée en fonction des autres stations de transports en commun existantes. Ici, on a simplement tracé un rectangle, mais ça autait pu être bien plus réfléchi. Dans cette zone d'où viennent les populations empruntant le nouveau métro, on découpe des polygones homogènes en terme de densité de population. On projette les centres de ces polygones sur la ligne, on les regroupe en paquets, puis on fait la moyenne pondérée de tous les points projetés dans chaque paquet pour obtenir les emplacements des stations.

En fonction de la population des polygones pris en compte pour chaque station, on estime la fréquentation des stations en heure de pointe (un certain pourcentage de la population des polygones concernés), ce qui permet de donner une première information pour leur capacité d'accueil. On choisit ensuite des véhicules, et en connaissant leur capacité, et en considérant une période "d'heure de pointe" de deux heures, on estime le nombre de rames et la fréquence nécessaire sur la ligne en heure de pointe.




{{<bouton article="/portfolio/santiago_flux/Rapport_Final_Santiago_UB02.pdf">}}Téléchargement du rapport (fr){{</bouton>}}