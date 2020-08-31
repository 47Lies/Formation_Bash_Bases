# Formation BASH

## User Interface

Communication entre l'utilisateur et la machine.

Input - Compute - Output


telephone portable

ecran tactile - les logiciels du telephone - ecran/son

Distributeur automatique de billet

clavier/écran tactile - la machine - ecran/autres parties mecaniques

Ordinateur de bureau

Entrées
clavier/souris/ecran tactile - la machine - l'écran/les haut parleurs/tout autre périphétique


Mais que fait la machine?

Interprétation des entrées - action du programme - retranscription du programme

Chacune de ces parties sont des programmes qui consomme des ressources

exemple sauvegarder un fichier dans excel

gestion de la souris (position/action d'un bouton/navigation dans les menus) 
ecoute du clavier(CTRL+S,ALT+F-ALT+S,ALT+F-flèches-entrée)

écriture d'un fichier

Le nom du fichier n'est plus rouge avec une étoile
L'icone de sauvegarde est grisée

Shell: interpréteur de commandes qui permet d'accéder aux fonctionnalités internes du système d'exploitation.

## BASH

Bash: l'interpréteur par défaut sur la plupart des systèmes Unix

Chaque système d'exploitation a une trousse à outils (programmes) de base avant même l'installation d'autres outils. Bash permets aussi l'utilisation de la plupart des programmes bioinformatiques prévus sans interface graphiques.


Invite de commande
PS1
PS2

## Commandes et concepts

### commande et options: cal

cal

cal --help

cal -h

cal --monday

cal -m

command cal - display a **cal**endar

options --monday

par convention

-h ou --help donne une breve description de la commande, ce quelle fait et ses différentes options

- option sous la forme courte une lettre en général, souvent combinable avec d'autres formes courte

-- option sous sa forme longue, human readable

pour aller plus loin

cal -year

cal -ym

### argument, variable, casse et caractères spéciaux: echo

echo "hello world"
ma_variable_pour_l_example="hello world"
echo "${ma_variable_pour_l_example}"
echo "${Ma_variable_pour_l_example}"

"hello world" est un argument passée à la commande echo, echo va donc afficher à l'écran ce que qui est entre guillemets doubles 

ma_variable_pour_l_example est une variable

elle a un nom qui aurait pu porter presque n'importe quel nom, nous vous recommandons de ne pas utiliser des noms déja utilisé, elle ne peut pas comporter de caractere de ponctuation

elle a une valeur dans notre cas une chaine de caracteres hello, un espace et enfin le mot world 

= sert d'opérateur et il assigne la valeur hello world à la variable ma_variable_pour_l_example

_ Bash interprète les espaces comme un séparateur de commandes, du coup l'emploi de l'underscore (tiret du 8) est un bon substitut

${} permets d acceder à la valeur de la variable, il existes d'autre formalisme pour acceder à la valeur de la variable mais celle ci est à toute épreuve des differents interpréteurs ainsi que de leur versions

echo va interpreter ${} comme des caracteres speciaux et va accomplir une action avec dans notre cas aller chercher la valeur d'une variable 

Ma_variable_pour_l_example pour bash ce nom est différent de ma_variable_pour_l_example, n'ayant pour l'instant aucune valeur assignée echo va donc afficher rien

pour aller plus loin

Ma_variable_pour_l_example=${ma_variable_pour_l_example}

on peut passer la valeur d'une variable en copie

echo "${ma_variable_pour_l_example}${Ma_variable_pour_l_example}"

on peut utiliser plusieurs variables en meme temps

echo -e "${ma_variable_pour_l_example}\n${Ma_variable_pour_l_example}"

\ est un caractere special pour annoncer que le caractere suivant ne doit pas etre interprétée comme un caractere special mais comme un simple caractere

\n est un caractere special pour retour à la ligne et il sera pris en compte comme tel avec l'option -e sans quoi il n'affichera qu'un n

arborescence, home, working directory, chemin absolu, chemin relatif: pwd, cd, ls

creation, copie, effacement, deplacement de fichier: touch, cp, rm, mv

creation et effacement de repertoire: mkdir, rmdir

affichage, affichage selectif, consultation 
