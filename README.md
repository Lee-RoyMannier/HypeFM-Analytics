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
