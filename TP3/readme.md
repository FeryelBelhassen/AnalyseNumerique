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
  "Méthode de Simpson" et "Méthode Milieu".</b>
  
  
  * **Méthode de Rectangle:**
  Dans cette méthode, on calcule l’intégrale numérique en réalisant une somme de surfaces de rectangles. Le domaine d’intégration est découpé en intervalles et on fait comme si la fonction restait constante sur chaque intervalle.

Sur chaque intervalle, on réalise ainsi l’approximation suivante :![image](https://user-images.githubusercontent.com/91917391/145693440-397a5172-b2d1-4adf-b1db-ddf0b5667601.png)
En choisissant une subdivision régulière de pas **xi+1 - xi = (b - a)/n** , donc indépendant de i avec une valeur de n "suffisamment grande".<br>
L'erreur commise est:
![image](https://user-images.githubusercontent.com/91917391/145694299-a1432739-25f8-4dd6-94dc-6b59d77a7aed.png) avec h= h = (b - a)/n .

![image](https://user-images.githubusercontent.com/91917391/145694523-699baac0-9d29-4682-ba81-7bbe43fb49db.png)
 
<b> =></b> **On conclure que cette méthode est exacte pour les fonctions constantes. Plus généralement, elle est d’autant plus précise que le nombre de points. Elle est une méthode d’ordre 1.**

  * **Méthode de trapèze:**
  La méthode d'intégration approchée dite des trapèzes consiste à remplacer l'arc de courbe MiMi+1 par le segment [MiMi+1] : c'est une interpolation linéaire. Soit N un entier non nul. On considère ici la subdivision xk = a + kh avec h =b−a/N (le pas de la subdivision) et k = 0, · · · , N. Donc xk+1 − xk = h (le pas est donc la diffèrence entre
chaque deux points consécutifs.) 
Ainsi, la valeur approchée de I par la formule composite des trapèzes est:
![image](https://user-images.githubusercontent.com/91917391/145694009-fe9252dc-f0d3-4fbe-bfe8-6ee83924ff85.png)<br>
L'erreur est: ![image](https://user-images.githubusercontent.com/91917391/145694814-828c0298-4f52-4f04-9176-c4639e83e135.png)

![image](https://user-images.githubusercontent.com/91917391/145695185-d5d28085-28f9-4ac4-88a9-d45587e9765c.png)

<b> =>A nouveau, cette méthode est exacte pour les fonctions constantes et affines (et même les paraboles en fait). Plus généralement, elle est d’autant plus précise que le nombre de points est grand et l’erreur décroit comme 1/n2. Elle est une méthode d’ordre 2.</b>

* **Méthode de Simpson:**
Soit N un entier non nul pair. On considére ici la subdivision xk = a + kh avec h =b−a/N (le pas de la subdivision) et k = 0, · · · , N. Donc xk+1 − xk = h. On a x0 = a 
et xN = b. En appliquant de meme ici la relation de Chasles, la formule composite de Simpson est donnée comme suit :<br>
![image](https://user-images.githubusercontent.com/91917391/145695401-4946f59c-b23b-4eca-91f9-2de8f5866228.png)<br>
L'erreur est: <br>![image](https://user-images.githubusercontent.com/91917391/145695419-7c201a85-1e77-4c65-98e9-7ec61e30170f.png)<br>
![image](https://user-images.githubusercontent.com/91917391/145695515-2f9e2f80-fa23-4eba-9e6f-ae4f28b4a504.png)<br>

 <b>=>Plus le nombre de points est grand, plus la méthode est précise. La méthode de Simpson est une méthode d’ordre 4.</b>
 
 * **Méthode du Point Milieu:**
Cette méthode utilise Ègalement le polynÙme constant pour approximer la fonction f. Cependant, elle exploite mieux les symètries du problème en choisissant la valeur milieu:<br>
![image](https://user-images.githubusercontent.com/91917391/145696963-0b3e4c34-1e73-480a-b5c1-feca92d4b541.png)<br>
L'erreur:il peut etre estimée en utilisant les développements en sÈrie de Taylor, ou le thèorème des accroissements finis. On trouve alors pour <b>h = b-a</b><br>

![image](https://user-images.githubusercontent.com/91917391/145697188-8ca26bc7-d8fa-43ee-be2a-6d31d48c50da.png)


<b>=>Du fait , cette mèthode d'intègration est exacte pour les fonctions f constante, mais aussi pour les fonctions affines .Dans le cas plus gènèral, cette mèthode est d'autant 
plus précise que les variations de f sont faibles .</b><br>
<b>=>Plus le domaine [a;b] est petit, plus l'erreur est faible. Cette mèthode du point milieu est toujours plus prècise que la mèthode rectangle.</b>



  <h4><b>Analyse comparatif des quatre méthodes:</h4><br></b>
  
  * On prend l'intervalle **[-3.32,3.06]**, le nombre de subdivision **n égale à 5** et notre fonction est **f(x)=sin(x)**

| Méthodes  | L'intégrale          | L'erreur               |
|-----------|----------------------|------------------------|
| Rectangle | 0.07466363874007897  | -0.061389388204362516  |
| Trapèze   | 0.011420427812558706 | 0.0018538227231577557  |
| Simpson   | -0.7879443813318426  | 0.8012186318675592     |
| Milieu    | 0.014220456986109    | -0.0009462064503925373 |


* On prend l'intervalle **[-3.32,3.06]**, le nombre de subdivision **n égale à 10** et notre fonction est **f(x)=sin(x)**

|  Méthodes |      L'intégrale     |        L'erreur        |
|:---------:|:--------------------:|:----------------------:|
| Rectangle | 0.04444204786309393  | -0.031167797327377466  |
| Trapèze   | 0.012820442399333715 | 0.0004538081363827471  |
| Simpson   | 0.013287113928258716 | -1.286339254225402e-05 |
| Milieu    | 0.01350231645617229  | -0.0002280659204558274 |

* On prend l'intervalle **[-3.32,3.06]**, le nombre de subdivision **n égale à 50** et notre fonction est **f(x)=sin(x)**

|  Méthodes |      L'intégrale     |        L'erreur        |
|:---------:|:--------------------:|:----------------------:|
| Rectangle | 0.019580538034059364 | -0.006306287498342902  |
| Trapèze   | 0.01325621694130733  | 1.8033594409131923e-05 |
| Simpson   | 0.013274270162622252 | -1.962690578984072e-08 |
| Milieu    | 0.013283269170265379 | -9.01863454891641e-06  |

* On prend l'intervalle **[-3.32,3.06]**, le nombre de subdivision **n égale à 10** et notre fonction est <b>f(x)=x**2+x-1</b>

|  Méthodes |     L'intégrale    |        L'erreur        |
|:---------:|:------------------:|:----------------------:|
| Rectangle | 12.827161955206417 | 1.5605038578138721     |
| Trapèze   | 14.801082835424289 | -0.41341702240399947   |
| Simpson   | 14.387665813020293 | -3.552713678800501e-15 |
| Milieu    | 14.180957301818294 | 0.2067085112019953     |

* On prend l'intervalle **[-3.32,3.06]**, le nombre de subdivision **n égale à 25** et notre fonction est <b>f(x)=x**2+x-1</b>

|  Méthodes |     L'intégrale    |       L'erreur       |
|:---------:|:------------------:|:--------------------:|
| Rectangle | 13.66424418451778  | 0.7234216285025088   |
| Trapèze   | 14.453812536604932 | -0.06614672358464269 |
| Simpson   | 11.593653905746976 | 2.7940119072733136   |
| Milieu    | 14.354592451227973 | 0.0330733617923169   |

<b>=> Plus le nombre de subdivisions augmente , plus l'erreur et l'intégrale diminuent.
Plus le nombre de points est grand, plus la méthode est précise.Plus le domaine [a;b] est petit, plus l'erreur est faible. La mèthode du point milieu est toujours plus prècise que la mèthode rectangle.
La méthode de Simpson esr plus précise que celle du trapèze car elle donne une valeur approchée plus proche de la valeur exacte.</b>



<h3>Conclusion Générale:</h3>
En conclusion, l'intègraltion numèrique est une mèthode pour calculer une valeur approximative d'une fonction qui est compliqueè d'une autre cotè, l'intègration numèrique permet d'estimer l'intègrale de cette fonction par la mèthode d'interpolation avec certain erreur.

<br>
[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/FeryelBelhassen/AnalyseNumerique/main?labpath=https%3A%2F%2Fgithub.com%2FFeryelBelhassen%2FAnalyseNumerique%2Fblob%2Fmain%2FTP3%2FExemple%2520TP3.ipynb)


