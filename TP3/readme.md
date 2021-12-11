<h1><center>TP3:Les méthodes d’intégrations numériques</h1></center><br>
<h3>Introduction:</h3><br>
  Si f est une fonction continue sur un intervalle [a,b], bien souvent on ne sait pas calculer une primitive de f. Ainsi, si l'on désire obtenir la valeur de , il faut parfois se contenter d'obtenir une valeur approchée à l'aide d'une méthode d'intégration numérique.
  La plupart des méthodes d'intégration numérique fonctionnent sur le même principe. On commence par couper le gros intervalle [a,b] en N plus petits intervalles [ai,ai+1], avec a1=a et aN+1=b. Puis, pour chaque intervalle [ai,ai+1], on essaie d'approcher 

**Analyse comparatif des quatre méthodes:**<br>
On prend l'intervalle **[-3.32,3.06]** , le nombre de subdivision **n égale à 5** et notre fonction est **f(x)=sin(x)**

| Méthodes  | L'intégrale          | L'erreur               |
|-----------|----------------------|------------------------|
| Rectangle | 0.07466363874007897  | -0.061389388204362516  |
| Trapèze   | 0.011420427812558706 | 0.0018538227231577557  |
| Simpson   | -0.7879443813318426  | 0.8012186318675592     |
| Milieu    | 0.014220456986109    | -0.0009462064503925373 |


**Méthode des Trapèzes:**

Principe : La méthode d'intégration approchée, dite des trapèzes, décrite par Newton & Cotes, consiste à remplacer l'arc de courbe MiMi+1 par le segment [MiMi+1] : c'est une interpolation linéaire. Si nous choisissons une subdivision régulière de l'intervalle [a,b] en n sous-intervalles [xi,xi+1] avec i variant de o à n : xo = a < x1< x2 < ... < xn = b, on a xi+1 - xi = (b - a)/n. La somme des aires colorées en jaune pointé représente une approximation J de l'intégrale I. Chaque aire est celle d'un trapèze de hauteur xi+1 - xi, de bases respectives f(xi) et f(xi+1).
