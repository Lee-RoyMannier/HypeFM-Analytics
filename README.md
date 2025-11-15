# HypeFM Analytics
## 🎧 Scénario :
Data Analyst pour HypeFM, une station de radio française urbaine et tendance, spécialisée dans les musiques actuelles (pop, rap, électro, RnB). La radio cherche constamment à rester à la pointe des goûts du public, notamment des jeunes auditeurs connectés (15–35 ans).

Depuis quelque temps, la direction constate que certaines émissions musicales obtiennent de meilleures audiences que d’autres, sans vraiment comprendre pourquoi. Pour rester compétitive face aux plateformes de streaming comme Spotify, Deezer ou Apple Music, HypeFM souhaite moderniser sa stratégie musicale en se basant sur les données réelles d’écoute en ligne.

## 🎯 Objectif du projet :
J'ai pour objectif, grâce à une analyse de donnée de streaming Spotify, d'essayer de sortir les tendances musicales des derniers mois pour ajuster la musique diffusée sur la radio.

## Les données :
Nos données sont sous format excel, directement téléchargé depuis la plateform Spotify, disponible directement sur notre repertoire GitHub.
Il s'agit d'un jeu de donnée regroupant les TOP 200 Charts de 2020 et 2021
<details>
<summary>Définition des données :</summary>
  
- Position la plus élevée dans les charts : La position la plus élevée de la chanson dans le Top 200 Weekly Global Charts de Spotify en 2020 et 2021.

- Nombre d'apparitions dans les charts : Le nombre de fois où la chanson a figuré dans le Top 200 hebdomadaire mondial de Spotify en 2020 et 2021.

- Semaine du plus haut classement : La semaine où la chanson a eu la position la plus élevée dans le Spotify Top 200 Weekly Global Charts en 2020 & 2021.

- Chanson : Nom de la chanson qui a figuré dans le Top 200 du classement mondial hebdomadaire de Spotify en 2020 et 2021.

- Ecoutes : Le nombre approximatif de streams de la chanson.

- Artiste : L'artiste/les artistes principaux impliqués dans la création de la chanson.

- Followers : Le nombre de followers de l'artiste principal sur Spotify.

- Genre principal : Les genres auxquels la chanson appartient.

- Date de sortie : La date initiale de sortie de la chanson.

- Popularité : La popularité du titre. La valeur sera comprise entre 0 et 100, 100 étant la valeur la plus populaire.

- Dansabilité : La Danceability décrit dans quelle mesure un titre est adapté à la danse en se basant sur une combinaison d'éléments musicaux, notamment le tempo, la stabilité du rythme, la force du battement et la régularité générale. Une valeur de 0,0 est la moins dansante et 1,0 est la plus dansante.

- Acousticité : Une mesure de 0,0 à 1,0 indiquant si le morceau est acoustique.

- Energie : L'énergie est une mesure de 0,0 à 1,0 et représente une mesure perceptive de l'intensité et de l'activité. En général, les pistes énergiques sont rapides, fortes et bruyantes.

- Concert : Détecte la présence d'un public dans l'enregistrement. Des valeurs plus élevées représentent une probabilité accrue que la piste ait été jouée en direct.

- Intensité : L'intensité sonore globale d'une piste en décibels (dB). La moyenne des valeurs d'intensité sonore est calculée sur l'ensemble de la piste. Les valeurs sont généralement comprises entre -60 et 0 db.

- Paroles : La qualité vocale détecte la présence de mots parlés dans une piste. Plus l'enregistrement est exclusivement vocal (par exemple, talk-show, livre audio, poésie), plus la valeur de l'attribut est proche de 1,0.

- Positivité : Une mesure de 0,0 à 1,0 décrivant la positivité musicale véhiculée par une piste. Les pistes à haute valence ont un son plus positif (par exemple, heureux, gai, euphorique), tandis que les pistes à
  faible valence ont un son plus négatif (par exemple, triste, déprimé, en colère).
</details>

## Etape 1: Analyse Descriptive des données
L'analyse descriptive est une étape préliminaire du traitement des données qui consiste à synthétiser des données pour en tirer des informations utiles, voire les préparer en vue d'une analyse complémentaire.

