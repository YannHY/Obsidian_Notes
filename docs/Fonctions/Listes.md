> Contrairement à MkDocs, avec Obsidian on n'est pas obligé de sauter une ligne pour commencer une liste. L'extension [mdx-breakless-lists](https://pypi.org/project/mdx-breakless-lists/) installée ici dans le `mkdocs.yml` élude ce problème en ajoutant systématiquement une ligne dans le code traduit pour MkDocs par rapport à celui venant d'Obsidian.

## Liste à puces

```md
Une liste uniformément pucée :
* Un élément de ma liste ;
- Un autre élément de ma liste ;
    * Un élément de ma sous-liste ;
    * Un autre élément de ma sous-liste ;
+ Encore un autre élément de ma liste.
```

Une liste uniformément pucée :
* Un élément de ma liste ;
* Un autre élément de ma liste ;
- Encore un autre élément de ma liste ;
    * Un élément de ma sous-liste ;
    - Un autre élément de ma sous-liste ;
+ Encore un autre élément de ma liste.

> Contrairement à Obsidian, dans MkDocs les changements de types de puces ne provoquent pas de saut de ligne supplémentaire.

## Liste ordonnées

```md
Une liste bien ordonnée :

4. Le premier élément de ma liste ;  
1. Le second élément de ma liste ;
    1. Le premier élément de ma sous-liste ;
    72. Le second élément de ma sous-liste ;
1024. Le troisième élément de ma liste.
```

Une liste bien ordonnée :

4. Le premier élément de ma liste ;  
1. Le second élément de ma liste ;
    1. Le premier élément de ma sous-liste ;
    72. Le second élément de ma sous-liste ;
1024. Le troisième élément de ma liste.

> Contrairement à Obsidian, dans MkDocs démarrer avec un `4.` ne débute pas la numérotation à 4. même si on fait un saut de ligne avant de commencer la liste.

## Liste de taches

```md
- [ ] Une tâche de ma todo liste ;
- [x] Une autre tâche de ma todo liste ;
    - [x] une sous tâche de ma todo liste ;
    - [ ] une autre sous tâche de ma todo liste ;
- [ ] Encore une autre tâche de ma todo liste.
```

- [ ] Une tâche de ma todo liste ;
- [x] Une autre tâche de ma todo liste ;
    - [x] une sous tâche de ma todo liste ;
    - [ ] une autre sous tâche de ma todo liste ;
- [ ] Encore une autre tâche de ma todo liste.

> Contrairement à Obsidian, dans MkDocs cocher le bouton d'une tâche ne barre pas le texte de cet item et cocher le bouton d'une tâche supérieure ne raye pas toutes les tâches de sa sous-liste sans exception.