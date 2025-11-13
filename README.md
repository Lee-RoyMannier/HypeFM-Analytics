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
</details>

<details>
  <summary>Les quartiles</summary>
</details>
<details>
  <summary>Les indicateurs de dispersions</summary>
</details>
<details>
  <summary>Récapitulatif global sur une colonne</summary>
</details>
<details>
  <summary>Analyse des variables qualitatives</summary>
</details>

