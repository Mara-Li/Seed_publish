---
share: True
title: "Pourquoi Obsidian ?"
---
# Introduction

Pourquoi ai-je choisi Obsidian par rapport à d'autres app de prise de note ? À la base, parce que c'est une application en **markdown**, **gratuite** et **disponible sur téléphone**. Pourquoi j'ai continué à l'utiliser, par rapport à Notion ou ClickUp ? 
- Pour la personnalisation,
- Les plugins

Il y a beaucoup à dire sur Obsidian. Personnellement, je n'utilise pas tout un tas de fonction, notamment les liens entre les notes ou les tags. Mais le fait est qu'Obsidian m'offre le choix de les utiliser ou non : je peux donc utiliser parfois des tags, mais aussi des dossiers.


# Obsidian Vanilla

Obsidian, sans plugin, offre déjà pas mal de fonction cool. Certaines sont liées au markdown en lui même, d'autres, les cores features d'Obs-.

## Le markdown

Déjà, on se demande pourquoi j'utilise et j'adore le markdown ? Parce que c'est **simple** à utiliser. On l'utilise déjà tous sur Discord, Messenger... Ici, on a :
- `**gras**` : Pour le **gras**.
- `*italic*` : Pour l'*italic*
- ` ==Surlignement==` : Pour ==surligner==

(Oui, contrairement à Discord, on peut pas souligner, je sais). On peut fusionner ses mises en formes et en plus, le markdown est supporté par de nombreuses apps et workflow. Du coup, facile de C/C un long message directement d'Obsidian directement sur Discord sans avoir à retoucher la mise en forme !

