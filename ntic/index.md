Bienvenue ! Voici ma synthèse sur les GNN, réalisée dans le cadre du MOS 4.4 "Nouvelles Technologies de l’Information et de la Communication" à l’École Centrale de Lyon - *Said Khaboud*

![Image1](fabric.jpg)

## Deep Learning sur les graphes

### Définition :
Les réseaux neuronaux graphiques (GNN) appartiennent à une catégorie de réseaux neuronaux qui fonctionnent naturellement sur des données structurées en graphes. Bien qu'il s'agisse d'un sujet qui cause un peu de confusion, les réseaux neuronaux graphiques peuvent être résumés en une poignée de concepts simples. Le but de cet article est d’expliquer ces principes et discuter des succès et perspectives de la technologie.

### Réseaux de neurones récurrents
Nous allons choisir un point de départ un peu plus familier : les réseaux neuronaux récurrents. Comme vous le savez, peut-être, les réseaux neuronaux récurrents sont bien adaptés aux données organisées en séquence, comme les données de séries chronologiques ou le langage. La caractéristique principale d'un réseau neuronal récurrent est que l'état d'un RNN dépend non seulement des entrées actuelles, mais aussi de l'état caché précédent du réseau. Les RNN ont fait l'objet de nombreuses améliorations au fil des ans. Ils entrent généralement dans la catégorie des RNN de type LSTM avec une fonction de déclenchement multiplicative entre l'état caché actuel et précédent du modèle. Un article discutant les variantes LSTM et leur relation avec les RNN classiques peut être trouvée [ici](https://www.exxactcorp.com/blog/Deep-Learning/5-types-of-lstm-recurrent-neural-networks-and-what-to-do-with-them).

![Image2](rnn.png)

Imaginez maintenant la séquence sur laquelle un RNN opère comme un graphe linéaire dirigé, mais enlevez les entrées et les connexions pondérées, qui seront intégrées comme des états de nœuds et des bords, respectivement. En fait, supprimez également la sortie. Dans un réseau neuronal à graphe, les données d'entrée sont l'état original de chaque nœud, et la sortie est analysée à partir de l'état caché après avoir effectué un certain nombre de mises à jour définies comme un hyperparamètre.