<details>
  <summary>Les valeurs extrêmes</summary>
  A quoi ça sert ?
  - Permet de connaitre les limites d'une série
  - De savoir que toutes les valeurs seront comprises entre ces 2 bornes (MAX et MIN)
  - Constater des éventuellees valeurs anormales

  Avec le calcule de l'étendue, on va pouvoir :
  - Calculer la différence entre 2 valeurs extremes
  - Donner une première idée de la disparité des données

<img width="856" height="365" alt="image" src="https://github.com/user-attachments/assets/77ce66fc-a497-4ef3-921a-301dcee0595f" />

</details>

<details>
  <summary>Les valeurs manquantes</summary>
  <img width="1028" height="161" alt="image" src="https://github.com/user-attachments/assets/f43cf09e-96fa-4d84-b48a-ffe7289c0fd4" />
  
  Après observation, on peut dire qu'il y a moins de 1% de valeurs manquantes pour la colonne des Followers
</details>

<details>
  <summary>Le mode</summary>
  <img width="858" height="141" alt="image" src="https://github.com/user-attachments/assets/53f3d912-4c68-464f-9968-18bfe732a98c" />
 
  On observe que la valeur majoritaire dans les positions dans le top est la premère position du classement.

  <img width="860" height="411" alt="image" src="https://github.com/user-attachments/assets/0fd5df23-7509-49dc-84ba-7f9f2dabaa67" />

  Conculsion:
  Dans le Top 200, la valeur la plus récurrente est la position 1, ce qui est logique car on est sur un jeu de donnée representant les TOP.
  On remarque cependant une longue traine sur l'ensemble des valeurs possibles.

  Question donc, pourquoi une musique qui ce trouve à la position 141 ce trouve dans le top ?
  => Hypothèse : Cela veut potentiellement dire que certaines chansons n'ont pas "explosés" sur une seule semaine mais sont restées populaire sur plusieurs semaines, les hissant dans le top des chansons.
</details>

<details>
  <summary>La moyenne et la médiane</summary>
  <img width="1032" height="211" alt="image" src="https://github.com/user-attachments/assets/da1df504-0bf2-416a-b798-1878f06383d0" />

  On voit que la moyenne est très impactée par des valeurs extrèmes, alors que la mediane ne subit pas ce type de déformation.
  
  <img width="1037" height="372" alt="image" src="https://github.com/user-attachments/assets/9b99a50e-17f7-45fa-9e48-161ca788a0bd" />


</details>

<details>
  <summary>Les quartiles</summary>
  <img width="1045" height="206" alt="image" src="https://github.com/user-attachments/assets/68a82438-439a-43fa-a139-3b5b1f33d219" />
  Distribution de nos valeurs Energie:
  <img width="622" height="370" alt="image" src="https://github.com/user-attachments/assets/14343a39-fb33-48d9-b5c1-6cdc1392f0e9" />
  
  Grâce à ce graphique on observe une distrubtion des valeurs autour de la moyenne

  Résumé de la distribution:
  <img width="970" height="387" alt="image" src="https://github.com/user-attachments/assets/24b6ce6e-ae8d-4185-ac2d-9213283d1d23" />

- Les musiques sont plutôt avec une Energie haute dans l'ensemble.
- Le premier quartile reste au dessus de 0,5
-  Attention, nous n'avons pour l'instant pas lié l'énergie avec la volumétrie de d'écoute ou de followers.
    Ca sera une information à confirmer.
</details>
<details>
  <summary>Les indicateurs de dispersions</summary>
  <img width="1067" height="461" alt="image" src="https://github.com/user-attachments/assets/d01f57b0-4513-482e-806d-fdfbe56a4a25" />
  
  Remarque:
  
  - On remarque tout de suite les critères dansabilité et energie qui on fortement la même distribution, plutôt sur des valeurs fortes.
  - Paroles est un critère dont il faudra se méfier.
  - Les valeurs fortes correspondent d'avantage à des podcasts qui ne figurent pas ce classement.
  
  - Accousticité et la positivité sont des critères très disparates, qui occupent toute la hauteur du spectre.

  - Au niveau des concert, la question que la chanson soit live ne semble pas plébisité par les utilisateurs. Il faut garder en tête que c'est potentiellement un problème de représentation.
  <img width="1047" height="130" alt="image" src="https://github.com/user-attachments/assets/5b2ad75b-e462-41bc-8ae2-382b691ab7b8" />
  <img width="353" height="127" alt="image" src="https://github.com/user-attachments/assets/67bfbd6c-04ee-43ba-b96b-0a744a1b8cc0" />

