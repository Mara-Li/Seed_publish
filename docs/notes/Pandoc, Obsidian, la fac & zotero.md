---
share: True
---
Souvent, on peut se demander "mais comment, bon dieu on peut continuer à utiliser word pour nos mémoires ?" car Word-google doc a de nombreux (très nombreux) problème. 

Ici, mon problème principal était lié à ma documentation. En effet, dès que mes profs éditaient le fichier, ma biblio sautait et je n'avais que mes numéros et mes yeux pour pleurer. Pas très ouf pour s'y retrouver n'est-ce pas ? Surtout quand on peut écrire facilement en Markdown un fichier où citer un tableau, graphique, ou un document équivaut à citer le numéro du tableau, image, ou une clé unique de citation créée par BibLatex.

Ici, je détaillerai les étapes pour écrire un rapport pour la Faculté de Lyon1 sans s'arracher les cheveux.

# Les logiciels

- [Pandoc](https://pandoc.org/) et [Python](https://pypi.org/)
- [Zotero](https://www.zotero.org/) et son extension [Better BibTex](https://retorque.re/zotero-better-bibtex/)
- [Pandoc xnos](https://github.com/tomduck/pandoc-xnos)

Une fois cela fait, pour faciliter votre boulot, vous pouvez créer un dossier "Export" pour faciliter la configuration. Dans ce fichier export, vous allez mettre : 
- [Le filtre "lua" pour les pagebreak](https://raw.githubusercontent.com/pandoc/lua-filters/master/pagebreak/pagebreak.lua) (clic droit -> enregistrer sous)
- [Le modèle docx adapté pour les mémoire de Lyon 1](https://docs.google.com/document/d/1P285wZw6rle2CIIC3f3HY3Ja64pHjQYq/edit?usp=sharing&ouid=109400928673768266798&rtpof=true&sd=true)

Ensuite, vous devez créer, dans le dossier d'export deux fichier [yaml](https://fr.wikipedia.org/wiki/YAML): `default.yml` et `page.yml`

# Configuration

Afin de créer votre configuration, il reste encore deux étapes : 
- Exporter votre bibliothèque Zotero en format better bibtex, en activant la synchronisation.
- Télécharger un modèle de citation (que vous pouvez retrouver [ici](https://www.zotero.org/styles))
Pour plus de faciliter, placer ses deux fichier dans le dossier `export`.

## Les fichiers yml

Note : Le chemin complet vers exort sera nommé `Users\export` mais vous devez modifier ce chemin par le véritable chemin ABSOLUE vers les fichiers. Sous windows, pour faciliter les choses : clic droit sur un fichier => Copier en tant que chemin d'accès.

Vous êtes obligé de doubler tous les `\` sous Windows. 

!!! WARNING
	Vos images ne sont pas trouvées magiquement par pandoc, n'oubliez pas de créer un dossier dans lequel elles seront rangés & nommée. 
	Ici, le dossier sera nommée `Users\export\attachment`

Dans `default.yml` : 
```yaml
filters:
	- 'Users\\export\\pagebreak.lua'
	- pandoc-xnos
csl: 'Users\\export\\style-zotero.csl' #Style zotero téléchargé précédemment
bibliography: 'Users\\export\\bibliography.bib' #Bibliography exportée précédemment 
resource-path: ['Users\\export\\attachment'] #N'oubliez pas les []
data-dir: 'Users\\mon_memoire' #Dossier contenant les fichiers markdown de votre mémoire
reference-doc: 'Users\\export\\custom-reference.docx' #Le fichier docx téléchargé prédemment
citeproc: true
from: markdown+lists_without_preceding_blankline+spaced_reference_links+hard_line_breaks+yaml_metadata_block+implicit_figures #Permet d'écrire du markdown plus facilement
standalone: true
metadata-file: 'Users\\export\\page.yml' 
input-files: # Contiendra tous les fichiers qui seront "compilé" pour créer votre mémoire. Ci-dessous un exemple
	- 'User\\mon_memoire\\Remerciements.md'
	- 'User\\mon_memoire\\Abbréviations.md' # Je fais mes abbréviations à la main, mais pandoc permet aussi de faire un fichier automatiquement exprès
	- 'User\\mon_memoire\\Résumé.md'
	- 'User\\mon_memoire\\Introduction.md'
# Attention, les fichiers doivent être mis dans l'ordre dans lequel ils doivent être lu. 
to: docx
output-file: 'User\\export\\Memoire_Master_2.docx'
```


Ensuite, dans le fichier `page.yml` : (donné à titre d'exemple)
Les images sont sous forme : `![description](nom de l'image)`. Pandoc cherchera automatiquement le même nom dans `resource-path` définie dans `default.yml`.
```yaml
title: |
	![logo-lyon1](Logo_lyon1.png)  
	\
	Nom du mémoire
#Les deux espace après le lien vers l'image est EXTRÊMEMENT important ! Ne les oubliez pas.
author: 
	- Nom Prénom
	- Fonction
	# Je mets ici plein de truc pour la mise en forme
date: |
	Date de la soutenance
	\
	\
	![Logo_laboratoire](logo_laboratoire){style="width=60%"}  
# Je mets le logo du laboratoire en fin, avec un style afin de permettre à pandoc de forcer le centrage de l'image.
subtitle: |
	Maître de stage: X Y
	Laboratoire d'accueil : NOM
	ADRESSE
	CP VILLE PAYS
fig_caption: yes
numbersections: true
toc: true
toc-title: Sommaire
toc-depth: 6
xnos-number-by-section: true
tablenos-plus-name: tableau
fignos-plus-name: figure
```


# L'écriture
Maintenant, vous pouvez utiliser n'importe quel logiciel pour ouvrir des fichiers markdown pour rédiger votre mémoire. 
Personnellement, j'utilise [Obsidian](https://obsidian.md/)avec [Pandoc Reference List](https://github.com/mgmeyers/obsidian-pandoc-reference-list)et [Zotero Desktop Connector](https://github.com/mgmeyers/obsidian-zotero-desktop-connector)

Pour :
- Citer un article : Copier/coller la clé pandoc tel que : `[@auteurNomannée]` comme `[@chenAgeassociatedSARSCoV2Breakthrough]` (astuce : chercher ses clés dans google vous donnera l'article aussi 😊)
- Citer et nommé un tableau : 
	- Créé votre tableau tel que :   
	```md  
	| Tableau | X |  
	|:--------|---|  
	|Truc|Machin|  
	Table: Demonstration d'une table {#tbl:id1}  
	```  
	- Ensuite, pour citer un tableau : "`+@tbl:id1` est un simple tableau.""
	Notons que vous pouvez citer des tableaux dans différents fichiers, avec l'aide de l'id qui doit être unique.
- Pour les images : 
	- `![Caption description](image.png){#fig:img-1}`
	- Et pour citer : `+@fig:img-1`
Pandoc xnos utilise à chaque fois la même idée de citation, avec toujours un `{#type:id}` où chaque `id` est unique, et `type` peut être `fig`, `tbl`... 
!!! note
	Juste pour info, vous aurez un warning de la part de citeproc, qui n'aura aucun impact sur l'export

# La commande pandoc
Maintenant que tout semble configuré, il vous suffit plus qu'à lancer la commande pour compiler le rapport. 

```sh
pandoc --defaults "User\Export\default.yml"
```

Oui, c'est tout, puisque toute la configuration se trouve dans le fichier `default.yml`