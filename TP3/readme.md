<h1><center>TP3:Les méthodes d’intégration numérique</h1></center><br>

<h3>Introduction:</h3><br>
L’intégration est un des problèmes les plus importants que l’on rencontre en analyse. En effet, on rencontre souvent des intégrales dont le calcul par des méthodes analytiques est très compliqué ou meme impossible, car il n’existe pas d’expression analytique d’une primitive de la fonction à intégrer. <br>

  * Si f est une fonction continue sur un intervalle [a,b], bien souvent on ne sait pas calculer une primitive de f. Ainsi, si l'on désire obtenir la valeur de ![image](https://user-images.githubusercontent.com/91917391/145692218-19fa1421-54ab-4dce-87ab-8bd81f048096.png) , il faut parfois se contenter d'obtenir une valeur approchée à l'aide d'une méthode d'intégration numérique.
  
  *  La plupart des méthodes d'intégration numérique fonctionnent sur le même principe. On commence par couper le gros intervalle [a,b] en N plus petits intervalles [ai,ai+1], avec a1=a et aN+1=b. Puis, pour chaque intervalle [ai,ai+1], on essaie d'approcher ![image](https://user-images.githubusercontent.com/91917391/145692304-0c61afe0-66a0-432e-acf9-37e8825ab190.png) <br>

Dans ces cas, on peut appliquer des méthodes numériques pour évaluer la valeur de l’intégrale donnée.<br>

<h3><b> Objectif du TP: </h3></b>
L'objectif de ce TP est de calculer l'intégrale I(a, b) et l'erreur d'intégration d'une fonction f(x) sur un certain intervalle [a, b]  et de mettre les méthodes numériques en oeuvre et de les tester .

<h3><b> Les méthodes d'intégration numérique: </h3></b>
Il existe de nombreuses méthodes pour réaliser une intégration numérique. Nous allons considérer ici quelques méthodes simples <b> "Méthode de Rectangle" "Méthode de Trapèze"
  "Méthode de Simpson" et "Méthode Milieu".</b><br>
  
  
  * **Méthode de Rectangle:**

  <h4><b>Analyse comparatif des quatre méthodes:</h4><br></b>
  
  * On prend l'intervalle **[-3.32,3.06]**, le nombre de subdivision **n égale à 5** et notre fonction est **f(x)=sin(x)**

| Méthodes  | L'intégrale          | L'erreur               |
|-----------|----------------------|------------------------|
| Rectangle | 0.07466363874007897  | -0.061389388204362516  |
| Trapèze   | 0.011420427812558706 | 0.0018538227231577557  |
| Simpson   | -0.7879443813318426  | 0.8012186318675592     |
| Milieu    | 0.014220456986109    | -0.0009462064503925373 |


**Méthode des Trapèzes:**

Principe : La méthode d'intégration approchée, dite des trapèzes, décrite par Newton & Cotes, consiste à remplacer l'arc de courbe MiMi+1 par le segment [MiMi+1] : c'est une interpolation linéaire. Si nous choisissons une subdivision régulière de l'intervalle [a,b] en n sous-intervalles [xi,xi+1] avec i variant de o à n : xo = a < x1< x2 < ... < xn = b, on a xi+1 - xi = (b - a)/n. La somme des aires colorées en jaune pointé représente une approximation J de l'intégrale I. Chaque aire est celle d'un trapèze de hauteur xi+1 - xi, de bases respectives f(xi) et f(xi+1).
>
