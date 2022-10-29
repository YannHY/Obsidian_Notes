# Dataview
- [Dataview plugin snippet showcase](https://forum.obsidian.md/t/dataview-plugin-snippet-showcase/13673) (À CONSULTER : plein de choses intéressantes)
- [Documentation](https://blacksmithgu.github.io/obsidian-dataview/#/functions) (currently out of date)
	- [Data Annotation](https://blacksmithgu.github.io/obsidian-dataview/data-annotation/)
	- [Queries](https://blacksmithgu.github.io/obsidian-dataview/query/queries/)
	- [Examples](https://blacksmithgu.github.io/obsidian-dataview/query/examples/)
	- [Expressions](https://blacksmithgu.github.io/obsidian-dataview/query/expressions/)
	- 
- [Plugin](https://github.com/blacksmithgu/obsidian-dataview) (GitHub)

## YouTube
<iframe width="560" height="315" src="https://www.youtube.com/embed/sEgzrRNkgsE" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<iframe width="560" height="315" src="https://www.youtube.com/embed/jW5pD4SioFM" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## List
Faire une liste (liste toutes les notes de votre vault) (ou utiliser `list from ""`)
````
```dataview
list
```
````

Faire une liste contenant un tag spécifique
````
```dataview
list from #Google or #iPad
```
`````

### Boolean operators
Faire une liste d'un dossier spécifique (possibilité d'utiliser les opérateurs booléens `AND` et `OR` ou encore le signe `-` pour exclure un terme)
````
```dataview
list from "Documentation" and #Google 
```
`````

````
```dataview
list
from "Écriture/Medium" and -#Houry
```
`````

Concaténer le fichier, le chemin menant à ce fichier et ajouter `:)`. 
````
```dataview
list "File Path: " + file.path + " :)"
from #iPad  
```
````

Liste toutes les notes avec les liens conduisant (coming into) dans la note sélectionnée
````
``` dataview
list
from [[Google]]
```
````

Liste toutes les notes avec les liens qui mènent vers (going out of) d'autres notes
````
```dataview
list
from outgoing([[Google]])
```
````

Une liste de listes
````
```dataview
list authors
from "Écriture/Medium"
```
`````

### Where
Utiliser `where`
`>`, `>=`, `<`, `<=`, `=`, `!=` (n'est pas égal)
Après "where", utiliser  `where {condition}`

````
```dataview
list from #Google 
where file.size > 1000
```
````

````
```dataview
list from #Google 
where file.name != 1000
```
````

## Tables
On peut faire des tables !!!!

```dataview
table authors
from "Écriture/Medium"
```

### sort field asc or desc
````
```dataview
table Rating
from "Notes"
sort Rating desc
```
````

### Group
À revoir. Pas bien compris. Vidéo trop rapide.

````
```dataview
table Rating, rows.file.name
from "Notes"
group by Rating
```
````

Lister toutes les notes sans tag
```dataview
list
where length(file.tags) = 0
```

<hr>

```dataview
TABLE file.name, file.outlinks SORT file.outlink DESC
```

```dataview
TABLE file.mtime AS "Last Modified" FROM "Documentation" SORT file.mtime DESC
```

```dataview
table file.mtime from "Documentation"
sort file.name asc
```