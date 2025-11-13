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
</details>

