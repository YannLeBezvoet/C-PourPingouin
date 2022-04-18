# Le C++ Pour les Pingouins

## Introduction

Bonjour mes pingouins, ce cours s'adresse aux débutants comme aux confirmés voulant approfondir des notions de C++.

Il est conseillé aux débutants de lire ce cours dans l'ordre et à ceux voulant approfondir leur connaissance du C++
d'aller directement aux notions voulues via le sommaire.

Bon il y a quand même quelques prérequis pour ce cours : avoir beaucoup de café et posséder un canard en plastique.


## Sommaire

- [Présentation du C++](#Présentation-du-C++)
- [L'IDE](#L'IDE)
- [Hello world](#Hello-world)

## Présentation du C++

Ici, ce n'est pas Wikipédia donc si tu veux lire l'historique du langage tu vas sur Google, je vais présenter seulement ce
qui va te servir pour coder histoire que les trois flemmards dans le fond ne décrochent pas.

Le C++ est un langage de programmation **compilé**, c'est-à-dire qu'à la différence d'autres langages (comme le Python
par exemple), le code n'est pas lu par un logiciel tiers, mais est transformé en un exécutable (le fameux ".exe")
directement lisible par la machine. Le logiciel permettant cette transformation est appelé "**compilateur**".

Le C++ utilise ce que l'on appelle "**la programmation orienté objet**", mais avant d'entrer là-dedans, voyons les bases.

Cette présentation est volontairement raccourcie au possible pour ne pas perdre les débutants

## L'IDE

_Cette partie ne s'adresse qu'aux débutants_

Alors c'est bien joli tout ça, mais on ne va pas coder sur word.
Pour developer on a truc qui s'appel l'**IDE**, ça veut dire _environnement de development intégré_, pour les puristes🥸
en anglais, c'est _Integrated Development Environment_. En bref, c'est un logiciel qui fait te permet d'avoir ton éditeur
de texte, ton compilateur et ton debugger tout en un.

Ici j'utilise CLion, alors cet IDE est gratuit pour les étudiants, donc si tu as une adresse mail universitaire profite,
c'est gratos pour toi, sinon il faut payer ou utiliser un autre logiciel tel que Visual Studio.

## Hello world

Bon je vous vois venir "agneugneugneu c'est quand qu'on commence à coder" du calme mes pingouins.
Bon déjà on va créer un nouveau projet :

<img src="rcs/newProject.png" alt="Nouveau Projet"/>

Et vous aller choisir l'option "C++ executable" puis renommer votre projet en "HelloWorld" :

<img src="rcs/HelloWorld.png" alt="HelloWorld"/>

Comme CLion fait tout à votre place, il va vous créer directement le programme "Hello World" :

```
#include <iostream>

int main() {
    std::cout << "Hello, World!" << std::endl;
    return 0;
}
```

Vous pouvez compiler votre programme avec l'icône de marteau ou compiler puis exécuter votre programme avec la fleche en
haut à droite de votre écran.

Normalement après exécution de votre programme vous devriez-voir apparaitre ceci dans une console:
```
Hello, World!
```

Chouette c'est votre premier programme, je vous mentirais si je vous disais que je pouvais dès maintenant tout expliquer
sur ce programme, mais retenez que :

- La première ligne ```#include <iostream>``` sert à charger de nouvelles fonctionnalités au C++, comme celle d'afficher des messages à l'écran.
- La ligne ```int main()``` permet de créer la fonction principale de votre code, c'est à partir de là que votre code 
sera lu.
- Pour la ligne ```std::cout << "Hello, World!" << std::endl;``` le mot clé ```cout``` permet d'afficher du texte séparé par
l'opérateur ```<<``` tandis que ```endl``` permet un retour à la ligne (mais pas que 😉)/
- ```return 0``` marque la fin du programme (en fait c'est plus compliqué que ça, vous verez dans le chapitre sur les
fonctions que je suis un peu un menteur).
- La dernière accolade permet de clore la fonction ```main```.

Vous remarquerez que le mot clé ```std::``` revient à plusieurs reprises, et que plus nous allons multiplier le nombre
```cout``` plus il va falloir l'écrire.

Une petite parade à ça consiste à inclure cette ligne dans le fichier ```using namespace std;```.

Ce qui nous donne :

```
#include <iostream>

using namespace std;

int main() {
    cout << "Salut les pingouins" << endl;
    return 0;
}

```

Felicitation vous avez écrit votre premier programme et vous n'avez rien compris parce que j'ai simplifié au maximum,
maintenant il est temps de coder pour de vrai !