</details>
<details>
  <summary>Synthèse sur la position la plus élevée dans les charts</summary>
  <img width="850" height="180" alt="image" src="https://github.com/user-attachments/assets/eb22d909-bfd3-418b-ae4a-8497b36400db" />
  <img width="621" height="371" alt="image" src="https://github.com/user-attachments/assets/0c357fa6-0e1b-4502-9111-c4a29501d12d" />

  <img width="343" height="55" alt="image" src="https://github.com/user-attachments/assets/dc6c41a7-1461-4ab6-b5c3-04db8c34b9ef" />
  <img width="217" height="78" alt="image" src="https://github.com/user-attachments/assets/87fc86d2-1c81-4520-b7a6-07883e6cac4a" />
  <img width="623" height="372" alt="image" src="https://github.com/user-attachments/assets/e3c053fd-0d8e-4557-881c-abf5b623e9fa" />




</details>
<details>
  <summary>Analyse des variables qualitatives</summary>
  <img width="907" height="170" alt="image" src="https://github.com/user-attachments/assets/8b174377-b51d-482f-bdc2-5ccf9a8b7e49" />
  
  conclusion:
  - Il n'y que 5% des chansons qui n'ont pas de style attitré, rendant cette information fiable.

  <img width="533" height="183" alt="image" src="https://github.com/user-attachments/assets/b6f84c85-05f7-409c-936c-8b3728bd4a5e" />

  conclusion:
  - Il existe un nombre très important de genres, ce qui empécherait de faire des analyses "simples" par genre.
  - Il est probablement que la réparation par genre ne soit pas uniforme et certains soient plus représentés que d'autre.

  TOP 10:
  
  <img width="393" height="338" alt="image" src="https://github.com/user-attachments/assets/acd49203-ba74-4d74-820c-e9b9bd51de23" />
  <img width="600" height="357" alt="image" src="https://github.com/user-attachments/assets/583518f0-f00d-42f9-954a-0af201dc0b19" />

  Conclusion:
  - Il y a énormément de disparité entre les genres en terme de volume de chansons.
  - Les 10 premiers genres représentent plus de la moitée des chansons.

  - A noter qu'on retrouve des sous-genres sur certaines thématiques (pop, rap, hip hop)

</details>

## Etape 2: Exploration de données
<details>
  <summary>EDA</summary>
  
  Grâce à une exploration des données, nous allons pouvoir répondre à certaines question:
  - Q1: Qu'est ce donc que "ohio hip hop" ?
    - Cela correspond à un seul artiste. Cela voudrai dire que des rassemblements de genres sont possibles.
    
  - Q2: Quels sont les autres style de hip hop ?
    - Grâce à l'utilisation de la formule: 
    => `=NBVAL(UNIQUE(FILTRE(Spotify[Genre principal];ESTNUM(CHERCHE("*hip hop*";Spotify[Genre principal])))))`
    Nous pouvons voir qu'il existe 25 sorte de hip hop.
    - Beaucoup de ses genres sont associés à des villes ou à des pays.
    
  - Q3: Est-ce qu'il y a eu des chansons sorties avant la sortie de ce classement ?
    - Il y a effectivement des musiques bien antérieures au classement.
    - Cela concerne des "classiques" et des musiques liées à noel.
    
  - Q4: Quel est l'artiste avec les plus de followers ? Quelles sont les chansons présentes de lui dans ce classement ?
    - L'artiste avec le plus de followers est Ed Sheeran, avec 9 chansons dans le classement.
      
  - Q5: Quelle la musique sortie en 2020 la plus écoutée ?
      - C'est une musique de Justin Bieber. 
      - On remarque que la majorité des chansons en tête de classement sont des musiques pop
    
  - Q6: Est-ce que les musiques avec le plus d'écoutes sont celles avec le plus de followers ?
      - Il ne semble pas y avoir de lien évident entre le nombre de followers et le nombre d'écoutes. A confirmer avec un test statistique.
        
  - Q7: Est-ce le cas avec la popularité ?
      - Il semble y avoir un lien entre la popularité et le nombre d'écoutes. A confirmer avec un test statistique
      
  - Q8: Quels critères semblent influencer les écoutes ?
      - Il n'y a pas de lien évident entre les critères et la popularité et les écoutes. A confirmer avec un test statistique  
  
