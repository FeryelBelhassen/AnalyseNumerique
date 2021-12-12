<h2> Interpolation Polynomiale </h2>

<h3> Objectif du TP: </h3>

L’objectif de ce TP est d’implémenter les polynômes d’interpolation de Lagrange et newtoon divisée. Pour cela nous réalisons et testons en Python ces deux polynômes qui servent à remplacer par des fonctions simples. 

<h3><b>Exercice 1: Méthode de Lagrange</h3></b>
 Dans cet exercice, nous étudions la méthode de Lagrange qui permet de résoudre de manière très efficace des problèmes d'une grande variété en utilisant des coordonnées généralisées. 
Le polynôme d’interpolation de Lagrange est l’unique polynôme de degré au plus n. 
On dispose de **(n+1) couples Xi=[xi,fi]** Le polynôme d’interpolation de Lagrange qui passe exactement par ces (n+1) points .<br>
Dans notre exercice ,la fonction PR prend comme paramètres X et Y deux tableaux : <br>
X prend les **Xi** et Y prend les **fi**<br> X=[1 ,2 ,3 ,4,-2];<br> Y=[-1, 0, 2 ,1,3];

 <table>
   <tr>
       <th>Xi</th>
       <td>X1</td>
       <td>X2</td>
       <td>X3</td>
       <td>X4</td>
       <td>X(-2)</td>
   </tr>
  
   <tr>
      <th>fi</th>
      <td>-1</td>
      <td>0</td>
      <td>2</td>
      <td>1</td>
      <td>3</td>
     
   </tr>
 </table>

Ce polynôme a pour expression :

 ![lagrange](https://user-images.githubusercontent.com/91917391/145247881-6de706b9-1f20-48a8-b40a-d5a02f0cf952.gif)

 
La méthode d’interpolation de Lagrange présente deux inconvénients majeurs: <br>

•	Si on approche une fonction f(x) par un polynôme d’interpolation, on fera évidemment des erreurs c’est l’erreur d’approximation e(x) = P(x) − f (x), x ∈ [x0, xn] peut ne pas diminuer si on augmente le nombre des points d’interpolation. <br>
•	La méthode n’est pas récurrente: il n’y a pas de récurrence avec Pn(x) et Pn+1(x)

<h3><b>Exercice 2: Phénomène de Runge</b></h3>

Le phénomène de Runge il est un problème avec tous les 'interpolation polynomiale de noeuds espacés régulièrement polynômes degré de haut. Elle consiste à augmenter l'amplitude d'erreur dans le voisinage des limites.
On a vu que  le phénomène de Runge qui se traduit par une mauvaise interpolation, lorsque l'on augmente le degré du polynôme d'interpolation de Lagrange de la fonction :

![runge](https://user-images.githubusercontent.com/91917391/145248645-65efcaa3-ab4d-46b1-afc5-f553efd0467f.gif)

 
Le but du cet exercice est d'observer ce phénomène mais aussi de mettre en œuvre une meilleure répartition des points d'interpolation à l'aide des racines des polynômes de Tchebychev et de constater l'atténuation du phénomène de Runge.
 
<h3><b>Exercice 3: Méthode des différences divisées</h3></b>
Un inconvénient de l’interpolation de Lagrange est lorsqu’on ajoute un point xN+1 aux points existants x0, x1, • • • , xN , on a recours à recalculer tous les éléments Li pour chaque i = 0, • • • , N+1, 2 c’est à dire, à répéter tout le travail et donc une perte de temps. 2. 

<b>Formule de Newton :</b> Ici, on utilise une autre alternative, dite l’alternative de Newton (ou méthode des différences divisées). Cette méthode ne diffère de l’interpolation lagrangienne que par la manière dont le polynôme est calculé, le polynôme d’interpolation qui en résulte est le même. Pour cette raison, on parle aussi plutôt de la forme de Newton du polynôme de Lagrange. Le polynôme d’interpolation de Newton associé à la fonction f aux nœuds x0, x1, • • • , xN s’écrit comme suit :

![divisee](https://user-images.githubusercontent.com/91917391/145249094-8ffb6b11-65df-45cd-995a-526e3f62f766.gif)
 
L’avantage de l’interpolation de Newton est lorsqu’on ajoute un nouveau point xN+1 aux points déjà existants on a conservé qu’on a obtenu  lors de calcul de p(x) par contre à l’interpolation de Lagrange  lorsqu’on ajoute un point xN+1, on a recours à recalculer tous les éléments Li pour chaque i = 0, • • • , N+1 c’est à dire, à répéter tout le travail et donc une perte de temps. 

<b>Calcul Manuelle</b>
<center>
 <table>
   <tr>
       <th>i</th>
       <th>xi</th>
       <th>yi</th>
   </tr>
   <tr>
       <td>0</td>
       <td>-1</td>
       <td>6</td>
   </tr>
   <tr>
       <td>1</td>
       <td>0</td>
       <td>1</td>
   </tr>
  
   <tr>
       <td>2</td>
       <td>2</td>
       <td>3</td>
   </tr>
  
   <tr>
       <td>3</td>
       <td>5</td>
       <td>66</td>
   </tr>
</table>
</center>

![Lagrange1](https://user-images.githubusercontent.com/91917391/145270553-1583ad91-5b6a-4941-b1ff-52e74e6ddc70.gif)<br>

![lagrange2](https://user-images.githubusercontent.com/91917391/145275313-537516d9-aa04-43ab-973b-132890f61757.gif)

![Newtoon](https://user-images.githubusercontent.com/91917391/145271215-47e13da4-eb38-4cd2-8274-733a826f2145.gif)

<h3> Conclusion: </h3>
La méthode de différences divisées est meilleure que la méthode de lagrange.

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/FeryelBelhassen/AnalyseNumerique/625b44902025069a04d2912ad18f007a2a130d1b?urlpath=lab%2Ftree%2FTP2%2FTP2_E.ipynb)
