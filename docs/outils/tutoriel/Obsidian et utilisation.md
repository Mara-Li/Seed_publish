---
share: true
title: "Comment j'utilise Obsidian"
category: outils/tutoriel
tags:
- Obsidian
---

Comme je l'ai déjà dit dans [[../Obsidian]], mon utilisation du logiciel diffère assez des autres utilisateurs. 
En effet, j'utilise une hiérarchie de dossier principalement, notamment parce que c'est aussi plus facile d'y naviguer directement depuis l'explorateur et, personnellement j'ai moins de soucis pour parcourir mentalement.

Mon astuce se trouve dans l'utilisation du plugin [Folder Note](https://github.com/aidenlx/alx-folder-note), et [Dataview](https://github.com/blacksmithgu/obsidian-dataview). 

Globalement, j'utilise principalement Obsidian pour écrire des fiches RPs, avec comme hiérarchie de dossier :
```sh
Nom du perso/
├─ Illustration/
│  ├─ Gallerie (*)
├─ RP rattaché 1/
│  ├─ Fiche RP rattaché
│  ├─ Relations
│  ├─ RP rattaché 1 (*)
├─ Fiche RP 2
├─ Nom du perso (*)
```

Note : les fichiers marqué d'un astérisque sont invisibles dans Obsidian s'ils ont le même nom que le dossier. Il est possible de personnaliser le comportement de Folder Note. Par exemple, vous pouvez les mettre à l'extérieur ou utiliser le nom "index" par défaut. 
Typiquement, pour la fiche de [[../../Compendium/Hayleen May/index|(i) Hayleen May]], le truc ressemble à ça :
![[../../assets/img/Pasted image 20220126170658.png]]
Mais en réalité, le dossier est composé comme ça :
![[../../assets/img/Pasted image 20220126171043.png|800]]
![[../../assets/img/Pasted image 20220126171006.png]]

Généralement, les notes servant de folder note (celles ayant le même nom que le dossier) sont des indexs, avec des liens vers les autres fichiers. Ca me permet d'accéder rapidement aux autres fichiers et d'avoir une vue d'ensemble. 
D'ailleurs, j'hésite pas à placer un tableau au début des fiches (qui se fait automatiquement) par dataview pour avoir encore une vue d'ensemble et des raccourcis vers les autres fichiers.

C'est d'ailleurs pour ça que j'utilise beaucoup des métadonnées pour classés mes fiches et leur donner une apparence précise quand je les cite. 
![[../../assets/img/Pasted image 20220126172840.png]]
(Ces apparences spéciales sont faites par un snippet CSS bordélique et par l'utilisation du plugin [SuperchargedLink](https://github.com/mdelobelle/obsidian_supercharged_links)). 

Ensuite, j'écris mes fiches exactement comme je le ferai dans Word/Google Note, les liens et les trucs mignons en plus. Mes fichiers sont justes "mieux" rangés, et mes images ne se perdent plus vraiment. Et, bonus, je peux garder une galerie littéralement à porté de main dans Obsidian, et faire un lien dessus. Pratique pour les refs de personnages.

Ce qu'Obsidian a changé dans l'écriture des fiches, c'est que j'ai tout à un même endroit, et ça ne bouge pas. Aussi, j'adore le markdown et je préfère largement écrire en Markdown. Le plus, c'est que je peux m'amuser avec du HTML plutôt que de me prendre la tête avec word/google doc.

Alors oui, certains font des trucs super jolie/aesthetic sur leur fiche mais pour être honnête je préfère un truc utilisable (surtout sur tel) qu'un truc BG.

Point bonus : Les CSSclass me permettent aussi d'avoir un affichage spécifique sur un fichier précis. Du genre, une fiche en cours ? Je mets une typo qui fait brouillon. C'est jolie pour les yeux, et ça permet de savoir où on se situe visuellement.
*(Note : Ma typo pref pour ça c'est [Fantasque Sans Mono](https://github.com/belluzj/fantasque-sans), une chouette typo Open-Source monotype donc pratique pour lire.)*

# Pour résumé
Du coup, par rapport à un gros fichier GDOC avec une page de garde, je décompose en plusieurs petit fichier avec un index, qui sera à la racine du dossier. L'index pointe vers les fichiers donc j'ouvre un fichier et j'ai comme si c'était un fichier "unique" et pas plusieurs fichiers mis bout à bout. 

Sauf que contrairement à un fichier GDOC énorme, j'ai pas à scroller pour atteindre une partie précise, surtout si je fais quel fichier éditer. En plus de ça, pas de soucis au niveau des formats des images, et ce genre de chose.
Pareil, plutôt que de péter entièrement la mise en forme quand je rajoute une partie, j'ai juste à rajouter un fichier. 

C'est plus léger et pratique, et ça me convient super bien. 

Typiquement le "carnet" de [[../../Compendium/Mnémosyne/index|(i) Mnémosyne]] pour [[(Fiche) Mnémosyne (Lagendia)|Lagendia]] ressemble à ça :
![[../../assets/img/Pasted image 20220126174208.png]]
(Petit bonus : Relation est un dossier, donc si je veux prendre des notes sur un perso, ça me créera un fichier automatiquement en cliquant sur le lien, et j'aurai **rien** à bouger.)