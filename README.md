# IA par renforcement - TictacToe

Groupe 1B :
- Ganassi Alexandre
- Gonzales Lenny
- Saadi Nils
- Sauva Mathieu

## Présentation du sujet
Pour le projet de modélisation, nous avons décidé de prendre le thème de l'intelligence artificielle par renforcement. Le principe d'une intelligence artificielle par renforcement réside dans son apprentissage en autonomie, l'IA apprend de ses expériences sur la base de récompense ou pénalité selon ses choix.
Pour que notre IA puisse s'exercer, nous avons choisi le jeu du Tic Tac Toe qui nous paraissait la solution la plus à même d'être utilisé. Le but du jeu est très simple, deux joueurs s'affrontent sur une grille de 3X3, posant chacun leur tour le symbole qui leur correspond (X ou O). Pour gagner un des deux joueurs doit arriver à aligner 3 symboles identiques que ce soit de manière verticale, horizontale ou en diagonale.
En ce qui concerne nos perspectives futures pour cette IA, elles sont étendues. L'intelligence artificielle par renforcement offre un éventail de possibilités. On peut notamment penser aux voitures autonomes, optimisation logistique ou encore de la production, et cetera...

## Difficultés et solutions
Après avoir choisi notre sujet, il a fallu choisir à quel jeu notre IA allé jouer, mais surtout apprendre à jouer, nous avons donc proposé plusieurs jeux qui sont simples comme le jeu de Nim, puissance 4 , et cetera… Mais en évaluant leurs difficultés, on s'est tourné vers le Tic Tac Toe, qui était assez simple pour y implémenter une IA, et avec plein de stratégies différentes pour que celle-ci puisse apprendre.
Le second problème qui s'est posé est la non-connaissance du sujet. En effet, nous n'étions pas formés au développement d'une intelligence artificielle, ce qui nous a fallu une certaine période de documentation sur ce sujet pour atteindre ce résultat.
D'un autre côté, nous avons essayé de produire le graphe orienté pondéré des états possibles du tableau de jeu. Les sommets correspondent aux états possibles du tableau de jeu, les arêtes représentent la possibilité de passer d'un état à un autre et les poids correspondent aux valeurs stockées dans le fichier de stockage. Cependant, étant donné le nombre de sommets et d'arêtes, nous avons pu générer le graphe, mais sa représentation n'est pas lisible. En effet, 3^9 = 19 683 états possibles du tableau puisque chaque case du tableau a 3 états possibles ('X', 'O', vide). Cependant, nous avons essayé de réduire ce nombre jusqu'à 6046 en enlevant les états impossibles (tableau remplit de symboles 'X', ...), mais nous n'avons pas eu le temps de l'implémenter.
Enfin, il nous a été assez difficile d'extraire les données les plus pertinentes pour réaliser des statistiques et des graphes qui le sont tout autant.

## Où sont les mathématiques ?
Les mathématiques se retrouvent à plusieurs endroits de notre programme. Nous pouvons prendre l'exemple de la variable epsilon qui nous permet d'équilibrer les actions de l'intelligence artificielle par soit de l'exploration en jouant un coup aléatoire, soit l'utilisation des connaissances qu'elle a acquis tout le long de ses parties.
La plus grosse partie mathématiques de notre projet est la partie statistique. Elle comprend notamment un diagramme en secteurs représentant les taux de victoires, défaites et égalités ainsi qu'un second diagramme de secteurs qui lui représente les types de victoires (horizontale, verticale, diagonale). De plus nous générons deux graphiques matriciels permettant de représenter la grille de jeu en exposant le nombre de fois que chaque case a été choisi comme premier et second coups à l'aide de couleurs. Enfin nous générons deux graphiques linéaires exposant l'évolution des valeurs d'apprentissages au cours des différentes parties jouées pour le joueur 1 et le joueur 2.
Enfin, les mathématiques sont également présentes lors de la mise à jour des points de l'IA, en effet, on utilise une courbe sigmoïde pour attribué plafonner la valeur avec un minimum et un maximum.