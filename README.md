Consignes :

- Compléter la premiere ligne de code pour créer une fonction maFonction qui affichera "Hello World!"
- Dans la seconde ligne de code, appeler la fonction que vous venez de créer
- Compléter la troisieme ligne pour afficher le premier parametre de ma fonction maFonctionParam
- Compléter la troisieme ligne de code pour que la fonction maFonctionParam retourne le deuxieme parametre
- Appeler cette fonction



Théorie :

Comme en Javascript, PHP permet de créer des tableaux, pour rappel, les tableaux permettent de stocker plusieurs valeurs
dans une seule variable.

Exemple :

$cars = array("Volvo", "BMW", "Toyota");
echo "I like " . $cars[0] . ", " . $cars[1] . " and " . $cars[2] . ".";

En php, on utilise array() pour créer un nouveau tableau.

Contrairement à Javascript qui ne supporte que des tableaux indéxés ( des tableaux avec un index numérique ), PHP
permet de créer également des tableaux associatifs ( des tableaux avec un index alpha-numérique ) et des tableaux multi-
dimensionels ( des tableaux contenant plusieurs tableaux )


- Pour créer des tableaux ayant un index numérique, il existe deux solutions :

$cars = array("Volvo", "BMW", "Toyota");

Ici, le tableau est créé en une seule fois, $cars[0] renverra Volvo, $cars[2] renverra Toyota ( l'index commence à 0, comme en javascript )

$cars[0] = "Volvo";
$cars[1] = "BMW";
$cars[2] = "Toyota";

Ici, le tableau est créé progressivement, PHP crée un tableau automatiquement lorsque le premier index est défini (
$cars[0] = "Volvo" )


- Pour connaitre la longueur d'un tableau, on utilisera la fonction count() :

$cars = array("Volvo", "BMW", "Toyota");
echo count($cars);

Ici , notre code retournera 3 car il y a trois valeur dans le tableau $cars

En javascript, on utilisera .length sur le tableau pour connaitre sa taille, en php l'approche est différente, le tableau
ne comporte que les valeurs qu'on lui a assigné, on utilise des fonctions spécifiques pour retourner les informations.


- Parcourir les éléments d'un tableau indéxé :

$cars = array("Volvo", "BMW", "Toyota");
$arrlength = count($cars);

for($x = 0; $x < $arrlength; $x++) {
    echo $cars[$x];
    echo "<br>";
}

Nous utilisons for pour parcourir les valeurs de notre tableau, $arrlength est égal à 3 ici , la boucle for parcourt donc
tout notre tableau.



- Tableaux associatifs :

Les tableaux associatifs permettent de définir un index sous forme de texte, on peut les créer de deux façons différentes :

$age = array("Peter"=>"35", "Ben"=>"37", "Joe"=>"43");

Ici, notre tableau associatif est créé en une seule fois, $age["Peter"] retournera 35

$age['Peter'] = "35";
$age['Ben'] = "37";
$age['Joe'] = "43";

Ici, on crée le tableau progressivement.

Si vous déclarez un tableau associatif, vous ne pourrez pas utiliser d'index numérique pour retourner les valeurs du tableau,
$age[0] retournera une erreur.


- Parcourir un tableau associatif :

Pour parcourir un tableau associatif, on peut utiliser foreach.

$age = array("Peter"=>"35", "Ben"=>"37", "Joe"=>"43");

foreach($age as $x => $x_value) {
    echo "Key=" . $x . ", Value=" . $x_value;
    echo "<br>";
}

L'intruction foreach parcourt le tableau $age et retourne deux valeurs : $x est l'index, $x_value est la valeur de chaque
entrée du tableau.


- Tableau multi-dimensionels :

Il est parfois nécessaire de stocker des valeurs sur plusieurs dimensions, un cas concret serait un jeu d'echec, les pions
peuvent être plaçés sur deux dimensions : la premiere est la largeur du plateau, la deuxieme est la longueur du plateau.

Par exemple, si on souhaite indiquer qu'un pion se trouve sur la troisieme case en largeur et la premiere case en longueur,
on pourrait écrire ceci : $echiquier[3][1] = "pion"

Il n'y a pas de limite technique sur le nombre de dimensions d'un tableau mais il est difficile pour un être humain de
représenter mentalement plus de trois dimensions ( sauf exceptions )

Pour parcourir un tableau multi dimensionel, on utilisera des boucles dans des boucles dans des boucles etc... ( bref plus
vous avez de dimensions plus vous avez de boucles )



