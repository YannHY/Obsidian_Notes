# Formatage du texte 

Comme pour les titres jusqu'au niveau 6, tout les marqueurs MarkDown de formatage du texte disponibles dans Obsidian sont remplacés par leurs balises HTML correspondantes.

## Corps de Texte

```md
On peut obtenir du _texte_ avec *simple emphase* rendu en *italique*,
 du __texte__ avec **forte emphase** rendu en **Gras**,
  du **_Texte_** à la fois en **gras** et en *italique*,
   du `code source` rendu en caractères `monospaces`,
    du ~~texte barré~~  rendu avec une ligne en travers du texte.     
     On peut aussi ==surligné==.

En regardant le code
qui produit cette phrase,
vous remarquerez que
même
si
on
fait 
des
retours
à
la
ligne
dans
le
code,
le texte                s'affiche              sans rupture
dans un seul            et                  même paragraphe
et les espaces      laissés en trop         sont supprimés...

Pour former des paragraphes séparés, il faut laisser une ligne vide entre eux.

Pour forcer le retour à la ligne dans un paragraphe,  
il faut ajouter deux espaces à la fin d'une ligne  
avant de faire un retour à la ligne...
```

> Le code MarkDown ci-dessus saisi en **activant les sauts de lignes stricts dans les options de l'éditeur d'Obsidian** produira :

On peut obtenir du _texte_ avec *simple emphase* rendu en *italique*,
 du __texte__ avec **forte emphase** rendu en **Gras**,
  du **_Texte_** à la fois en **gras** et en *italique*,
   du `code source` rendu en caractères `monospaces`,
    du ~~texte barré~~  rendu avec une ligne en travers du texte.
     On peut aussi ==surligné==.

En regardant le code
qui produit cette phrase,
vous remarquerez que
même
si
on
fait 
des
retours
à
la
ligne
dans
le
code,
le texte                s'affiche              sans rupture
dans un seul            et                  même paragraphe
et les espaces      laissés en trop         sont supprimés...

Pour former des paragraphes séparés, il faut laisser une ligne vide entre eux.

Pour forcer le retour à la ligne dans un paragraphe,  
il faut ajouter deux espaces à la fin d'une ligne  
avant de faire un retour à la ligne...

> Il est donc préférable d'**activer les sauts de lignes stricts dans les options de l'éditeur d'Obsidian** pour ne pas avoir de mauvaises surprises avec les retours à la ligne simples lors du passage d'Obsidian à MkDocs.
***
> MkDocs avec Material offre davantage de [formatage de texte ](https://squidfunk.github.io/mkdocs-material/reference/formatting) mais il ne sont pas compatible avec Obsidian.