En outre, Obsidian supporte les tables (bon, les tables en MD c'est... Pas trop ça) et le latex, je peux donc faire :
- Des maths, comme $x+y=12$ (`$x+y=12$`) 
- Des tableaux (oui, logique)

Des tableaux tel que :
```md
| Je suis un titre   | Je suis un deuxième titre |
| ------------------ | ------------------------- |
| Je suis du contenu | Et moi aussi              |
```


(Je sais, c'est moche)

Ah oui, vous pouvez aussi insérer directement du HTML pour vous amuser un peu aussi. 

## Les trucs d'Obsidian
### Wikilinks
Déjà, Obsidian permet de citer des parties, voire des notes, où quelle soit dans votre architecture. Du coup, par exemple, je peux faire une note uniquement avec mes formules de maths puis les citer, plutôt que de réécrire 45 fois la formule. Ça marche aussi pour les définitions ou les OC que vous réutilisez.

Il est possible de faire ça de deux manières :
- Soit en utilisant les wikilinks, comme ceci : `[[wikilinks]]` pour juste créé un lien, et `![[wikilinks]]` pour carrément inséré la note dans la note actuelle. Il est possible d'utiliser/créé des alias de notes...
- Soit avec la syntaxe MD : `![titre](wikilinks)`.

J'adore les wikilinks, parce qu'ils sont plus facile à lire et courts. Le truc, c'est contrairement au MD de base, les wikilinks sont peu/pas supportés par les autres applications. 

### Live Preview
On va pas se mentir, le Live Preview c'est littéralement la raison pour laquelle j'utilise Obsidian. C'est super fluide, bien que ce soit récent (le LP est sortie cet hiver). Le LP c'est le fait que la syntaxe change automatiquement en utilisant la syntaxe MD / HTML. Avant, il fallait switcher entre le mode lecture et écriture. C'était pas hyper pratique, mais on s'y faisait assez rapidement.

Notons que le LP est, à l'heure où j'écris ses lignes, en bêta sur mobile et ça marche super super bien. De fait, les images et différents attachements s'affichent directement !

### Les options
Obsidian permet de carrément personnaliser l'utilisation, et on peut complètement désactiver/activer des core features. Vous pouvez donc avoir un Obsidian bourré d'option/outils, ou un truc giga simple. En plus, on peut personnalisée notre vue comme on veut : je peux mettre mon plan à droite, avoir ma liste de dossiers et fichier à gauche...

![[Pasted image 20220121203402.png]]
(*Feat mes fautes*)

### La vue graphique et les tags
Il faut savoir que je n'utilise quasiment pas la vue graphique et les tags. Je préfère une organisation hiérarchique par dossier, et il y a déjà énormément d'article à ce sujet. En gros, pour résumé vite-fait : vous pouvez avoir un affichage de vos notes avec des liens entre elles.

Plutôt pratique pour suivre les relations d'un sujet, d'un personnage... 
![[Pasted image 20220121204230.png]]
Par exemple, ici, on voit bien les trucs reliés à mes cours et ceux qui sont reliés au RP. 

Y'a encore et encore d'autres trucs, genre, afficher les liens entrants-sortants d'une note, les templates... 

Mais je veux juste faire une petite présentation de l'app' moi !

# Les extensions Obsidian : Le vrai endgame

Obsidian peut être étendu. Facilement : il suffit de le vouloir et savoir coder en JS. Même moi j'ai pu créer ma propre extension, alors que le JS ce n'est pas ma tasse de thé. Comme quoi !
Ca fait que vous n'avez pas besoin de supplier les devs pour avoir une feature. Soit, quelqu'un l'a déjà codé pour vous, soit vous pouvez le faire vous-même !

En plus, les extensions sont faciles à installer : il y a un store directement dans l'application. Par contre, les plugins ne se mettent pas à jour automatiquement, faut le faire régulièrement avec le bouton exprès. 

Deux extensions m'ont fait rester sur Obsidian : [Language Tool](https://github.com/Clemens-E/obsidian-languagetool-plugin) & [Admonition](https://github.com/valentine195/obsidian-admonition). Aujourd'hui, j'en utilise presque 70, et je suis activement le développement des futurs plugins. 

En outre, il existe une multitude de thèmes, et vous pouvez créer vos propres "snippet" CSS pour modifier Obsidian. Ainsi, vous pouvez créer des syntaxes MD spéciale pour avoir genre de la couleur, souligner, changer la couleur du surlignage… Ou encore personnalisée l'UI, comme moi avec mes dossiers colorés.
> Par contre, y'a pas *encore* de store snippet et l'organisation du dossier peut vite devenir chaotique. Une mise à jour est prévu, mais les devs se concentrent d'abord sur le LP. 

![[Pasted image 20220121205357.png|+side-sm]] 
Notons que les icônes sont rajoutées avec, soit, un snippet CSS (oui, c'est possible) soit un super plugin nommé Icon Folder qui n'a vraiment pas assez d'amour.

Moi qui aime avoir une vue d'ensemble rapide, les couleurs m'y aident vraiment !

# Le reste
Obsidian est gratuit, et vous pouvez stocker vos notes où vous voulez. Dans une clé USB, un disque dur, votre cloud personnel… Mais aussi dans le *Sync* d'Obsidian (payant, 5€/mois) qui est assez cool. 
Notons, comme ce sont des dossiers (des vrais, qui existent sur votre ordi), vous pouvez mettre ce que vous voulez dedans, pas que des notes Markdown : je mets mes PDF et les images relatifs à mes persos par exemple. J'en profite pour faire des notes qui réunissent les images pour faire une sorte de petite galerie. 

Sinon, y'a leur Publish, qui permet de poster des notes en ligne pour 20€/mois. Encore une fois, il existe des alternatives. Je considère la mienne comme la meilleure et si vous voulez pouvoir publier vos notes en ligne, "à la Notion" je vous conseille d'y jeter un œil : [Obsidian2Mkdocs](https://github.com/Mara-Li/mkdocs_obsidian_publish)

(Oui, je suis très fière de mon taf)

Il est aussi possible de faire des dons à la team si vous aimez l'application et que vous voulez avoir les mises à jour en avance.

Le seul hic, c'est qu'une grande majorité du contenu autour d'Obsidian est anglais, et qu'il peut sembler bizarre-difficile à prendre en main mais sincèrement, ça vaut le coup de s'y pencher !
> Une bonne description pour Obsidian est d'un.e des développeurs, Silver : Obsidian est un IDE pour écrire. Si vous avez déjà utilisé des IDE, vous ne serez pas perdu avec Obsidian.

Ah, oui, aussi : le Discord est super actif et les Devs sont hypers présent, ce qui fait plaisir à voir !

Dernière note : l'app n'est pas open source (et franchement, vu ce qu'il y a eu autour de log4shell, faker.js & color.js je dirai que c'est pas une mauvaise chose) toutefois il y a eu diverses analyses et c'est hyper sécure : les **devs** n'ont PAS accès à vos notes. Les seuls envois sur internet, c'est concernant github et les plugins (ainsi que le publish). Malgré le fait que l'app soit codé en electron, c'est hyper rapide et jolie. Pour une fois que l'on a une app en electron bien codée, j'pense que l'on peut difficilement la bouder ! 

Source (En anglais) :
- [Open sourcing of Obsidian](https://forum.obsidian.md/t/open-sourcing-of-obsidian/1515/44)
- [Obsidian Performance test](https://www.zsolt.blog/2021/05/obsidian-performance-test-take-1.html)
- [TfT Performance : Obsidian](https://www.goedel.io/p/tft-performance-obsidian)
- [Obsidian Privacy](https://cdn.discordapp.com/attachments/908731169305153606/908774932077498408/unknown.png)
- [Silver's (Erica Xu) Interview ](https://nesslabs.com/obsidian-featured-tool)