</details>

## Etape 3: Analyse de correlation
<details>
  <summary>Corrélation</summary>

  <img width="611" height="427" alt="image" src="https://github.com/user-attachments/assets/63520091-53df-495b-8a4c-6bb85d29c70f" />

  <img width="252" height="51" alt="image" src="https://github.com/user-attachments/assets/e76791c0-be85-4cec-89bd-dd124a80738d" />
  
  Conclusion:
  - 'La corrélation entre les 2 variables est faible.
  - L'intuition de départ était biaisée car on observait des valeurs extrèmes.
  - Le nombre d'écoute n'est pas un indicateur fiable pour expliquer la popularité

  <img width="601" height="417" alt="image" src="https://github.com/user-attachments/assets/66a9b902-39d2-4c51-b23a-38010371207d" />

  <img width="251" height="48" alt="image" src="https://github.com/user-attachments/assets/004c667b-8120-4b5a-9472-0a714d69adc0" />

  Conclusion:
  - Corrélation un peu plus forte malgré une grande disparité
  - Les musiques dansantes ont tendance à être plus positive mais cela n'est pas une regle absolue.
  - Si HypeFM reste dans la logique GoodVibes, la dansabilité reste quand même un critère à ne pas rejeter pour sélectionner les futures titres.

  <img width="597" height="446" alt="image" src="https://github.com/user-attachments/assets/9b4998d3-e25a-4f64-9e8e-a739715fed73" />

  <img width="251" height="51" alt="image" src="https://github.com/user-attachments/assets/7b8ca5d1-d4b2-40d7-8f52-071849907ed2" />

  Conclusion:
  - Corrélation plus forte, l'indicateur d'intensité semble bien lié à celle de l'énergie.
  - Connaître l'intensité d'une chanson peut nous donner une indication sur l'énergie et ainsi selectionner ce type de morceau

  Matrice de corrélation pour nos variables quantitatives:
  <img width="1820" height="310" alt="image" src="https://github.com/user-attachments/assets/f28bf860-2f12-43a6-a096-1ebd43bc5cc4" />

  Observation:
  - On observe une corrélation forte négativement entre l'énergie d'une chanson avec l'acousticité, ce qui semble logique, donc la radio va pouvoir se baser sur ça, il faudra donc éviter les chansons de ce type.
  - On observe aussi une correlation négative relativement forte mais difficile à voir sur le graphique.
  La logique sera que plus un morceaux est présent semaine après semaine et moins sa position moyenne est élevé. Cela explique le fait que certains morceaux ne soient jamais aller au délà de 150ième place et     figurent quand même dans les chansons les plus écoutées. Il ne faut donc pas forcement regarder le haut du classement pour trouver des morceaux à potentiel.
</details>
<details>
  <summary>Transformation</summary>
  
  Dans notre fichier excel, nous allons appliquer une transformation sur les colonnes de genre pour avoir une certaine harmonisation:
  `=SIERREUR(SI.CONDITIONS(ESTNUM(CHERCHE("*rock*";[@[Genre principal]]))=VRAI;"ROCK";
                            ESTNUM(CHERCHE("*hip hop*";[@[Genre principal]]))=VRAI;"HIP HOP"; 
                            ESTNUM(CHERCHE("*pop*";[@[Genre principal]]))=VRAI;"POP";
                            ESTNUM(CHERCHE("*rap*";[@[Genre principal]]))=VRAI;"RAP";
                            ESTNUM(CHERCHE("*country*";[@[Genre principal]]))=VRAI;"COUNTRY");
              "AUTRE")`

  Dans le même esprit, on va créer une nouvelle colonne de transformation de date pour extraire seulement l'année de sortie des titre.
  `=ANNEE([@[Date de sortie]])`
  
  
</details>
